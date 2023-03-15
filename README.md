# FRW - Formulaires Web

## Qu'est-ce que c'est?
Un outil incroyable qui permet de créer des formulaires très rapidement à l'aide de simples fichiers de configuration YAML (low code).

Les formulaires générés sont accessibles, adaptatifs (responsive), sécuritaires et respectent les règles du [système de design Québec.ca](https://design.quebec.ca/).


&nbsp;
## Comment l'utiliser?
### Pré-requis

1. Cloner le dépôt courant et copiez le répertoire "Exemple" pour le nommer à votre goût, il regroupera tous vos formulaires (Ne faire cette étape qu'une seule fois);

1. Configurer votre [bac à sable](https://formulaires.it.mtess.gouv.qc.ca/Form/1/P700U/0/N/#p=2);

&nbsp;
### Créer un formulaire
  
1. Utiliser le bac à sable afin de définir la configuration de vos formulaires. Consulter le [guide de configuration de formulaires FRW](https://formulaires.it.mtess.gouv.qc.ca/Form/1/P700U/0/N); 

&nbsp;
### Déployer un formulaire

1. Se procurer une clée API et un code de système autorisé auprès du MESS (Documentation à venir...);
   
1. Déployez un formulaire avec DevOps ou autre (Documentation à venir...)
 
&nbsp;
### Définir un ou plusieurs fichiers PDF en sortie pour un formulaire (optionnel)
1. Configurer le fichier de transmission du formulaire; (Documentation à venir...) 
1. Créer un gabarit PDF 
1. Configurer le fichier "bind" du formulaire
1. À venir...

&nbsp;
### Définir un fichier Word en sortie pour un formulaire (optionnel)
1. Configurer le fichier de transmission du formulaire; (Documentation à venir...) 
1. Créer un gabarit Word 
1. À Venir...

&nbsp;
### Recevoir les données du formulaire transmises à votre système
1. Configurer le fichier de transmission du formulaire; (Documentation à venir...) 
1. Dans votre système, créer un api permettant de recevoir les données. (Documentation à venir...) 

&nbsp;
### Utiliser les services FRW à partir de votre système

1. [Créer une instance du formulaire et y rediriger l'utilisateur](Documentation/ConnexionAuSysteme.md#cr%C3%A9er-un-formulaire-et-y-rediriger-lutilisateur);
1. [Afficher la liste des formulaires d'un utilisateur](Documentation/ConnexionAuSysteme.md#afficher-la-liste-des-formulaires-dun-utilisateur) ;
1. [Reprendre un formulaire](Documentation/ConnexionAuSysteme.md#reprendre-un-formulaire);
1. [Supprimer un formulaire](Documentation/ConnexionAuSysteme.md#supprimer-un-formulaire);

&nbsp;
## Vous avez une question ou une suggestion?

1. Vérifier si une discussion existe avec le même questionnement/suggestion;
1. Créez une discussion si vous n'avez toujours pas de réponse à votre question ou si votre suggestion n'existe pas déjà;
1. N'hésitez pas à aider d'autres utilisateurs ou à partager vos idées;

&nbsp;
## Vous avez trouvé un probème (bug) dans la solution?

1. Vérifier si une "issue" existe avec le même problème;
1. Créez une "issue" s'il n'est existe pas déjà une et mettre le plus de détails possibles afin de reproduire le problème;
