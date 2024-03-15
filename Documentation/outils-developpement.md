# Outils de développement
Dans ce guide, nous expliquons comment utiliser les outils de développement intrégrés à FRW. Ces outils sont disponibles uniquement dans l'environnement IT. Ils permettent notamment de :
- Voir la liste des formulaires pour votre système et en tester un;
- Voir le modèle de données du formulaire en temps réel;
- Tester la transmission afin de voir les données qui auraient été transmises à votre API, les fichiers générés, ainsi que des messages liées à votre configuration de transmission;
- Configurer un contexte d'utilisation. 


&nbsp;

## Afficher la liste de tous les formulaires et essais de formulaires
La page de démarrage d'essais est disponible à l'url `https://formulaires.it.mtess.gouv.qc.ca/{id de votre système}?s={guid de votre système}`. Contactez le MESS afin d'obtenir cette information.

Dans cette interface vous trouverez :

1. Un bouton radio permettant de choisir le mode d'ouverture du formulaire;

1. La liste des formulaires de votre système (pour l'ouverture);

1. Un champ afin de saisir du JSON afin de simuler un pré-remplissage (non disponible si accès anonyme);

1. Une case à cocher vous permettant d'indiquer si vous désirez afficher la barre d'outils de développement;
   
1. Le bouton "Ouvrir" qui ouvrira le formulaire sélectionné.


![image](https://raw.githubusercontent.com/MTESSDev/FRW/main/Documentation/images/imgModeOuverture.png)

![image](https://raw.githubusercontent.com/MTESSDev/FRW/main/Documentation/images/imgChoixForm.png)

![image](https://raw.githubusercontent.com/MTESSDev/FRW/main/Documentation/images/imgJsonPreRemp.png)

![image](https://raw.githubusercontent.com/MTESSDev/FRW/main/Documentation/images/imgOutilDev2.png)

![image](https://raw.githubusercontent.com/MTESSDev/FRW/main/Documentation/images/imgBtnOuvrir.png)

&nbsp;

## Afficher la barre d'outils de développement

Il existe 2 façons d'afficher la barre d'outils de développement.

La première est via la case à cocher "Afficher les outils de développement" disponible dans la page de sélection d'un formulaire (voir point 4 de l'image à la section précédente)

La seconde est via le lien "Outils de développement" situé à droite dans le pied page (visible uniquement si les outils de développement ne sont pas déjà affichés) :

![image](https://user-images.githubusercontent.com/26974817/226039237-5595596a-8825-42cf-b0a6-34b2f36153e6.png)

&nbsp;

## Afficher la barre d'outils de développement (bac à sable)

En mode "bac à sable", la barre d'outils de développement ne contiendra que le contenu du modèle de données.

Pour afficher la barre d'outils, il faut ajouter `devTools=true` dans la ligne de commentaires `debug` du fichier de configuration d'un formulaire.
###Ici insérer image


&nbsp;

## Consulter le modèle de données du formulaire
Le modèle de données du formulaire est toujours disponible en temps réel dès que les outils de développement sont activés.

Il suffit d'ouvrir la section "Contenu du modèle de données" (1).

Il est également possible de copier le modèle de données dans le presse-papiers à l'aide du bouton (2) prévu à cet effet. Ce modèle de données peut ensuite être directement copié comme données de [pré-remplissage](pre-remplissage.md) d'un formulaire.

![image](https://user-images.githubusercontent.com/26974817/226624360-ddc94ad5-806b-4127-9c68-61b78996d312.png)


&nbsp;

## Tester la transmission du formulaire
Cette fonctionnalité est disponible en cliquant sur le bouton "Tester transmission" situé à l'intérieur de la zone "Outils de développement" qui est au bas de la page.

Non disponible dans le bac à sable.

![image](https://user-images.githubusercontent.com/26974817/226016145-376fccb1-0cdd-4d2e-83f0-60a2e6c00702.png)

Elle permet de voir :
1. Les fichiers pdf ou word qui auraient été générés (s'il y a lieu selon votre config);
2. Les informations qui auraient été transmises à votre API (sans les transmettre réellement) et autres messages en lien avec les tâches définies dans votre fichier de transmission.
 
Puisque les validations ne sont pas effectuées, il est possible de tester avec un formulaire partiellement rempli.


&nbsp;

## Définir un contexte d'utilisation

Documentation à venir... 

