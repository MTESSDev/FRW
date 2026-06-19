# Configurer la transmission

Pour que l'outil FRW puisse gérer le contenu en sortie, il faut ajouter un fichier transmission. il sera nommé `default.v0.transmission.yml` s'il est au niveau de votre répertoire système, sinon, au niveau du formulaire, il sera nommé `NOM_DU_FORM.v0.transmission.yml` où le `NOM_DU_FORM` est identique à votre nom de répertoire du formulaire.


> **Les niveaux**\
> Certains blocs de config sont [définissables à plusieurs niveaux-fichiers-config](niveaux-fichiers-config.md), par contre le comportement de chaque bloc peut différer, voici un tableau détaillant ces comportements. 
>| Bloc config  | Niveau Global | Niveau Système | Niveau Formulaire  |   Détails |
>|---|---|---|---|---|
>| etapes  |   |  X  | X  | Si le bloc `etapes` est défini au niveau `Formulaire` il écrase complètement la configuration Système |   
>| http_client  |   | X  | X  | Les éléments `http_client` se cumulent  |


Un fichier `Transmission` est principalement nécessaire au niveau `Système` et dans certains cas précis au niveau d'un formulaire, comme par exemple pour remplacer les étapes par défaut que vous aviez défini.

Il existe deux grands types d'orchestration de transmission supportés par FRW :
- **Transmission standard** : La transmission classique déclenchée par l'utilisateur (citoyen) à la fin de la complétion de son formulaire web.
- **Transmission personnalisée** : Une transmission déclenchée de façon automatisée par votre système ou par un partenaire externe directement via l'appel d'une API, sans interaction de l'utilisateur dans l'interface web de FRW.

## Transmission standard

### Étapes
Lors de la transmission, le traitement FRW exécute les étapes dans l'ordre qu'elles ont été configurées dans le fichier de transmission. Nous vous recommandons donc d'utiliser le même ordre que nous utilisons dans notre exemple plus bas.

#### genererWord
Permet de produire un extrant contenant les données saisies dans le formulaire Web à partir d'un gabarit Word (docx).

Il vous est possible de vous créer un gabarit Word personnalisé ou d'utiliser celui offert par la solution FRW.

Référez-vous à la page [fichiers-bind](https://github.com/MTESSDev/FRW/blob/main/Documentation/fichiers-bind.md) pour plus de détails.

#### genererPDF
Permet de produire un extrant contenant les données saisies dans le formulaire Web à partir d'un gabarit PDF avec champs de saisie dynamiques.

Il vous est possible de vous créer un gabarit Word personnalisé ou d'utiliser celui offert par la solution FRW.

Référez-vous à la page [fichiers-bind](https://github.com/MTESSDev/FRW/blob/main/Documentation/fichiers-bind.md) pour plus de détails.

#### ajouterEstampille
Permet d'ajouter des informations par dessus l'extrant produit par les étapes `genererWord`ou `genererPDF` pour reproduire une estampille apposée manuellement. 

L'estampille est configurée dans le fichier `bind` associé au formulaire. Il est possible de définir les informations qu'on veut afficher ainsi que sa position dans la page.

Référez-vous à la page [fichiers-bind](https://github.com/MTESSDev/FRW/blob/main/Documentation/fichiers-bind.md) pour plus de détails.

#### signerPDF
Permet d'ajouter une signature numérique dans le PDF produit à l'étape 'genererPDF'. Cette signature permet de certifier que le PDF a été produit par FRW et elle peut contenir l'empreinte numérique provenant du contrôle de signature électronique du formulaire Web.

Cette tâche doit être positionnée APRÈS les tâches qui manipulent le PDF (ex: estampille), car on ne doit pas altérer le document une fois signé sous peine d'invalider la signature.

#### traiterDocumentsSoumis
Permet de traiter les pièces jointes que l'utilisateur a envoyé avec le formulaire. Le scan d'antivirus est effectué dans ce traitement.

Cette tâche est requise si votre formulaire permet de joindre des documents.

#### extraireQuestions
Permet d'ajouter toutes les questions du formulaire dans l'objet JSON fourni lors de la transmission. Les questions sont extraites dans les deux langues lorsqu'applicable.

#### envoyerCourriel (disponible à partir de la release [2024.2](https://github.com/MTESSDev/FRW/releases/tag/2024.2-IT))
Permet d'envoyer un courriel via le système FRW lors de la transmission du formulaire. Il faudra définir autant d'étapes "envoyerCourriel" qu'il y a de courriels différents à envoyer ainsi qu'un gabarit de courriel à utiliser pour chaque tâche.

Pour chaque gabarit courriel, il est possible :
- de spécifier une liste de destinataires, de copies conformes et de copies conformes invisibles et celles-ci peuvent être différentes entre chaque étape `envoyerCourriel`;
- d'ajouter l'extrant produit par les étapes `genererWord`ou `genererPDF` ainsi que les documents fournis par l'utilisateur en pièces jointe du courriel.
    - Il est possible de spécifier quelles pièces jointes on veut rendre disponible dans le courriel en appliquant des filtres. Se référer à l'exemple complet plus bas.
- d'utiliser des parties variables définies dans la tâche elle même.
- de spécifier si la version estampillée des pièces jointes doit être utilisée.

#### conserverFichier (disponible à partir de la release 2024.3)
Permet d'indiquer au système de conserver une copie du fichier produit par l'orchestration dans un répertoire interne pour être récupéré par un autre traitement.

#### appelerServiceExterne
Permet de spécifier l'API externe à appeler lors de la transmission.

Il est possible de définir le comportement attendu avec l'utilisation du bouton `Tester transmission` offert dans les outils de développement afin de simuler une transmission.

Cette tâche est directement liée à la section `http_client`.

#### http_client
Cette section permet de spécifier toutes les caractéristiques de l'appel à l'API défini dans l'étape `appelerServiceExterne`.

#### expirerFormulaire (Disponible pour les formulaires en workflow seulement)
Permet d'ajouter un délai d'expiration programmé pour le formulaire. Lorsque le délai est atteint, le formulaire sera automatiquement expiré s'il n'a pas été transmis, ce qui fait qu'il ne sera plus possible pour les participants de le compléter.
Se référer à l'exemple du fichier de transmission en [workflow](workflows.md#config-transmission).

### Exemple de toutes les possibilitées de configuration (transmission standard)
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

    # Ajouter estampille, permet d'ajouter une "Étampe" sur un document 
    # comme pour l'officialiser (mettre la date de transmission, 
    # le no. de confirmation, etc)
    - tache: ajouterEstampille

    # Permet d'ajouter une signature numérique sur le document afin de certifier son authenticité.
    - tache: signerPDF

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
          partie3: '{{donneesFormulaire.form.testCourriel}}'
        # Indique si la version estampillée des pièces jointes doit être utilisée. Valeur par défaut : true.
        afficherEstampille: true

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

    # [Worflows seulement] Permet de faire expirer un formulaire après le délai désiré
    - tache: expirerFormulaire
      options:
          gabarit: formExpire # Optionel : doit être défini sous gabaritsCourriels de la présente config, si non défini, aucun courriel n'est envoyé automatiquement
          delaiExpirationHeures: 48 
          langue: fr
          # Permet de définir des conditions pour exécuter le traitement dans certains cas seulement
          conditionsEt:
            - condition: '=='
              champFormulaire: 'donneesFormulaire.form.sexe'
              valeur: 'Masculin' 

# Liste des gabarits de courriel pour la tâche "envoyerCourriel"
gabaritsCourriels:
  - id: confirmation
    # Liste des destinataires (peut être une liste)
    a:
      tous: 
        - 'esun-a02@essais.mess.gouv.qc.ca'
    # Liste des copies conformes (Facultatif, peut être une liste)
    # Dans cet exemple, une des adresse réfère à un champ du formulaire nommé "testCourriel"
    cc:
      tous:
        - 'esun-a05@essais.mess.gouv.qc.ca'
        - '{{donneesFormulaire.form.testCourriel}}'
    # Liste des copies conformes invisibles (Facultatif, peut être une liste)
    # Dans cet exemple, une des adresse réfère à la partie variable "partie3" définie dans le module "envoyerCourriel"
    cci:
      tous:
        - 'esun-a04@essais.mess.gouv.qc.ca'
        - '{{envoyerCourriel.partiesVariables.partie3}}'
    # Nom de l'expéditeur (Par défaut, "Formulaires en ligne" ou "Online forms" selon la langue)
    nomExpediteur: Test FRW Transmission
    # Permet de spécifier l'adresse de retour
    retourA: '{{envoyerCourriel.partiesVariables.partie3}}'
    # L'objet du courriel peut contenir des parties variables
    objet: '{{envoyerCourriel.partiesVariables.partie1}} demande {{envoyerCourriel.partiesVariables.partie2}}'
    # Les données du formulaires peuvent être réutilisées dans le contenu du courriel.
    # Les données retournées par Moneris lors d'un paiement sont également accessibles.
    corps: |
      <p>ceci est un test</p>
      <p>Exemple1a : {{donneesFormulaire.form.Exemple1a.0}}, Exemple1b : {{donneesFormulaire.form.Exemple1b.0}}</p>
        # Pour faire afficher les documents téléchargeables, il faut ajouter le tableau ci-dessous. Une liste contenant chaque document avec son nom original dans FRW sera ajoutée au contenu du courriel. Sur le clique du lien, le document sera téléchargé.
        <ul>
          {{#listePJ}}
        <li><a href="{{url}}">{{nomOriginal}}</a></li>
          {{/listePJ}}
        </ul>
        # Si vous avez utilisé la fonctionnalité de paiement avec FRW et que vous désirez afficher un reçu, il faut copier tout le bloc '{{#with donneesFormulaire.form.paiement}}'
        # Vous pourrez modifier les textes à votre guise. 
        {{#with donneesFormulaire.form.paiement}}
        <div style="font-family: Arial, sans-serif; color: #333; max-width: 500px; border: 1px solid #e0e0e0; padding: 20px; border-radius: 5px;">
        <h2 style="color: #2c3e50; margin-top: 0;">Reçu de transaction</h2>
        <div style="background-color: #f9f9f9; padding: 15px; margin-bottom: 20px;">
        <p style="margin: 5px 0;"><strong>Statut :</strong> {{receipt.Message}}</p>
        <p style="margin: 5px 0;"><strong>Date :</strong> {{receipt.TransDate}} à {{receipt.TransTime}}</p>
        </div>
        
            <table width="100%" cellpadding="5" cellspacing="0" style="border-collapse: collapse;">
        <tr>
        <td style="border-bottom: 1px solid #eee; color: #777;">Sous-total :</td>
        <td style="border-bottom: 1px solid #eee; text-align: right; color: #777;">{{commande.cart.subtotal}} $</td>
        </tr>
        <tr>
        <td style="border-bottom: 1px solid #eee; color: #777;">Taxes :</td>
        <td style="border-bottom: 1px solid #eee; text-align: right; color: #777;">{{commande.cart.tax.amount}} $</td>
        </tr>
        <tr>
        <td style="border-bottom: 1px solid #eee; padding-top: 10px;"><strong>Montant total :</strong></td>
        <td style="border-bottom: 1px solid #eee; text-align: right; font-size: 1.2em; padding-top: 10px;"><strong>{{receipt.TransAmount}} $</strong></td>
        </tr>
        <tr>
        <td style="border-bottom: 1px solid #eee;">Type de carte :</td>
        <td style="border-bottom: 1px solid #eee; text-align: right;">{{receipt.CardType}}</td>
        </tr>
        <tr>
        <td style="border-bottom: 1px solid #eee;"># Autorisation :</td>
        <td style="border-bottom: 1px solid #eee; text-align: right;">{{receipt.AuthCode}}</td>
        </tr>
        <tr>
        <td># Référence :</td>
        <td style="text-align: right;">{{receipt.ReferenceNum}}</td>
        </tr>
        </table>
        <div style="margin-top: 20px; font-size: 0.8em; color: #777; text-align: center;">
                Merci de votre confiance.
        </div>
        </div>
        {{/with}}

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

### Variables et contenu

Variables du bloc `http_client` utilisables dans le style `mustache`. Tout le bloc `http_client` est basé sur l'outil [YamlHttpClient](https://github.com/anisite/YamlHttpClient), vous pouvez vous y référer pour bâtir votre `json_content`.

| Variable | Type/Valeur | Description |
| ---      |----         | ---         |
| langue | `fr`, `en`    | Langue d'affichage du formulaire |
| noFormulaire | numérique   | Numéro unique séquentiel du formulaire |
| typeFormulaire   `Disponible à partir de la version 2024.3` |string   | Type du formulaire, c'est le code du formulaire soumis ``ex: FORM1234`` |
| noConfirmation | numérique  | Numéro unique de confirmation, peut-être validé par un agent, termine par ``311``. <br> En mode simulé (en utilisant le bouton "Tester transmission"), le numéro de confirmation sera forcé à '9999999999311'|
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

## Transmission personnalisée

> Disponible à partir de la release [2026.7](https://github.com/MTESSDev/FRW/releases)

La transmission personnalisée permet à un système autorisé ou à un partenaire externe de déclencher l'exécution de tâches de transmission (comme par exemple la production directe d'un PDF), et ce, sans aucune interaction utilisateur via l'interface WEB.

**Caractéristiques importantes :**
- Déclenche la production d'une transmission à la fois.
- Ne valide ni la structure JSON, ni le format des champs lors de la génération. Le document final (ex: PDF) pourrait être incomplet ou contenir des erreurs de format si les données fournies par l'appelant sont incomplètes ou invalides.
- Il est impossible d'exécuter la même transmission personnalisée (le même identifiant) plus d'une fois pour un même formulaire. Il est toutefois possible d'en exécuter des différentes.
- Le coût de production est équivalent à celui d'une transmission normale.
- Exclut les processus gérés par le workflow (comme la signature électronique) ainsi que les pièces jointes annexées au PDF. 

### Configurer une transmission personnalisée

La transmission personnalisée doit être définie dans la configuration de transmission (fichier `transmission.yml` au niveau Système ou Formulaire) sous le bloc de configuration `transmissionsPerso`. 

Vous pouvez y lister les étapes à exécuter pour l'identifiant concerné :

```yaml
transmissionsPerso:
  - id: envoi-partenaire # Identifiant unique de la transmission personnalisée
    etapes:
      - tache: genererPdf
        langue: fr
      - tache: ajouterEstampille
      - tache: envoyerCourriel
        options:
          gabarit: monBeauCourriel
```
### Tâches non supportées
Toutes les tâches d'une [transmission standard](#transmission-standard) sont supportées à l'exception de celles listées ci-dessous, qui nécessitent une interaction avec l'utilisateur ou que la transmission soit de type "Workflow" : 
- traiterDocumentsSoumis
- signerPDF 
- expirerFormulaire

### Déclencher une transmission personnalisée (via API)

Pour lancer une transmission personnalisée, l'appelant (système autorisé ou partenaire externe) doit orchestrer deux appels API successifs : la création du formulaire, puis le déclenchement de la transmission.

#### 1. Créer le formulaire

Le formulaire ciblé doit d'abord être instancié dans FRW.

Vous devez appeler l'API de création de formulaire (`CreerFormulaireIndividu` - FRW111) avec les éléments suivants :

- **Authentification :**
  - *Système autorisé :* Fournir le numéro public de votre système autorisé ainsi que la clé d'API.
  - *Partenaire externe :* Fournir la clé de partenaire externe dans l'en-tête HTTP `X-ClePartenaire`.
- **Données de pré-remplissage :** Injecter un objet de pré-remplissage JSON contenant toutes les données nécessaires (ex: pour remplir le PDF lors de sa génération).
  > **Attention :** Pour que la tâche `genererPdf` produise un rendu valide, il faut qu'au moins un champ soit pré-rempli avec une valeur valide.

**Exemple de payload JSON (FRW111) :**
```json
{
  "typeFormulaire": "VOTRE_FORMULAIRE",
  "donneesFormulaire": {
    "form": {
      "nomLocataire": "Tremblay",
      "prenomLocataire": "Jean",
      "adresse": "123 rue des Lilas"
    }
  }
}
```

L'API vous retournera en réponse un **numéro public de formulaire** (ShortGuid). Conservez-le pour l'étape suivante.

#### 2. Déclencher la transmission

Une fois le formulaire créé, vous pouvez déclencher l'exécution des tâches en appelant l'API de transmission personnalisée (`DeclencherTransmissionPersonnalisee` - FRW122).

Les paramètres requis pour cet appel sont les suivants :

- **Authentification :** Utiliser la même méthode d'authentification que lors de la création (clé de partenaire externe ou informations du système autorisé).
- **NoPublicFormulaire :** Le numéro public (ShortGuid) obtenu à la première étape.
- **IdTransmissionPerso :** L'identifiant de la transmission configurée dans votre fichier `transmission.yml` (ex: `envoi-partenaire`). *Cet identifiant n'est pas sensible à la casse.*
- **Identifiant Utilisateur :** (Optionnel) Identifiant de suivi fourni dans l'en-tête `X-IdentifiantUtilisateur`.

**Traitement effectué par FRW :**
Le système valide l'authentification et vérifie que cet identifiant de transmission (`IdTransmissionPerso`) n'a pas déjà été complété pour ce formulaire. Si les conditions sont remplies, un numéro de confirmation est généré (s'il n'existe pas déjà) et les étapes sont exécutées. Ce formulaire sera ensuite considéré comme transmis et facturable. 

#### 3. Récupérer les résultats

En réponse à l'appel de la transmission personnalisée, l'API retourne un payload contenant :
- **documents :** La liste des documents produits (ex: le PDF généré), chaque document incluant un `nom`, un flux `fichier` (encodé en base64) et le type source du document (ex: `genererPdf`).
- **messages :** Une liste de messages retournés par l'orchestration des tâches (avec leur `mnemonique` et texte du `message`).
- Le contenu du retour peut varier en fonction des tâches que vous avez configurées.
