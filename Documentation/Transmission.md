# Configurer la transmission

Pour que l'outil FRW puisse gérer le contenu en sortie, il faut ajouter un fichier transmission. il sera nommé `default.v0.transmission.yml` s'il est au niveau de votre répertoire système, sinon, au niveau du formulaire, il sera nommé `NOM_DU_FORM.v0.transmission.yml` où le `NOM_DU_FORM` est identique à votre nom de répertoire du formulaire.


> **Les niveaux**\
> Certains blocs de config sont [définissables à plusieurs niveaux](Niveaux.md), par contre le comportement de chaque bloc peut différer, voici un tableau détaillant ces comportements. 
>| Bloc config  | Niveau Global | Niveau Système | Niveau Formulaire  |   Détails |
>|---|---|---|---|---|
>| etapes  |   |  X  | X  | Si le bloc `etapes` est défini au niveau `Formulaire` il écrase complètement la configuration Système |   
>| http_client  |   | X  | X  | Les éléments `http_client` se cumulent  |


Un fichier `Transmission` est principalement nécessaire au niveau `Système` et que dans certains précis cas au niveau d'un formulaire, comme par exemple pour remplacer les étapes par défaut que vous aviez défini.

## Exemple de toutes les possibilitées de configuration
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
    # ATTENTION: pour le moment il n'est pas possible d'activer genererPdf en même temps
    - tache: genererWord
      numeroExecution: 02
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
      # Ici le json_content que nous allons passés à votre API, vous êtes libres de mettre la structure que vous voulez, {{{Json .}}} permet de tout "dumper" les variables de l'application vers votre API, utile aussi pour connaître les variables/objets disponibles
      json_content: |
          {{{Json .}}}
      # Utile pour valider que l'appel s'est bien terminé en 200 avec une validation du retour de contenu de votre API en prime
      check_response:
        throw_exception_if_body_not_contains_all:
            - success # À remplacer par un code de retour ou un mot retourné par votre api afin de valider que tout est concluant
``` 
Tout le bloc `http_client` est basé sur l'outil [YamlHttpClient](https://github.com/anisite/YamlHttpClient), vous pouvez vous y référer pour bâtir votre `json_content`.

## Variables 

| Variable | Description |
| --- |----|
|IdUtilisateur| Identifiant de l'utilisateur reçus lors de la création du formulaire |
||Tableau à compléter...|

