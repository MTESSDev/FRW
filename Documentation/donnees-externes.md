# Données externes
Il est possible d'obtenir des données externes que vous pouvez exploiter dans votre formulaire.

Actuellement, les données externes peuvent être utilisées dans un domaine de valeurs pour une liste déroulante de votre formulaire;

Selon vos besoins, il serait possible de faire évoluer la solution afin de gérer d'autres cas d'utilisation:
- Indicateur (Ex: indicateur d'éligibilité vrai/faux);
- Objet qui peut être mappé dans des champs du formulaire.

## Guide d'utilisation
La majeure partie des configurations nécessaires pour l'obtention des données externes se situe dans la configuration "transmission". C'est dans ce fichier qu'il faudra définir les appels http pour obtenir les données externes.

Une fois cela fait, il suffit de définir la "source de données externes" sur le contrôle de votre choix dans la configuration "form" de votre formulaire.

Voir le détail complet dans les sections suivantes.

### Config transmission
Les sources de données externes sont définies dans la config transmission de votre formulaire ou de votre système autorisé.

En résumé les composantes à configurer sont les suivantes : 
- `http_client_set` - Ici vous déclarez les noms que vous voulez donner aux sources de données externes (par exemple "regions", "municipalites", etc...). Pour chaque source vous devez définir les éléments suivants : 
    - `sequence` - Permet de définir une séquence d'appel `http_client` :
        - Pour l'instant un seul élément est supporté, mais la base est là afin de supporter éventuellement plusieurs appels en séquence;
        - Par exemple si la source de données externes nécessite préalablement l'obtention d'un jeton d'authentification.
    - `data_adapter:template` - Ceci permet de formater les données dans le format de votre choix; dans notre exemple on transforme les données reçues en domaine de valeurs pour appliquer sur une liste déroulante du formulaire.
- `http_client` - Ici vous définissez chaque appel http_client présent dans la `sequence` définie précédemment.
    - Utiliser la syntaxe "input.donneesFormulaire.form.LeNomDeVotreChamp" si c'est un champ standard ou "input.donneesFormulaire.groupeCourant.LeNomDeVotreChamp" si le champ fait parti d'un groupe dans l'url d'obtention des données.

Voici un exemple complet de config transmission avec définition de sources de données externes (régions et municipalités de Données Québec).
- Les éléments "regionsGroupe" et "municipalitesGroupe" sont présents pour démontrer l'utilisation avec des contrôles qui sont dans des groupes (standards ou répétables) dans le formulaire.

```yml
#Le bloc "etapes" est affiché à titre d'exemple pour représenter un fichier de transmission.
etapes:
- tache: genererWord
  options:
    fichierBind: exempleBidon.bind.yml
- tache: extraireQuestions

http_client_set:
  regions:
    sequence:
      - http_client: donnees_qc_regions_api
        
    data_adapter:
      template: |
          {{> GenererDomaine items=donnees_qc_regions_api.body.result.records value="{{{NO_REG_ADM}}}" label_fr="{{{DESCR}}}"}}

  municipalites:
    sequence:
      - http_client: donnees_qc_municipalites_api
        
    data_adapter:
      # On réutilise exactement la MÊME partial GenererDomaine que pour les régions !
      # On ajuste simplement le nom des colonnes val et desc_fr
      # un label_en a été ajouté manuellement pour démontrer qu'il est possible de le gérer si la source de données est disponible dans les deux langues.
      template: |
          {{> GenererDomaine items=donnees_qc_municipalites_api.body.result.records value="{{{mcode}}}" label_fr="{{{munnom}}}" label_en="{{{munnom}}} (EN)"}}

  regionsGroupe:
    sequence:
      - http_client: donnees_qc_regions_groupe_api
        
    data_adapter:
      template: |
          {{> GenererDomaine items=donnees_qc_regions_groupe_api.body.result.records value="{{{NO_REG_ADM}}}" label_fr="{{{DESCR}}}"}}

  municipalitesGroupe:
    sequence:
      - http_client: donnees_qc_municipalites_groupe_api
        
    data_adapter:
      # On réutilise exactement la MÊME partial GenererDomaine que pour les régions !
      # On ajuste simplement le nom des colonnes val et desc_fr
      template: |
          {{> GenererDomaine items=donnees_qc_municipalites_groupe_api.body.result.records value="{{{mcode}}}" label_fr="{{{munnom}}}"}}

http_client:
  donnees_qc_regions_api:
      method: GET
      url: 'https://www.donneesquebec.ca/recherche/api/3/action/datastore_search?resource_id=8a69813f-eeb0-45b3-aab0-7541d573ae31&sort=DESCR&filters={"NO_REG_ADM":["01","02","03","04","05","06","07","08","09","10","11","12","13","14","15","16","17"]}&limit=32000'
      # chaos permet de simuler des erreurs
      chaos:
        enabled: false
        injection_rate_percentage: 100
        delay_milliseconds: 1500
        simulate_status_code: 500
        #On ne peut pas avoir simulate_status_code et simulate_network_exception en même temps
        #simulate_network_exception: true
      headers:
        Accept: 'application/json'
        Content-Type: 'application/json'

  donnees_qc_municipalites_api:
      method: GET
      url: 'https://www.donneesquebec.ca/recherche/api/3/action/datastore_search?resource_id=19385b4e-5503-4330-9e59-f998f5918363&filters={"mcodedesi":["01","02","04","05","06","09","10"]}&q={"regadm":"{{{input.donneesFormulaire.form.regionAdministrativeCallBackendFRW}}}"}&sort=munnom&limit=32000'
      headers:
        Accept: 'application/json'
        Content-Type: 'application/json'

  donnees_qc_regions_groupe_api:
      method: GET
      url: 'https://www.donneesquebec.ca/recherche/api/3/action/datastore_search?resource_id=8a69813f-eeb0-45b3-aab0-7541d573ae31&sort=DESCR&filters={"NO_REG_ADM":["01","02","03","04","05","06","07","08","09","10","11","12","13","14","15","16","17"]}&limit=32000'
      headers:
        Accept: 'application/json'
        Content-Type: 'application/json'

  donnees_qc_municipalites_groupe_api:
      method: GET
      url: 'https://www.donneesquebec.ca/recherche/api/3/action/datastore_search?resource_id=19385b4e-5503-4330-9e59-f998f5918363&filters={"mcodedesi":["01","02","04","05","06","09","10"]}&q={"regadm":"{{{input.donneesFormulaire.groupeCourant.regionAdministrativeGroupe}}}{{{input.donneesFormulaire.groupeCourant.regionAdministrativeGroupeRepet}}}"}&sort=munnom&limit=32000'
      headers:
        Accept: 'application/json'
        Content-Type: 'application/json'

  # Cet exemple sert pour l'utilisation avec une liste à choix multiple
  donnees_qc_municipalites_groupe_repet_api:
      method: POST
      url: https://www.donneesquebec.ca/recherche/api/3/action/datastore_search_sql
      content:
        json_content: |      
            {
              "sql": "SELECT * FROM \"19385b4e-5503-4330-9e59-f998f5918363\" WHERE mcodedesi IN ('01','02','04','05','06','09','10') AND ({{#each input.donneesFormulaire.groupeCourant.regionAdministrativeGroupeRepet2}}regadm LIKE '%{{this}}%'{{#unless @last}} OR {{/unless}}{{/each}}) ORDER BY munnom LIMIT 32000"
            }
      headers:
        Accept: 'application/json'
        Content-Type: 'application/json'

```

### Config form 
Vous devez ensuite appliquer la source de données externes sur votre liste déroulante dans la config form de votre formulaire.

[Voir le P700U Guide utilisateur FRW section "Domaines de valeurs externes"](https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=DomainesValeursExternes). 
