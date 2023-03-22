# Créer votre premier fichier de transmission

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

Une fois le déploiement terminé, rendez-vous sur votre formulaire et lancez les [outils de développement](OutilsDeveloppement.md)

Il suffira alors de remplir quelques champs pour tester et cliquer sur `Tester transmission` pour voir apparaître les données que votre API aurait reçues si elle avait été réellement appelée.