# Configurer la transmission

Pour que l'outil FRW puisse gérer le contenu en sortie, il faut ajouter un fichier transmission. il sera nommé `default.v0.transmission.yml` s'il est au niveau de votre répertoire système, sinon, au niveau du formulaire, il sera nommé `NOM_DU_FORM.v0.transmission.yml` où le `NOM_DU_FORM` est identique à votre nom de répertoire du formulaire.


> **Les niveaux**\
> Certains blocs de config sont [définissables à plusieurs niveaux](Niveaux.md), par contre le comportement de chaque bloc peut différer, voici un tableau détaillant ces comportements. 
>| Bloc config  | Niveau Global | Niveau Système | Niveau Formulaire  |   Détails |
>|---|---|---|---|---|
>| etapes  |   |  X  | X  | Si le bloc `etapes` est défini au niveau `Formulaire` il écrase complètement la configuration Système |   
>| http_client  |   | X  | X  | Les éléments `http_client` se cumulent  |


Un fichier `Transmission` est principalement nécessaire au niveau `Système` et que dans certains cas au niveau d'un formulaire, comme par exemple pour remplacer le comportement par défaut que vous aviez défini.

## Créer votre premier fichier de transmission

Pour débuter et tester un premier coup votre fichier de transmission, il est recommandé de débuter avec un fichier nommé `default.v0.transmission.yml` que vous créez à la racine, donc au niveau système là ou tous vos répertoires de formulaires sont.

Amusons-nous à simuler un appel vers un API fictif afin de se familiarisé avec la solution et les diverses options. Cette étape est pratique aussi pour se faire une idée des données que votre API pourra recevoir lorsqu'elle sera configurée.

Copiez-y ensuite le contenu ci-dessous tel quel :

```yaml
# Ajouter une tâche pour l'appel à un service web, même si vous n'avez pas encore d'API, copiez tel quel.
etapes:
- tache: appelerServiceExterne
  options:
    client: mock
    modeBoutonTesterTransmission: simuler # Permet d'indiquer de ne pas effectuer l'appel

# Définir un http client de "mock"
http_client:
  mock:
      method: POST
      url: http://votreapi.ministere.gouv.qc.ca/api/endpoint
      headers:
          Accept: 'application/json'
      content:
         # Permet de tout "dumper" les variables de l'application vers votre API
        json_content: |
          {{{Json .}}}
      check_response:
        throw_exception_if_body_not_contains_all:
            - success # À remplacer par un code de retour ou un mot retourné par votre api afin de valider que tout est concluant
```

Vous pouvez maintenant [déployer](Déployer.md). 

Une fois le déploiement terminé, rendez-vous sur votre formulaire et lancez les [outils de développement](Documentation/Outils-developement.md)

Il suffira alors de remplir quelques champs pour tester et cliquer sur `Tester transmission` pour voir apparaître les données que votre API aurait reçues si elle avait été réellement appelée.

```yaml
# Liste des étapes désirées dans votre transmission.
# L'ordre est importante, le traitement la respectera
etapes:  
    # Différer selon plage de disponibilité
    # Permet de demander au traitement d'attendre une période spécifique pour
    # exécuter les prochaines étapes
    - tache: differerSelonPlageDisponibilite
        # (Fonction avancée) Permet de spécifier lors de quelle "batch" 
        # d'exécution nous voulons exécuter la tâche 
      numeroExecution: 01
      options:
        # (Fonction avancée) Numéro d'exécution, permet de faire plus d'une batch d'appels 
        execution: 02

    # Générer Word, permet de créer un document docx/pdf/html en sortie
    # contenant questions/réponses automatiquement
    - tache: genererWord
      numeroExecution: 02
      options:
        # Fichier Bind est requis pour générer WORD pour préciser quel 
        # fichier nous allons utiliser
        fichierBind: NOM_FORM.v1.bind.yml  

    # Générer PDF, permet de remplir un ou des PDF avec champs de saisies
    # Il faut alors ajouter un fichier NOM_DU_FORM.v0.bind.yml pour 
    # permettre l'association des champs
    - tache: genererPdf

    # Traiter documents soumis, permet de valider les pièces jointes 
    # d'un utilisateur (scan antivirus et gestion pour la sortie)
    - tache: traiterDocumentsSoumis

    # Ajouter estampille, permet d'ajouter une "Étampe" sur un document 
    # comme pour l'officialiser (mettre la date de transmission, 
    # le no. de confirmation, etc)
    - tache: ajouterEstampille

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
``` 
