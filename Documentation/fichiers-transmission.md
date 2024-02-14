# Configurer la transmission

Pour que l'outil FRW puisse gérer le contenu en sortie, il faut ajouter un fichier transmission. il sera nommé `default.v0.transmission.yml` s'il est au niveau de votre répertoire système, sinon, au niveau du formulaire, il sera nommé `NOM_DU_FORM.v0.transmission.yml` où le `NOM_DU_FORM` est identique à votre nom de répertoire du formulaire.


> **Les niveaux**\
> Certains blocs de config sont [définissables à plusieurs niveaux-fichiers-config](niveaux-fichiers-config.md), par contre le comportement de chaque bloc peut différer, voici un tableau détaillant ces comportements. 
>| Bloc config  | Niveau Global | Niveau Système | Niveau Formulaire  |   Détails |
>|---|---|---|---|---|
>| etapes  |   |  X  | X  | Si le bloc `etapes` est défini au niveau `Formulaire` il écrase complètement la configuration Système |   
>| http_client  |   | X  | X  | Les éléments `http_client` se cumulent  |


Un fichier `Transmission` est principalement nécessaire au niveau `Système` et que dans certains précis cas au niveau d'un formulaire, comme par exemple pour remplacer les étapes par défaut que vous aviez défini.

# Contenu du fichier de transmission
## Étapes
Lors de la transmission, le traitement FRW exécute les étapes dans l'ordre qu'elles ont été configurées dans le fichier de transmission. Nous vous recommandons donc d'utiliser le même ordre que nous utilisons dans notre exemple plus bas.

### genererWord
Permet de produire un extrant contenant les données saisies dans le formulaire Web à partir d'un gabarit Word (docx).

Il vous est possible de vous créer un gabarit Word personnalisé ou d'utiliser celui offert par la solution FRW.

Référez-vous à la page [fichiers-bind](https://github.com/MTESSDev/FRW/blob/main/Documentation/fichiers-bind.md) pour plus de détails.

### genererPDF
Permet de produire un extrant contenant les données saisies dans le formulaire Web à partir d'un gabarit PDF avec champs de saisie dynamiques.

Il vous est possible de vous créer un gabarit Word personnalisé ou d'utiliser celui offert par la solution FRW.

Référez-vous à la page [fichiers-bind](https://github.com/MTESSDev/FRW/blob/main/Documentation/fichiers-bind.md) pour plus de détails.

### traiterDocumentsSoumis
Permet de traiter les pièces jointes que l'utilisateur a envoyé avec le formulaire. Le scan d'antivirus est effectué dans ce traitement.

Cette tâche est requise si votre formulaire permet de joindre des documents.

### extraireQuestions
Permet d'ajouter toutes les questions du formulaire dans l'objet JSON fourni lors de la transmission. Les questions sont extraites dans les deux langues lorsqu'applicable.

### ajouterEstampille
Permet d'ajouter des informations par dessus l'extrant produit par les étapes `genererWord`ou `genererPDF` pour reproduire une estampille apposée manuellement. 

L'estampille est configurée dans le fichier `bind` associé au formulaire. Il est possible de définir les informations qu'on veut afficher ainsi que sa position dans la page.

Référez-vous à la page [fichiers-bind](https://github.com/MTESSDev/FRW/blob/main/Documentation/fichiers-bind.md) pour plus de détails.

### envoyerCourriel (disponible à partir de la release [2024.2](https://github.com/MTESSDev/FRW/releases/tag/2024.2-IT))
Permet d'envoyer un courriel via le système FRW lors de la transmission du formulaire. Il faudra définir autant d'étapes "envoyerCourriel" qu'il y a de courriels différents à envoyer ainsi qu'un gabarit de courriel à utiliser pour chaque tâche.

Pour chaque gabarit courriel, il est possible :
- de spécifier une liste de destinataires, de copies conformes et de copies conformes invisibles et celles-ci peuvent être différentes entre chaque étape `envoyerCourriel`;
- d'ajouter l'extrant produit par les étapes `genererWord`ou `genererPDF` ainsi que les documents fournis par l'utilisateur en pièces jointe du courriel.
    - Il est possible de spécifier quelles pièces jointes on veut rendre disponible dans le courriel en appliquant des filtres. Se référer à l'exemple complet plus bas.
- d'utiliser des parties variables définies dans la tâche elle même.

### conserverFichier (disponible à partir de la release 2024.3)
Permet d'indiquer au système de conserver une copie du fichier produit par l'orchestration dans un répertoire interne pour être récupéré par un autre traitement.

### appelerServiceExterne
Permet de spécifier l'API externe à appeler lors de la transmission.

Il est possible de définir le comportement attendu avec l'utilisation du bouton `Tester transmission` offert dans les outils de développement afin de simuler une transmission.

Cette tâche est directement liée à la section `http_client`.

## http_client
Cette section permet de spécifier toutes les caractéristiques de l'appel à l'API défini dans l'étape `appelerServiceExterne`.

## Exemple de toutes les possibilitées de configuration
```yaml
# Liste des étapes désirées dans votre transmission.
# L'ordre est importante, le traitement la respectera
etapes:  
    # Générer Word, permet de créer un document docx/pdf/html en sortie
    # contenant questions/réponses automatiquement
    # ATTENTION: pour le moment il n'est pas possible d'activer genererPdf en même temps
    - tache: genererWord
      options:
        # (optionnel) Fichier Bind précis, sinon celui par défault
        fichierBind: NOM_FORM.v1.bind.yml  

    # Générer PDF, permet de remplir un ou des PDF avec champs de saisies
    # Il faut alors ajouter un fichier NOM_DU_FORM.v0.bind.yml pour 
    # permettre l'association des champs
    # ATTENTION: pour le moment il n'est pas possible d'activer genererWord en même temps
    - tache: genererPdf

    # Traiter documents soumis, permet de valider les pièces jointes 
    # d'un utilisateur (scan antivirus et gestion pour la sortie)
    - tache: traiterDocumentsSoumis
      options:
        # (optionnel) Permet de désactiver l'estampille (false par défaut)
        # Disponible à partir de la release 2023.11.1
        desactiverEstampille: false

    # Permet d'extraire toutes les questions du formulaire dans toutes les langues dans un objet "questionsFormulaire"
    # peu importe si la question ait été affichée ou répondue
    # Disponible à partir de la release 2023.6
    - tache: extraireQuestions

    # Ajouter estampille, permet d'ajouter une "Étampe" sur un document 
    # comme pour l'officialiser (mettre la date de transmission, 
    # le no. de confirmation, etc)
    - tache: ajouterEstampille

    # Permet d'envoyer un courriel via le système FRW. Ajoutez une tâche "envoyerCourriel" pour chaque courriel différent à envoyer.
    # Disponible à partie de la release 2024.2
    - tache: envoyerCourriel
      options:
        # Le gabarit spécifié doit être défini dans la section "gabaritsCourriels"
        gabarit: confirmation
        # Les filtres permettent de définir des documents précis à ajouter au courriel. Si aucun filtre n'est spécifié, tous les documents seront affichés dans la liste du courriel.
        # **IMPORTANT** Les filtres sont combinés entre eux (condition "ET"). Il est donc possible de spécifier un seul filtre à la fois sinon les documents seront tous exclus du courriel.
        filtresDocuments:
            #Permet de spécifier un document précis à joindre au courriel en utilisant son nom original
          - typeFiltre: nomOriginal
            # Doit correspondre au "nomSortie" défini pour le bundle dans le fichier "bind" du formulaire ou à la propriété "name" du composant de fichiers joint dans le formulaire (customFile)
            valeurs: 0006-01 - Dépôt direct
            # Permet de spécifier un document précis à exclure du courriel en utilisant son nom original
          - typeFiltre: exclureNomOriginal
            valeurs: 0006-01 - Dépôt direct
            # Permet de joindre au courriel le document produit par la tâche "genererWord"   
          - typeFiltre: tacheSource
            valeurs: genererWord
            # Permet de joindre au courriel tous les documents joints au formulaire via les contrôles de fichiers joints (customFile) 
          - typeFiltre: tacheSource
            valeurs: traiterDocumentsSoumis
            # Permet de joindre au courriel le document produit par la tâche "genererPDF"
          - typeFiltre: tacheSource
            valeurs: genererPDF
            # Permet de sélectionner des documents selon une métadonnée qui aura été spécifiée dans le formulaire pour la pièce jointe
          - typeFiltre: metadonnee
            clee: TypeDocument
            valeurs: 
              - INFOPERS 
              - SANTE
              - REVENU
        # Permet de définir des conditions pour déclencher l'envoi du courriel.
        # Il est possible d'utiliser "conditionsET" ou "conditionsOU", mais pas en même temps.
        conditionsEt:
          - condition: '=='
            champFormulaire: 'donneesFormulaire.form.adulte1Sexe'
            valeur: 'Masculin' 
          - condition: "=="
            champCalcule: "{{#ifCond donneesFormulaire.form.adulte1Langue '==' 'Francais'}}true{{/ifCond}}"
            valeur: true   
        # Permet de définir des parties variables à utiliser dans le courriel.
        partiesVariables: 
          partie1: 'Une'
          partie2: 'de test'

    # Conserver une copie du fichier produit par l'orchestration dans un répertoire interne pour être récupéré par un autre traitement.
    - tache: conserverFichier

    # Appeler service externet permet d'appeler un API de dépôt.
    - tache: appelerServiceExterne
      options: 
        # Nom du client à utiliser
        # (il doit être inscrit dans le fichier default.v0.transmission.yml) 
        # dans le bloc de config "http_client:"
        client: appel_externe      

        # Permet de désactiver l'appel à ce service web lors du clique sur le bouton "Tester transmission" de l'interface des outils de développement
        # Options disponibles : ignorer, simuler ou encore retirer l'option pour que l'étape s'exécute sur le bouton tester transmission
        modeBoutonTesterTransmission: simuler 

# Liste des gabarits de courriel pour la tâche "envoyerCourriel"
gabaritsCourriels:
  - id: confirmation
    # Liste des destinataires (peut être une liste)
    a:
      tous: 
        - 'esun-a02@essais.mess.gouv.qc.ca'
    # Liste des copies conformes (Facultatif, peut être une liste)
    cc:
      tous:
        - 'esun-a05@essais.mess.gouv.qc.ca'
    # Liste des copies conformes invisibles (Facultatif, peut être une liste)
    cci:
      tous:
        - 'esun-a04@essais.mess.gouv.qc.ca'
    # Nom de l'expéditeur (Par défaut, "Formulaires en ligne" ou "Online forms" selon la langue)
    nomExpediteur: Test FRW Transmission
    # L'objet du courriel peut contenir des parties variables
    objet: '{{envoyerCourriel.partiesVariables.partie1}} demande {{envoyerCourriel.partiesVariables.partie2}}'
    # Les données du formulaires peuvent être réutilisées dans le contenu du courriel
    corps: |
      <p>ceci est un test</p>
      <p>Exemple1a : {{donneesFormulaire.form.Exemple1a.0}}, Exemple1b : {{donneesFormulaire.form.Exemple1b.0}}</p>
        # Pour faire afficher les documents téléchargeables, il faut ajouter le tableau ci-dessous. Une liste contenant chaque document avec son nom original dans FRW sera ajoutée au contenu du courriel. Sur le clique du lien, le document sera téléchargé.
        <ul>
          {{#listePJ}}
        <li><a href="{{url}}">{{nomOriginal}}</a></li>
          {{/listePJ}}
        </ul>

# La liste des clients http
http_client:
  # Nom de votre client, ici appel_externe
  appel_externe:
    # Méthode d'appel de votre API, Peut-être POST, PUT, PATCH ou autre... normalement POST est le meilleur choix
    method: POST
    # Url de votre API, des paramètres en GET ici peuvent être passés, il est possible de mettre des variables aussi
    url: http://votreapi.ministere.gouv.qc.ca/api/endpoint
    # Tous les headers que votre API doit reçevoir sont ici, possible aussi de mettre des variables
    headers:
      Accept: application/json
    content:
      # Ici le json_content que nous allons passés à votre API, vous êtes libres de mettre la structure que vous voulez, {{{Json .}}} permet de tout "dumper" les variables de l'application vers votre API (voir Variables ci-dessous), utile aussi pour connaître les variables/objets disponibles
      json_content: |
          {{{Json .}}}
      # Utile pour valider que l'appel s'est bien terminé en 200 avec une validation du retour de contenu de votre API en prime
      check_response:
        throw_exception_if_body_not_contains_all:
            - success # À remplacer par un code de retour ou un mot retourné par votre api afin de valider que tout est concluant
``` 


## Variables et contenu

Variables du bloc `http_client` utilisables dans le style `mustache`. Tout le bloc `http_client` est basé sur l'outil [YamlHttpClient](https://github.com/anisite/YamlHttpClient), vous pouvez vous y référer pour bâtir votre `json_content`.

| Variable | Type/Valeur | Description |
| ---      |----         | ---         |
| langue | `fr`, `en`    | Langue d'affichage du formulaire |
| noFormulaire | numérique   | Numéro unique séquentiel du formulaire |
| noConfirmation | numérique  | Numéro unique de confirmation, peut-être validé par un agent, termine par ``311`` |
| noExecution | numérique  | **Ne pas utiliser sera retiré**|
| documentsProduits | objet | Liste des documents produits par FRW (pdf, word) par les tâches `genererWord` et `genererPdf` <details><summary>**documentProduit**</summary>**nom** : Le nom du document généré en sortie<br> **fichier** : Le contenu du fichier en ``base64``</details>|
| donneesFormulaire | objet | Tout le contenu ``formulaire`` inclus, `form`, `config` et vos objets passés en pré-remplissage<details><summary>**donneeFormulaire**</summary>**form** : Les données du formulaire<br> **config** : Certaines configurations<br> **AUTRES** : Vos objets personnalisés</details>|
| configDev | objet | Contenu spécial pour les essais, configurations developpeurs/analystes|
| fichiersExternes | objet | Contenu d'un ou des fichiers requis en sortie |
| contenuFormulaireJson | string | **Ne pas utiliser sera retiré** Contenu du formulaire tel que stocké dans la BD |
| IdUtilisateur| string |Identifiant de l'utilisateur reçus lors de la création du formulaire | 
| dateTransmission | date | Date de transmission correspondant au moment où l'utilisateur clique sur le bouton pour transmettre le formulaire | 
| modeSimulation | booléen | `true` si l'appel provient du bouton Tester transmission | 
| documentsSoumis | objet | Liste des documents soumis par les utilisateurs (pièces jointes au formulaire). C'est la tâche `traiterDocumentsSoumis` qui renseigne cet objet en préparant et validant vos fichiers. <details><summary>**documentSoumis**</summary>Il s'agit d'un dictionnaire contenant comme clée le nom du ``champ pièce jointe`` et comme valeur un tableau d'objet. <br>Chaque objet contient alors:<br>**url** : Le nom du fichier à utiliser tel quel lors de l'appel à l'API `Telecharger`.<br>**name** : Le nom de la pièce jointe et son type (ex: ``GrpPJCertificatNaissance_0_PJCertificatNaissance.pdf``)<br>**AUTRES** : Les métadonnées (extraites automatiquement, il s'agit des autres champs dans le même groupe qui sont convertis comme métadonnées automatiquement ex: `LigneAffaire`, `TypeDocument`)</details>|
| questionsFormulaire <br> `Disponible à partir de la version 2023.6` | objet | Contient **toutes** les questions associées à des champs du formulaire dans toutes les langues disponibles.<details><summary>**questionsFormulaire**</summary>Il s'agit d'un dictionnaire contenant comme clée l'identifiant de la question et comme valeur un tableau d'objet. <br>Chaque objet contient alors:<br>**label** : Le libellé de la question. <br> **options** : Le libellé des choix pour les questions à choix multiples.<br> **components** : Contient une structure de **label** et **options**. Il s'applique lorsqu'on a des libellés dans un groupe.</details>|
| InformationsSupplementaires `Disponible à partir de la version 2023.6` | objet | Contient les informations supplémentaires.


[Exemple de json produit par FRW en sortie vers un API externe](exemple-json-appeler-service-web.md)
