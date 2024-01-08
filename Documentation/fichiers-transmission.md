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

### genererPDF
### traiterDocumentsSoumis
### extraireQuestions
### ajouterEstampille
### envoyerCourriel
### appelerServiceExterne

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
        # Il est possible de définir des parties variables à utiliser dans le courriel.
        partiesVariables: 
          partie1: 'Une'
          partie2: 'de test'

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
    # Le PDF du formulaire produit par FRW ainsi que les pièces jointes ajoutées au formulaire peuvent être ajoutées au courriel. Un lien de téléchargement peut être affiché pour chaque fichier dans le courriel.
    corps: |
      <p>ceci est un test</p>
      <p>Exemple1a : {{donneesFormulaire.form.Exemple1a.0}}, Exemple1b : {{donneesFormulaire.form.Exemple1b.0}}</p>
      {{#each listePJ}}
        {{#ifCond @first '=' True}}
        <br>
        <ul>
        {{/ifCond}}
          <li><a href="{{url}}">{{nomOriginal}}</a></li>
        {{#ifCond @last '=' True}}
        </ul>
        {{/ifCond}}
      {{/each}}

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
