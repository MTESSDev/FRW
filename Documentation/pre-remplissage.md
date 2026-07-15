## Pré-remplir les données d'un formulaire

Le pré-remplissage permet d'initialiser automatiquement certaines données d'un formulaire à partir d'informations déjà connues par un système.

Lors de la création du formulaire, un système peut fournir un objet JSON contenant des valeurs qui seront automatiquement appliquées aux champs du formulaire.

Le pré-remplissage peut notamment être utilisé pour :

- éviter à l'utilisateur de saisir des informations déjà connues;
- réduire les erreurs de saisie;
- accélérer le remplissage du formulaire;
- transmettre des informations provenant d'autres systèmes;
- protéger certaines données qui ne doivent pas être modifiées par l'utilisateur.

Ce guide explique les grandes étapes recommandée pour construire un pré-remplissage.

### Paramètres du JSON de pré-remplissage

Le JSON de pré-remplissage peut contenir plusieurs propriétés.

#### form

Contient les données qui seront utilisées pour pré-remplir les champs du formulaire.

Les valeurs présentes dans cet objet peuvent être modifiées par l'utilisateur lors du remplissage du formulaire.

#### formProtege

Contient des données dont la valeur doit obligatoirement provenir du système autorisé.

Les champs présents dans cet objet ne peuvent pas être modifiés par l'utilisateur.

Lorsque le même champ est présent dans `form` et `formProtege`, la valeur contenue dans `formProtege` a préséance.

#### config

Permet notamment de fournir des domaines de valeurs personnalisés.

#### informationsSupplementaires

Permet de sauvegarder des informations supplémentaires associées au formulaire.

Ces informations peuvent notamment contenir un contexte ou un texte de bas de page affichables à l'utilisateur.

Les données enregistrées dans cet objet ne sont pas chiffrées et ne doivent pas contenir d'informations sensibles.

#### Propriétés personnalisées

Il est également possible d'ajouter des objets personnalisés propres à votre intégration.

Ces objets peuvent être utilisés durant le traitement de votre système à la réception d'un formulaire car ils sont redonnés en sortie par FRW au moment de la transmission.

Par exemple :

- un contexte applicatif;
- des données servant à générer une estampille;
- des informations techniques propres à votre intégration.

### Obtenir la structure d'un formulaire

> Disponible à partir de la release [2026.x](https://github.com/MTESSDev/FRW/releases).

Afin de pouvoir construire un pré-remplissage, il est recommandé d'utiliser le service **FRW119 - Obtenir la structure d'un formulaire**.

Ce service retourne :

- la structure JSON attendue par FRW;
- la liste des champs du formulaire;
- le type de chaque champ;
- les groupes répétables;
- les valeurs permises pour les champs de sélection;
- les métadonnées nécessaires à la validation des données.

#### Exemple de structure retournée

Lorsque le paramètre `vide=false` est utilisé (valeur par défaut), la propriété `structurePreRemplissage` contient des indications permettant de comprendre le format attendu pour chaque champ.

todo : insérer exemple en json

#### Comprendre les métadonnées des champs

En complément de `structurePreRemplissage`, le service retourne une collection `champs`.

Cette collection permet notamment de connaître :

- le nom du champ;
- son type;
- son groupe;
- s'il appartient à un groupe répétable;
- son nombre maximal d'occurrences;
- les valeurs permises;
- les libellés affichés à l'utilisateur;
- son caractère obligatoire.

Pour les champs de type :

- select;
- radio;
- checkbox;

la propriété `valeursPossibles` contient les valeurs pouvant être transmises au formulaire.

Exemple :

todo : intégrer cet exemple et ces commentaires dans l'exemple principal du retour de FRW119

Le pré-remplissage doit utiliser les clés techniques retournées par FRW et non les libellés affichés à l'utilisateur.

Pour les groupes répétables, les propriétés suivantes peuvent être utilisées :

todo : intégrer cet exemple et ces commentaires à l'exemple principal FRW119

#### Paramètre vide=true

Le service peut être appelé avec le paramètre optionnel `vide=true`.

Dans ce mode, la structure retournée contient directement des valeurs vides ou des valeurs par défaut plutôt que des indications de format.

Cette option peut simplifier la génération d'un modèle de pré-remplissage dans certains systèmes.

#### Utilisation recommandée

La séquence recommandée est la suivante :

1. Appeler FRW119 pour obtenir la structure du formulaire.
2. Partir de `structurePreRemplissage:form` comme modèle de départ.
3. Utiliser la collection `champs` pour comprendre les types, valeurs permises et groupes répétables.
4. Remplacer les valeurs du modèle par les données provenant de votre système.
5. Retourner le JSON obtenu comme résultat du service de pré-remplissage.
6. Utiliser le JSON obtenu lors de la création du formulaire avec FRW.

Cette approche permet de toujours travailler à partir de la structure réellement configurée dans FRW sans devoir maintenir manuellement une définition de formulaire.

#### Suggestion d'implémentation

Plusieurs approches peuvent être utilisées pour fusionner les données provenant de votre système avec la structure retournée par FRW119.

Par exemple :

- génération programmatique du JSON;
- moteurs de gabarits Mustache;
- Handlebars.Net;
- YamlHttpClient.

Le choix de la technologie utilisée demeure à la discrétion du système intégrateur.

#### Accès au service

Exemples d'appel :

```http
GET /api/v1/SIS/structureFormulaire/{typeFormulaire}

GET /api/v1/SIS/structureFormulaire/{typeFormulaire}?vide=true
```

Une fois authentifié dans Swagger :

1. Sélectionner **FRW119 - Obtenir la structure d'un formulaire**.
2. Saisir le `typeFormulaire`.
3. Exécuter la requête.
4. Copier le contenu de `structurePreRemplissage`.
5. Utiliser ce résultat comme point de départ pour construire votre pré-remplissage.

## Création versus modification

Certaines informations peuvent être prises en compte seulement au moment de la création du formulaire, d’autres peuvent aussi être modifiées lors de la reprise (reprise "authentifiée" seulement). Le tableau suivant résume les possibilités : 

| Type  d'information pré-remplie | Création | Reprise |
| ---- | ---------- | ---------- |
| Champs de formulaire (form) | ✔ |  |
| Champs de formulaire protégés (formProtege) | ✔ | ✔ |
| Propriétés personnalisées | ✔ | ✔ |
| Informations supplémentaires | ✔ |  |
| Domaine de valeurs personnalisées | ✔ | ✔ |

## Pré-remplissage anonyme
> À partir de la version ``2025.10``

Le pré-remplissage est maintenant disponible pour les formulaires anonymes, toutefois vous devez préalablement autoriser les champs concernés dans la config "form.yml" de votre formulaire ou de votre système autorisé.

> Important : 
> - Ne pas autoriser le pré-remplissage de données sensibles.
> - Le système supporte des données en pré-remplissage d'une longueur jusqu'à environ 1000 caractères maximum.

Pour plus de détails, voir la section [Personnalisation des formulaires - Concepts de base](https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=personnalisationBase) du P700.
