# Configurer le fichier produit à partir des données du formulaire (fichier bind)

L'outil FRW permet de générer un fichier à partir des données du formulaire transmis. Le fichier de configuration "bind" est requis afin de configurer le format et les caractéristiques de l'extrant à produire.

## Créer votre premier fichier bind avec le gabarit Word générique
Pour débuter et tester un premier coup votre fichier bind, vous devez créer le fichier dans le même répertoire que votre formulaire en cours. Il doit être nommé NOM_DU_FORM.v0.bind.yml où le NOM_DU_FORM est identique à votre nom de répertoire du formulaire.

Lorsque le fichier existera dans le répertoire du formulaire, vous pouvez essayer les différents exemples suivants :

### Exemple de configuration de base (gabarit Word)
Détails:
1. Le fichier produit est un PDF;
1. Utilise le gabarit Word générique offert par la solution FRW;
1. Aucune estampille ne s'affiche sur le fichier produit;
1. Tous les champs du formulaire Web vont s'afficher dans le fichier produit;

````yaml
bundles:
#Le nomSortie sert à définir le nom du fichier qui sera produit. 
#Lorsqu'on utilise un gabarit Word pour la production du fichier, on doit spécifier l'extension désirée du document.
#Dans ce cas-ci, le fichier produit par FRW sera un fichier PDF. La solution supporte les PDF et les DOCX.
  - nomSortie: test.pdf
#Le template permet de référer à la section template plus bas dans le fichier.
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
  #Le name n'est pas utilisé dans le traitement. Vous pouvez mettre n'importe quoi.
  name: Fichier word
````

### Exemple de configuration avec un gabarit Word spécifique
Détails:
1. Le fichier produit est un DOCX;
1. Utilise un gabarit Word spécifique;
1. Aucune estampille ne s'affiche sur le fichier produit;
1. Certain champs du formulaire Web ne seront pas affichés dans le fichier produit;

````yaml
bundles:
#Le nomSortie sert à définir le nom du fichier qui sera produit. 
#Lorsqu'on utilise un gabarit Word pour la production du fichier, on doit spécifier l'extension désirée du document.
#Dans ce cas-ci, le fichier produit par FRW sera un fichier PDF. La solution supporte les PDF et les DOCX.
  - nomSortie: test.pdf
#Le template permet de référer à la section template plus bas dans le fichier.
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
#ignorer permet de spécifier les champs du formulaire Web qu'on ne veut pas afficher dans le document produit.
ignorer:
- champ: champ1
- champ: champ2
````

Vous pouvez maintenant tester votre formulaire.


