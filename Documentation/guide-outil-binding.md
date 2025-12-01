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

3.  **Formatage de la donnée (SmartFormat)** :
    Cette section permet de transformer la donnée brute avant de l'afficher.
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


# Gif de l'outil 

![Animation](https://github.com/MTESSDev/FRW/blob/main/Documentation/images/Outil_Binding.gif)
