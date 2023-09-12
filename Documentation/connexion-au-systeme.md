# Connecter votre système à la solution FRW
Dans ce guide, nous expliquons comment intégrer notre solution de formulaires en ligne à votre système. Nous couvrons la partie de connexion en amont des formulaires, c'est-à-dire les étapes pour démarrer, reprendre, supprimer un formulaire ou encore lister les formulaires d'un utilisateur à partir de votre système.

&nbsp;
## Créer un formulaire et y rediriger l'utilisateur

Pour déclencher la création d'un nouveau formulaire, il faut avoir une page de traitement dans votre système qui fait l'orchestration des étapes suivantes :

1. [Préparer les données de pré remplissage](pre-remplissage.md) (facultatif);

1. Créer le formulaire en appelant l'API [CreerFormulaireIndividu](../Swagger/readme.md#apiv1siscreerformulaireindividutypeformulaire) (FRW111)
   
    C'est à cette étape que vous devez fournir les données de pré-remplissage le cas échéant;

1. Préparer l'URL de redirection à la page du formulaire

    L'URL prend la forme qui suit : `{{ **Adresse du site FRW** }}/{{ **langue** }}/reprise?no={{ **No Public Session** }}`
    
    Ex. `https://formulaires.it.mtess.gouv.qc.ca/fr/Reprise?no=123456afaf3344`

    Attention : la session SYSTEME créé à l'étape 2. est valide seulement pour une durée de 30 secondes. La redirection doit être effectuée dans les 30 secondes qui suivent la création sinon la session devient invalide.

1. Rediriger l'utilisateur à cette url (idéalement dans un nouvel onglet du fureteur);

&nbsp;

## Afficher la liste des formulaires d'un utilisateur

Pour obtenir la liste des formulaires d'un utilisateur afin de l'afficher dans une de vos pages, vous devez d'appeler l'API [ObtenirFormulairesIndividu](../Swagger/readme.md#apiv1sisobtenirformulairesindividu) (FRW112).
 

&nbsp;
## Reprendre un formulaire

Pour reprendre un formulaire, il faut connaitre son numéro de formulaire public en ayant préalablement appelé l'API [ObtenirFormulairesIndividu](../Swagger/readme.md#apiv1sisobtenirformulairesindividu) (FRW112)
 qui obtient la liste des formulaires d'un utilisateur.

Pour déclencher la reprise, il faut également avoir une page de traitement qui s'occupera des étapes à réaliser. 

Vous pouvez utiliser la même page que celle que vous aurez fait à l'étape « Créer un formulaire » en spécifiant un contexte de création ou de reprise.

Les étapes à effectuer sont les suivantes :

1. Obtenir un identifiant de session pour le formulaire en appelant l'API [ObtenirIdentifiantSessionFormulaire](../Swagger/readme.md#apiv1sisobteniridentifiantsessionformulairenoformulairepublic)
 (FRW113);

   
1. Préparer l'URL de redirection vers la page du formulaire;

   L'URL prend la forme qui suit : `{{ **Adresse du site FRW** }}/{{ **langue** }}/reprise?no={{ **No Public Session** }}`

    Ex. `https://formulaires.it.mtess.gouv.qc.ca/fr/Reprise?no=123456afaf3344`

    Attention : la session SYSTEME créé à l'étape 1. est valide seulement pour une durée de 30 secondes. La redirection doit être effectuée dans les 30 secondes qui suivent la création sinon la session devient invalide.

1. Rediriger l'utilisateur à cette url (idéalement dans un nouvel onglet du fureteur);

&nbsp;
## Supprimer un formulaire

Il est possible de supprimer un formulaire à partir de son numéro de formulaire public. Il suffit d'appeler l'API [SupprimerFormulaire](../Swagger/readme.md#apiv1sissupprimerformulairenoformulairepublic) (FRW114).


