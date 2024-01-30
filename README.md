[![Build](https://github.com/MTESSDev/FRW/actions/workflows/build.yml/badge.svg)](https://github.com/MTESSDev/FRW/actions/workflows/build.yml)

# FRW - Formulaires Web

## Qu'est-ce que c'est?
Un outil incroyable qui permet de créer des formulaires très rapidement à l'aide de simples fichiers de configuration YAML (low code). [Consulter les technologies utilisées](Documentation/technologies-utilisees.md).

Les formulaires générés sont accessibles, adaptatifs (responsive), sécuritaires et respectent les règles du [système de design Québec.ca](https://design.quebec.ca/).

Nous vous invitons à consulter la [présentation complète](https://github.com/MTESSDev/FRW/blob/main/Documentation/Documents/FRW%20-%20Pr%C3%A9sentation%20compl%C3%A8te.pptx) du système. Il est important de la télécharger et de l'ouvrir dans PowerPoint directement, car sinon, dans le navigateur, les gifs ne sont pas animés.

[![Image](https://user-images.githubusercontent.com/129791924/251484311-8dcc5dd2-ee22-4f6e-9df0-2ae0b0293df6.png)](Documentation/Documents/FRW%20-%20Pr%C3%A9sentation%20compl%C3%A8te.pptx)

[Consulter la liste des fonctionnalités offertes par FRW](Documentation/fonctionnalites.md).

&nbsp;

## Comment l'utiliser?

[Consulter la présentation "fonctionnelle" d'arrimage à un système](Documentation/Documents/FRW_Arrimage%20d'un%20système%20autorisé.pdf)


### Pré-requis

1. Clôner le dépôt courant et copiez le répertoire "Exemple" pour le nommer à votre goût, il regroupera tous vos formulaires (Ne faire cette étape qu'une seule fois);
2. Installer [VS Code](https://code.visualstudio.com/);

3. [Configurer votre bac à sable](https://github.com/MTESSDev/vscode-mtess-frw-bacasable) (Contactez le MESS afin d'obtenir l'url à utiliser lors de la configuration);

&nbsp;
### Créer un formulaire
    
Utiliser le bac à sable afin de définir la configuration de vos formulaires. Consulter le [guide de configuration de formulaires FRW](https://formulaires.it.mtess.gouv.qc.ca/Form/7/P700U/0/N); 


Pour un premier formulaire, il est fortement recommandé de clôner le présent dépot GitHub (tel que mentionné en [pré-requis](#pré-requis)), afin de comprendre la structure requise et diposer d'une base de travail.

&nbsp;
### Déployer un formulaire

1. Se procurer une clé API et un code de système autorisé auprès du MESS (Contacter le MESS);
1. [Déployer un formulaire avec DevOps](Documentation/deployer.md);
 
&nbsp;
### Définir le ou les fichiers à produire à partir des données du formulaire (optionnel)
1. [Configurer le fichier de transmission](Documentation/fichiers-transmission.md) du formulaire; 
1. [Créer un gabarit](Documentation/gabarits.md) (PDF ou Word);
1. [Configurer le fichier "bind"](Documentation/fichiers-bind.md) du formulaire;

&nbsp;

### Déployer vos fichiers
- [Déployer vos fichiers avec Azure DevOps](https://marketplace.visualstudio.com/items?itemName=MTESS.mtess-frw-deploiement);

&nbsp;
### Tester vos formulaires
- [Utiliser les outils de développement](Documentation/outils-developpement.md) afin de tester vos formulaires;

&nbsp;
### Recevoir les données du formulaire transmises à votre système
1. [Configurer le fichier de transmission](Documentation/fichiers-transmission.md) du formulaire; 
1. Dans votre système, créer un api permettant de recevoir les données (exemple à venir). 

&nbsp;
### Utiliser les services FRW à partir de votre système

1. [Créer une instance du formulaire et y rediriger l'utilisateur](Documentation/connexion-au-systeme.md#cr%C3%A9er-un-formulaire-et-y-rediriger-lutilisateur);
1. [Afficher la liste des formulaires d'un utilisateur](Documentation/connexion-au-systeme.md#afficher-la-liste-des-formulaires-dun-utilisateur) ;
1. [Reprendre un formulaire](Documentation/connexion-au-systeme.md#reprendre-un-formulaire);
1. [Supprimer un formulaire](Documentation/connexion-au-systeme.md#supprimer-un-formulaire);

&nbsp;
## Vous avez une question ou une suggestion?

1. Vérifier si une [discussion](https://github.com/MTESSDev/FRW/discussions) existe avec le même questionnement/suggestion;
1. Créez une [discussion](https://github.com/MTESSDev/FRW/discussions) si vous n'avez toujours pas de réponse à votre question ou si votre suggestion n'existe pas déjà;
1. N'hésitez pas à aider d'autres utilisateurs ou à partager vos idées.

&nbsp;
## Vous avez trouvé un problème (bug) dans la solution?

1. Vérifier si une [issue](https://github.com/MTESSDev/FRW/issues) existe avec le même problème;
2. Créez une [issue](https://github.com/MTESSDev/FRW/issues) si elle n'existe pas déjà une et mettre le plus de détails possibles afin de reproduire le problème.


&nbsp;
## Vous désirez être informé des changements en cours et à venir?

[Consultez les milestones](https://github.com/MTESSDev/FRW/milestones), ils vous donnent l'information sur les travaux en cours et à venir, ainsi que la date prévue de livraison.


[Configurez vos notifications](Documentation/configurer-notifications.md) afin d'être avisé lors de la publication d'une nouvelle release.

Une release est publiée lorsqu'une nouvelle version est déployée dans l'environnement d'essais (normalement quelques semaines avant la production, et une date de MEP prévue est indiquée), ainsi que lors d'une mise en production.
