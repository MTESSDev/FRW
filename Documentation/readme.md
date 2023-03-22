# Guide d'intégration de la solution de formulaires en ligne FRW

## Introduction

Dans ce guide, nous expliquons comment intégrer notre solution de formulaires en ligne à votre système. Nous couvrirons la partie de connexion en amont des formulaires, c'est-à-dire les étapes pour démarrer ou reprendre un formulaire à partir de votre système. De plus, nous expliquerons les fonctionnalités offertes lorsque l'utilisateur transmet son formulaire.

## Connecter votre système à la solution FRW

### Avant de débuter

- Consulter la section d'arrimage à FRW dans le guide utilisateur;

1. [https://master-www.extra-frw.sa.mes.reseau.intra/Form/1/P700U/0/N/#p=1](https://master-www.extra-frw.sa.mes.reseau.intra/Form/1/P700U/0/N/#p=1)

### Afficher la liste des formulaires d'un utilisateur

- Pour afficher une liste des formulaires d'un utilisateur dans une de vos pages, celle-ci doit appeler l'API ObtenirFormulairesIndividu (FRW112)

1. [https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1sisobtenirformulairesindividu](https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1sisobtenirformulairesindividu)

- Il est possible de supprimer un formulaire en appelant l'API SupprimerFormulaire (FRW114)

1. [https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1sissupprimerformulairenoformulairepublic](https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1sissupprimerformulairenoformulairepublic)

### Créer un formulaire

- Pour déclencher la création d'un nouveau formulaire, il faut avoir une page de traitement dans votre système qui fera l'orchestration des étapes suivantes :

1. Préparer les données de pré remplissage (facultatif);

1. Si vous voulez fournir des données pour pré remplir des champs du formulaire comme le nom ou l'adresse, vous devez avoir un service dans votre système qui fait cette opération. Se référer à l'annexe « Service de pré remplissage »;

1. Créer le formulaire en appelant l'API CreerFormulaireIndividu (FRW111);

1. [https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1siscreerformulaireindividutypeformulaire](https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1siscreerformulaireindividutypeformulaire)

1. C'est dans cet appel que vous devez envoyer les données de pré remplissage lorsqu'applicable.

1. Préparer l'URL de redirection vers la page du formulaire;

1. L'URL prend la forme qui suit : {{ **Adresse du site FRW** }}/{{ **langue** }}/ ?utm\_source={{ **votre système** }}&no={{ **No Public Session** }}

1. Rediriger vers l'URL du formulaire;

### Reprendre un formulaire

- Pour reprendre un formulaire, il faut connaitre son numéro de formulaire public en ayant préalablement appelé l'API qui obtient la liste des formulaires d'un utilisateur (FRW112)
- Pour déclencher la reprise, il faut également avoir une page de traitement qui s'occupera des étapes à réaliser.

1. Vous pouvez utiliser la même page que celle que vous aurez fait à l'étape « Créer un formulaire » en spécifiant un contexte de création ou de reprise.

- Les étapes à effectuer sont les suivantes :

1. Obtenir un identifiant de session pour le formulaire en appelant l'API ObtenirIdentifiantSessionFormulaire;

1. [https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1sisobteniridentifiantsessionformulairenoformulairepublic](https://github.com/MTESSDev/FRW/tree/main../Swagger#apiv1sisobteniridentifiantsessionformulairenoformulairepublic)

1. Préparer l'URL de redirection vers la page du formulaire;

1. L'URL prend la forme qui suit : {{ **Adresse du site FRW** }}/{{ **langue** }}/ ?utm\_source={{ **votre système** }}&no={{ **No Public Session** }}

1. Rediriger vers l'URL du formulaire;

## Configuration du formulaire

La solution FRW repose sur l'utilisateur de trois fichiers de configuration :

1. Form : Contient tous les champs et sections du formulaire ainsi que les domaines de valeur et les conditions d'affichage;

- Se référer aux documentations suivantes pour connaitre les différents outils d'aide à la configuration des formulaires :

- P700U – Guide utilisateur : [https://master-www.extra-frw.sa.mes.reseau.intra/Form/1/P700U/0/N/#p=0](https://master-www.extra-frw.sa.mes.reseau.intra/Form/1/P700U/0/N/#p=0)

- Documentation du bac à sable : [https://github.com/MTESSDev/vscode-mtess-frw-bacasable](https://github.com/MTESSDev/vscode-mtess-frw-bacasable)

1. Bind : Permet de faire l'association entre les champs du formulaire WEB et ceux de l'extrant à produire;

1. Transmission : Permet de définir les étapes à exécuter lors de la transmission du formulaire;

## Gérer la transmission des données du formulaire

La solution FRW n'offre pas d'API permettant de consulter les données d'un formulaire à tout moment. Cependant, plusieurs fonctionnalités sont offertes lorsqu'un utilisateur transmet son formulaire. La présente section vise à démontrer les différentes possibilités.

Fichier Bind

Fichier Transmission





## ANNEXE

### Service de pré remplissage

### Exemple de fichier Bind

#### À partir d'un gabarit PDF avec champ de saisie dynamique

#### À partir d'un gabarit Word