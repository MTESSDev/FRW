# Connecter votre système à la solution FRW
Dans ce guide, nous expliquons comment intégrer notre solution de formulaires en ligne à votre système. 

Il existe deux types de formulaire : 
- Formulaire **authentifié** : permet une intégration complète avec votre système autorisé;
- Formulaire **anonyme** : permet d’utiliser FRW de façon indépendante; aucune intégration à votre système (outre la redirection initiale qui permet de créer le formulaire).

||Formulaire authentifié|Formulaire anonyme|
|--|--|--|
|Création du formulaire|Initiée par un appel de votre système à une API de FRW.|Effectuée par FRW suite à une redirection web à partir de votre système.|
|Association du formulaire à un identifiant utilisateur|Oui.|Non.|
|Reprise du formulaire|Via votre système (appel API FRW).|Via un courriel de reprise envoyé par FRW contenant un lien sécurisé par mot de passe.|
|Suppression du formulaire|Via votre système (appel API FRW).|Non supportée.|

## Formulaire authentifié
Cette section couvre la partie de connexion en amont des formulaires authentifiés, c'est-à-dire les étapes pour démarrer, reprendre, supprimer un formulaire ou encore lister les formulaires d'un utilisateur à partir de votre système.

### Créer un formulaire et y rediriger l'utilisateur

Pour déclencher la création d'un nouveau formulaire, il faut avoir une page de traitement dans votre système qui fait l'orchestration des étapes suivantes : 

1. [Préparer les données de pré remplissage](pre-remplissage.md) (facultatif);

1. Créer le formulaire en appelant l'API [CreerFormulaireIndividu](../Swagger/readme.md#apiv1siscreerformulaireindividutypeformulaire) (FRW111)
   
    C'est à cette étape que vous devez fournir les données de pré-remplissage le cas échéant;

1. Préparer l'URL de redirection à la page du formulaire

    L'URL prend la forme qui suit : `{Adresse du site FRW}/{langue}/reprise?no={No Public Session}`
    
    Ex. `https://formulaires.it.mtess.gouv.qc.ca/fr/Reprise?no=123456afaf3344`

    > **Attention** \
    > La session SYSTEME créé à l'étape 2. est valide seulement pour une durée de 30 secondes. La redirection doit être effectuée dans les 30 secondes qui suivent la création sinon la session devient invalide.

1. Rediriger l'utilisateur à cette url (idéalement dans un nouvel onglet du fureteur);

## Afficher la liste des formulaires d'un utilisateur

Pour obtenir la liste des formulaires d'un utilisateur afin de l'afficher dans une de vos pages, vous devez d'appeler l'API [ObtenirFormulairesIndividu](../Swagger/readme.md#apiv1sisobtenirformulairesindividu) (FRW112).
- Si vous offrez la possibilité de Reprendre ou Supprimer, vous devez filtrer sur les [états de formulaire](cycle-de-vie-etats.md) suivants afin de conserver seulement les formulaires qui sont pertinents à afficher pour l'utilisateur : `CRE`, `MAJ`, `COURRIEL`, `REP`, `REPAGENT`.
   - Dans toute autre état, la reprise et la suppression ne sont pas supportées.
- Pour filtrer, il suffit de passer la liste des états dans la propriété `etatsFormulaireRecherche` du paramètre d'entrée [entrantrechercherformulairessis](../Swagger/readme.md#entrantrechercherformulairessis) de FRW112.

## Reprendre un formulaire

Pour reprendre un formulaire, il faut connaitre son numéro de formulaire public en ayant préalablement appelé l'API [ObtenirFormulairesIndividu](../Swagger/readme.md#apiv1sisobtenirformulairesindividu) (FRW112) qui obtient la liste des formulaires d'un utilisateur.

Pour déclencher la reprise, il faut également avoir une page de traitement qui s'occupera des étapes à réaliser. 

Vous pouvez utiliser la même page que celle que vous aurez fait à l'étape « Créer un formulaire » en spécifiant un contexte de création ou de reprise.

Les étapes à effectuer sont les suivantes :

1. Obtenir un identifiant de session pour le formulaire en appelant l'API [ObtenirIdentifiantSessionFormulaire](../Swagger/readme.md#apiv1sisobteniridentifiantsessionformulairenoformulairepublic)
 (FRW113);

   
1. Préparer l'URL de redirection vers la page du formulaire;

   L'URL prend la forme qui suit : `{{ **Adresse du site FRW** }}/{{ **langue** }}/reprise?no={{ **No Public Session** }}`

    Ex. `https://formulaires.it.mtess.gouv.qc.ca/fr/Reprise?no=123456afaf3344`

   > **Attention** \
   > La session SYSTEME créé à l'étape 1. est valide seulement pour une durée de 30 secondes. La redirection doit être effectuée dans les 30 secondes qui suivent la création sinon la session devient invalide.

1. Rediriger l'utilisateur à cette url (idéalement dans un nouvel onglet du fureteur);


## Supprimer un formulaire

Il est possible de supprimer un formulaire à partir de son numéro de formulaire public. Il suffit d'appeler l'API [SupprimerFormulaire](../Swagger/readme.md#apiv1sissupprimerformulairenoformulairepublic) (FRW114).

## Formulaire anonyme
### Créer un formulaire
1. [Préparer les données de pré remplissage](pre-remplissage.md) encodées en base 64 (facultatif);
    1. Disponible à partir du milestone [2025.10](https://github.com/MTESSDev/FRW/milestones).

1. Préparer l'URL de redirection à la page du formulaire;
  
   L'URL prend la forme qui suit :
  
   `{Adresse du site FRW}/{langue}/Form/{No Systeme Autorisé}/{Type Formulaire}/0/N?donnees={Json de préremplissage en base 64}`

    Ex. `https://formulaires.it.mtess.gouv.qc.ca/fr/Form/1/3003/0/N?donnees=eyJmb3JtIjp7Im5vbUNoYW1wMSI6InZhbGV1ckNoYW1wMSJ9fQ==`

    > **Attention** \
    > Aucune donnée sensible ne doit être transmise dans le préremplissage anonyme. Celui-ci doit uniquement être utilisé à des fins d’orientation ou de guidage au sein du formulaire.
    > Le nombre de caractères maximum supporté est de 1000.

1. Rediriger l'utilisateur à cette url (idéalement dans un nouvel onglet du fureteur);
&nbsp;
