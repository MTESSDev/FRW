# Outils de développement
Dans ce guide, nous expliquons comment utiliser les outils de développement intrégrés à FRW. Ces outils sont disponibles uniquement dans l'environnement IT. Ils permettent notamment de :
- Voir la liste des formulaires pour votre système et sélectionner celui à tester;
- Voir le modèle de données du formulaire en temps réel;
- Tester la transmission afin de voir les données qui auraient été transmises à votre API, ainsi que les pdf qui auraient été générés;
- Configurer un contexte d'utilisation. 


&nbsp;

## Afficher la liste de tous les formulaires de votre système aux fins d'essais
Accéder à l'url https://formulaires.it.mtess.gouv.qc.ca/{id de votre système}?s={guid de votre système}. Contactez le MESS afin d'obtenir cette information.

Dans cette interface vous avez :

1. La liste des formulaires de votre système;

1. Un champ afin de saisir du JSON afin de simuler un pré-remplissage;

1. Une case à cocher vous permettant d'indiquer si vous désirez afficher la barre d'outils de développement;
   
1. Le bouton "Ouvrir" qui ouvrira le formulaire sélectionné.

###Insérer l'image ici###

&nbsp;

## Afficher la barre d'outils de développement

Il existe 2 façons d'afficher la barre d'outils de développement.

La première est via la case à cocher "Afficher les outils de développement" disponible dans la page de sélection d'un formulaire :

###Insérer l'image ici###


La seconde est via le lien "Outils de développement" situé à droite dans le pied page (visible uniquement si les outils de développement ne sont pas déjà activés) :

###Insérer l'image ici###

&nbsp;

## Consulter le modèle de données du formulaire
Le modèle de données du formulaire est toujours disponible en temps réel dès que les outils de développement sont activés.

Il suffit d'ouvrir la section "Contenu du modèle de données".

###Insérer l'image ici###


&nbsp;

## Tester la transmission du formulaire
Cette fonctionnalité est disponible en cliquant sur le bouton "Tester transmisssion" situé à l'intérieur de la zone "Outils de développement".

###Insérer l'image ici###

Elle permet de voir :
- Les fichiers pdf ou word qui auraient été générés (s'il y a lieu selon votre config);
- Les informations qui auraient été transmises à votre API (sans les transmettre réellement).
 
Puisque les validations ne sont pas effectuées, il est possible de tester avec un formulaire partiellement rempli.


&nbsp;

## Définir un contexte d'utilisation

Documentation à venir... 

