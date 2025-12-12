# Guide Utilisateur : FRW.PDFBinder

## 1. Présentation
**FRW.PDFBinder** est un outil permettant de configurer le mappage ("binding") entre des données techniques (JSON) et les champs visuels d'un formulaire PDF (comme le Bail du Tribunal administratif du logement).

### URL

URL de l'outil de binding : https://formulaires.it.mtess.gouv.qc.ca/binding/1/3003/

Dans cet exemple, c'est le formulaire 3003 du système autorisé 1 (ECS).

Vous pouvez remplacer "1" par le numéro de votre système autorisé, et "3003" par votre identifiant de formulaire.


## 2. Interface Principale
L'écran d'accueil affiche le formulaire en mode prévisualisation.

### A. Navigation et Options (Haut de page)
* **Liens YAML** : Permet de *Télécharger le fichier YAML* de configuration ou de *Copier le contenu* dans le presse-papier.
* **Onglets de documents** : Basculez entre les différents fichiers du dossier (ex: `53000 - BAIL`, `Ajout`, `Annexe 6`).
* **Version anglaise** : Un lien permet de visualiser les PDF en version anglaise.

### B. Légende des couleurs (État des champs)
Les champs sur le PDF sont colorés pour indiquer leur état de configuration :
* **🟩 Vert (Champ assigné)</span>** : Le champ est correctement lié à une donnée source.
* **🟨 Jaune (Champ non-assigné)</span>** : Le champ est vide et n'a aucune donnée liée.
* **🟥 Rouge (Source inexistante)</span>** : Le champ est lié à une variable qui n'existe plus ou est introuvable.

---

## 3. Configurer un champ (Assignation)

Pour configurer ou modifier un champ, cliquez simplement sur la zone colorée (verte, jaune ou rouge) directement sur le PDF. La fenêtre **"Assignation source"** s'ouvre.

### Détails de la fenêtre d'assignation :

1.  **Champ du PDF** :
    Indique le nom technique du champ dans le document PDF (ex: `Avertisseur_Date_locateur`).

2.  **Sélection de la donnée (Champ(s) et valeur(s))** :
    * Utilisez la barre de recherche pour trouver la variable de données (ex: `signatureLocateurPrincipal.0.Date`).
    * Vous pouvez cocher "Afficher même les valeurs assignées" pour voir toutes les options disponibles.

3.  **Optionnel: Formatage de la donnée (SmartFormat)** :
    Cette section permet de transformer la donnée brute avant de l'afficher, nécessaire dans certains cas plus complexes.
    * **Formules rapides** : Cliquez sur les liens bleus pour insérer automatiquement des formats courants (ex: `yyyy-MM-dd` pour les dates, `Chiffres seulement` pour les nombres).
    * **Formule (optionnel)** : Zone de texte pour éditer manuellement le formatage.
        * *Exemple visible* : `{signatureLocateurPrincipal.0.Date:dd MM yyyy}` (Transforme la date en format Jour/Mois/Année avec des espaces).
    * **Formule Anglaise** : Permet de définir un formatage spécifique si le formulaire est généré en anglais.

### Validation
* Cliquez sur **Enregistrer** pour sauvegarder la liaison et fermer la fenêtre.
* Le champ sur le PDF devrait maintenant apparaître en **Vert**.

---

## 4. Astuces
* **Vérification visuelle** : Avant de terminer, parcourez tout le document pour vous assurer qu'il ne reste aucun champ **Jaune** (sauf si l'information est optionnelle) ou **Rouge** (erreur).
* **SmartFormat** : Pour des formatages complexes, référez-vous à la documentation "SmartFormat" mentionnée dans la fenêtre d'assignation.




## 5. Syntaxe de Binding (fichier bind.yml)

Notez que les formules sont normalement appliquées avec la fenêtre de binding de l'outil. La documentation ici détaille la structure du fichier mais aussi des formules qui peuvent être saisie directement dans l'interface.

### 📌 Structure Générale

Chaque définition de champ suit ce modèle :

```yaml
Nom_Du_Champ_PDF:
  champs: [Chemin.Vers.Donnee]
  formule: '{Expression}'
```

* **champs** : Liste des propriétés JSON requises pour que la formule fonctionne.
* **formule** : Chaîne de caractères définissant la logique d'affichage.

---

### 🛠 Opérateurs et Syntaxe

#### 1. Interpolation Simple
Affiche directement la valeur d'une donnée. On peut combiner plusieurs valeurs et du texte statique.

* **Syntaxe** : `'{Chemin}'`
* **Exemple** :
    ```yaml
    formule: '{locateurs.0.adresse.0.Municipalite}, {locateurs.0.adresse.0.Province}'
    ```
    *Résultat :* `Montréal, Québec`

#### 2. Conditionnelle Ternaire
Évalue une condition booléenne.
* **Syntaxe** : `'{Condition:{ValeurSiVrai}|{ValeurSiFaux}}'`
* **Exemple** : Si un représentant est défini, utiliser son courriel, sinon utiliser celui du locateur.
    ```yaml
    formule: '{locateurs.0.questionRepresentant:{locateurs.0.courrielRepresentant}|{locateurs.0.courrielLocateur}}'
    ```

#### 3. Fonction `include()`
Vérifie si la valeur d'un champ correspond à une chaîne spécifique ou à une liste d'options (séparées par `|`).

* **Syntaxe** : `'{Chemin:include(valeur):{SiVrai}|{SiFaux}}'`
* **Exemple (Choix multiple)** : Si le nombre de pièces est "autre", afficher la précision textuelle.
    ```yaml
    formule: '{nbPieces:include(autre):{nbPiecesAutre}|{nbPieces}}'
    ```
* **Exemple (Case à cocher)** : Retourne `true` seulement si le mode est chèque ou chèque postdaté.
    ```yaml
    formule: '{modePaiement:include(cheque|chequePostDate):true}'
    ```

#### 4. Formatage de Date
Formate une date selon un masque spécifique. Les espaces sont littéraux (utiles pour l'alignement dans les cases PDF).

* **Syntaxe** : `'{CheminDate:format}'`
* **Exemple** :
    ```yaml
    formule: '{dateDebutBail:dd          MM          yyyy}'
    ```
    *Résultat :* `01          07          2025`

#### 5. Vérification `isnullOrEmpty`
Vérifie si une valeur est nulle ou vide.

* **Syntaxe** : `'{Chemin:isnullOrEmpty:{SiVide}|{SiNonVide}}'`
* **Exemple** : Cocher une case "Oui" si le champ n'est pas vide.
    ```yaml
    formule: '{annexe6ServicesLoisirs.0.accesActivitesLoisirs:isnullOrEmpty:false|true}'
    ```
>Notez que la formule ne retournera rien et ne s'exécutera pas si ``annexe6ServicesLoisirs.0.accesActivitesLoisirs`` est ``null`` dans le code.

#### 6. Conditions sur les Collections (`Length`)
Permet d'effectuer des conditions basées sur la taille d'une liste (array).

* **Syntaxe** : `'{Chemin.Length:cond:Operateur?{SiVrai}|{SiFaux}}'`
* **Exemple** :
    ```yaml
    formule: '{locateurs.Length:cond:>=3?true|false}'
    ```

---

### 📝 Exemples Complexes

#### Concaténation Conditionnelle
Si la propriété est une copropriété, afficher les initiales, sinon ne rien afficher (ou afficher autre chose).

```yaml
formule: '{logementCoproprieteDivise:include(true):{signatureLocataire1.0.Initiales}    {signatureLocataire3.0.Initiales}}'
```

#### Logique de Fallback (Date)
Utiliser la `dateRemiseReglementImmeuble`. Si `possedeRemiseReglementImmeuble` est faux, utiliser alors la `X-DateTransmission`.

```yaml
formule: '{dateRemiseReglementImmeuble:dd          MM          yyyy}{possedeRemiseReglementImmeuble:include(false):{X-DateTransmission:dd          MM          yyyy}}'
```





# Gif de l'outil 

![Animation](https://github.com/MTESSDev/FRW/blob/main/Documentation/images/Outil_Binding.gif)
