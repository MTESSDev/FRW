# Configurer le fichier produit à partir des données du formulaire (fichier bind)

L'outil FRW permet de générer un fichier à partir des données du formulaire transmis. Le fichier de configuration "bind" est requis afin de configurer le format et les caractéristiques de l'extrant à produire.

## Tester vos formulaires
À tout moment, vous pouvez utiliser les [outils de développement](outils-developpement.md) afin de tester vos formulaires;

Référez vous à la section [Tester la transmission du formulaire](outils-developpement.md#tester-la-transmission-du-formulaire) pour prévisualiser le fichier produit à partir de la page Web du formulaire.

## Créer votre premier fichier bind avec le gabarit Word générique
Pour débuter et tester un premier coup votre fichier bind, vous devez créer le fichier dans le même répertoire que votre formulaire en cours. Il doit être nommé `NOM_DU_FORM.v0.bind.yml` où le `NOM_DU_FORM` est identique à votre nom de répertoire du formulaire.

Lorsque le fichier existe dans le répertoire du formulaire, vous pouvez essayer l'exemple suivant :

### Exemple de configuration de base (gabarit Word)
Détails:
1. Le fichier produit par FRW sera un PDF;
1. Le traitement utilisera le gabarit Word générique offert par la solution FRW;
    * Vous n'avez pas à fournir de gabarit Word.
1. Aucune estampille ne s'affichera sur le fichier produit;
1. Tous les champs du formulaire Web s'afficheront dans le fichier produit;

````yaml
bundles:
#Le nomSortie sert à définir le nom du fichier qui sera produit. 
#Lorsqu'on utilise un gabarit Word pour la production du fichier, on doit spécifier l'extension désirée du document.
#Dans ce cas-ci, le fichier produit par FRW sera un fichier PDF. La solution supporte les PDF et les DOCX.
  - nomSortie: test.pdf
#Le template permet de référer à la section template plus bas dans le fichier.
    templates:
      - template1
#La section templates sert à définir les caractéristiques du gabarit utilisé.
#Lorsqu'on utilise le gabarit Word générique de FRW pour la production du fichier, cette section ne sert qu'à lister les champs à exclure.
templates:
- id: template1
#Le name n'est pas utilisé dans le traitement. Vous pouvez mettre n'importe quoi.
  name: Fichier word
````

## Créer un fichier bind avec votre gabarit Word
Si vous voulez avoir une mise en page spécifique pour afficher les données de votre formulaire, vous pouvez vous construire un gabarit Word. 

Pour que FRW l'utilise, vous devez créer un répertoire "Gabarits" dans le même répertoire que votre formulaire en cours et y déposer votre gabarit.

Vous pouvez ensuite modifier le fichier bind que vous avez créé précédemment en utilisant l'exemple suivant:

### Exemple de configuration avec un gabarit Word spécifique
En plus d'utiliser un gabarit Word spécifique, cet exemple vous montrera quelques fonctionnalités supplémentaires de FRW.

Détails:
1. Le fichier produit sera un DOCX;
1. Le traitement utilisera le gabarit Word spécifique que vous aurez déposé dans le répertoire "Gabarits".
1. Une estampille s'affichera sur le fichier produit;
1. Certain champs du formulaire Web ne seront pas affichés dans le fichier produit;

````yaml
bundles:
#Le nomSortie sert à définir le nom du fichier qui sera produit. 
#Lorsqu'on utilise un gabarit Word pour la production du fichier, on doit spécifier l'extension désirée du document.
#Dans ce cas-ci, le fichier produit par FRW sera un fichier PDF. La solution supporte les PDF et les DOCX.
  - nomSortie: test.docx
    templates:
      - template1
#Une estampille est un texte qu'on affiche sur le document produit pour donner plus d'informations. Cette section est facultative.
    estampille:
#positionX et positionY sont les coordonnées de l'emplacement de l'estampille dans la page.
      positionX: 400
      positionY: 710
#tailleFont permet de spécifier la grosseur de police dans le fichier
      tailleFont: 9
#lignes permet de spécifier l'information à afficher dans l'estampille dans l'ordre désiré
      lignes:
        - 'Numéro de référence : {{NoConfirmation}}'
        - 'Date de transmission : {{FormatterDate DateTransmission "yyyy-MM-dd HH:mm:ss"}}'
#La section templates sert à définir les caractéristiques du gabarit utilisé.
#Lorsqu'on utilise le gabarit Word générique de FRW pour la production du fichier, cette section ne sert qu'à lister les champs à exclure.
templates:
- id: template1
  name: Fichier word
  gabarit:
    fr: NomDeVotreGabaritFR.docx
    en: NomDeVotreGabaritEN.docx
#ignorer permet de spécifier les champs du formulaire Web qu'on ne veut pas afficher dans le document produit.
ignorer:
- champ: champ1
- champ: champ2
````

## Créer votre premier fichier bind avec un gabarit PDF avec champs de saisie dynamique
La solution FRW permet d'envoyer les données du formulaire dans un gabarit PDF avec champs de saisie dynamique. 

Pour que FRW l'utilise, vous devez créer un répertoire "Gabarits" dans le même répertoire que votre formulaire en cours et y déposer votre gabarit en vous assurant qu'il soit déverouillé.

Vous pouvez ensuite modifier le fichier bind que vous avez créé précédemment en utilisant l'exemple suivant:

### Exemple de configuration de base avec un gabarit PDF avec champs de saisie dynamique

Détails:
1. Le fichier produit sera obligatoirement un PDF;
1. Le traitement utilisera le gabarit PDF spécifique que vous aurez déposé dans le répertoire "Gabarits".
1. Une estampille s'affichera sur le fichier produit;

````yaml
config:
  formulaire:
#Le système doit être l'identifiant de système autorisé que vous aurez obtenu de l'équipe FRW.
    systeme: 1
#Le type doit être le même nom que le répertoire de votre formulaire
    type: FormTest
#La section "pdf" permet de définir des options pour la production du fichier.
  pdf:
#rapetisserTexteTropLong permet de réduire automatiquement la taille de la police d'un texte qui dépasse légèrement la longueur du champ dans le gabarit PDF.
    rapetisserTexteTropLong: true
#redirigerAnnexeTexteTopLong permet de créer une page d'annexe après la dernière page du formulaire pour y afficher les champs qui dépassent la longueur permise dans le gabarit.
    redirigerAnnexeTexteTroplong: true
#pourcentageDepassementAnnexe permet de spécifier une limite avant de créer l'annexe des textes trop longs. En dessous de la limite, on rapetisse la police et au dessus, on créé l'annexe.
    pourcentageDepassementAnnexe: 20
#verouillerChampsPdf permet de verouiller le fichier lorsque le traitement a terminé d'insérer les valeurs.
    verrouillerChampsPdf: true
bundles:
#Le nomSortie sert à définir le nom du fichier qui sera produit. 
#Lorsqu'on utilise un gabarit PDF pour la production du fichier, il n'est pas nécessaire de spécifier d'extension puisque ce sera toujours un PDF.
  - nomSortie: FormTest
    templates:
      - test1
    estampille:
      positionX: 400
      positionY: 710
      tailleFont: 9
      lignes:
        - 'Numéro de référence : {{NoConfirmation}}'
        - 'Date de transmission : {{FormatterDate DateTransmission "yyyy-MM-dd HH:mm:ss"}}'
templates:
- id: test1
  name: NomInutile
  gabarit:
    fr: FormTest.v1.FR
    en: FormTest.v1.EN
````


