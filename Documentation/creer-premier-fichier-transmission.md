# Créer votre premier fichier de transmission

> Le présent guide vous explique comment créer une config de transmission **simple** pour votre premier formulaire. Toutefois, le guide [fichiers-transmission.md](/Documentation/fichiers-transmission.md) est plus complet et détaille toutes les tâches possibles.

Pour débuter et tester un premier fichier de transmission, il est recommandé de débuter avec un fichier nommé `default.v0.transmission.yml` que vous créez à la racine, donc au [niveau système](niveaux-fichiers-config.md), là où tous vos répertoires de formulaires sont.

Amusons-nous à simuler un appel vers un API fictif afin de se familiariser avec la solution et les diverses options. Cette étape est pratique aussi pour se faire une idée des données que votre API pourra recevoir lorsqu'elle sera configurée.

Copiez-y ensuite le contenu ci-dessous tel quel :

```yaml
# Ajouter une tâche pour l'appel à un service web, même si vous n'avez pas encore d'API, copiez tel quel.
etapes:
  # Traiter les documents transmis par les utilsateurs dans votre formulaire
  - tache: traiterDocumentsSoumis
  # Générer un document style questions/réponses à partir d'un gabarit word (gabarit par défaut)
  - tache: genererWord
  # Ajouter une estampille aux documents
  - tache: ajouterEstampille
  # Appeler une API externe pour la transmision
  - tache: appelerServiceExterne
    options:
      # Le nom du client HTTP à utiliser (doit être défini dans l'objet http_client)
      client: appel_externe
      # Permet d'indiquer de ne pas effectuer l'appel reel en mode test
      modeBoutonTesterTransmission: simuler

# La liste des clients http désirés, ici seulement appel_externe est défini
http_client:
  appel_externe:
    method: POST
    url: http://votreapi.ministere.gouv.qc.ca/api/endpoint
    headers:
      Accept: application/json
    content:
      # Permet de tout "dumper" les variables de l'application vers votre API
      json_content: |
          {{{Json .}}}
      check_response:
        throw_exception_if_body_not_contains_all:
            - success # À remplacer par un code de retour ou un mot retourné par votre api afin de valider que tout est concluant
```

Vous pouvez maintenant [déployer](deployer.md). 

Une fois le déploiement terminé, rendez-vous sur votre formulaire et lancez les [outils de développement](outils-developpement.md).

Il suffira alors de remplir quelques champs pour tester et cliquer sur `Tester transmission` pour voir apparaître les données que votre API aurait reçues si elle avait été réellement appelée.

Pour vous aider, il existe [un exemple complet d'un système simple](../Exemples/SystemeSimple/) qui démontre comment nommer les fichiers de base et leur contenu le plus courant.