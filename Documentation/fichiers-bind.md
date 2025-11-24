# Configurer le(s) fichier(s) produit(s) à partir des données du formulaire (fichier bind)

L'outil FRW permet de générer un ou des fichiers à partir des données du formulaire transmis. Le fichier de configuration "bind" est requis afin de configurer le format et les caractéristiques de l'extrant à produire.

## Gabarits

La mise en page des données du formulaire dans un PDF peut être déterminée avec un gabarit Word ou un gabarit PDF avec champs de saisie dynamiques.

### Gabarit Word 

#### Gabarit Word générique

Un gabarit générique est offert par la solution FRW. Il affiche toutes les sections et les champs tels qu'ils sont paramétrés dans le formulaire.
Notez bien que seul les noms de section et les champs (libellé du champ et valeur associée) sont traités par le gabarit. Tous les éléments visuels (étapier, icônes, messages informationnels) sont exclus par le gabarit et ne s'affichent pas dans le PDF produit.

#### Gabarit Word personnalisé

Il est possible de se construire un gabarit word personnalisé, par exemple pour organiser la façon que les informations sont affichées dans une mise en page spécifique, ou pour mettre un logo spécifique.

### Gabarit PDF avec champs de saisie dynamiques

À utiliser lorsque les données du formulaire sont à insérer dans un fichier PDF avec champs de saisie dynamiques. Chaque champ doit alors être associé à une donnée du formulaire. Il est recommandé d’utiliser l’outil de binding pour produire cette section. Consulter le [guide de l’outil de binding](guide-outil-binding.md) pour produire votre premier fichier bind à l’aide de l’outil de binding. 

Important : le gabarit PDF doit être déverrouillé pour être utilisable par FRW.

## Tester vos formulaires
À tout moment, vous pouvez utiliser les [outils de développement](outils-developpement.md) afin de tester vos formulaires;

Référez vous à la section [Tester la transmission du formulaire](outils-developpement.md#tester-la-transmission-du-formulaire) pour prévisualiser le fichier produit à partir de la page Web du formulaire.

## Créer votre premier fichier bind avec le gabarit Word générique
Pour débuter et tester un premier coup votre fichier bind, vous devez créer le fichier dans le même répertoire que votre formulaire en cours. Il doit être nommé `NOM_DU_FORM.v0.bind.yml` où le `NOM_DU_FORM` est identique à votre nom de répertoire du formulaire.

Lorsque le fichier existe dans le répertoire du formulaire, vous pouvez essayer l'exemple suivant :

### 1- Exemple de configuration de base (gabarit Word)
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

### 2- Exemple de configuration avec un gabarit Word spécifique
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
#rotation permet d'appliquer une rotation au texte, par exemple 90 pour que le texte soit affiché verticalement de bas en haut.
      rotation: 90
#couleurRGBA permet de définir la couleur de l'estampille.
      couleurRGBA: [255, 0, 0]
#toutePages lorsqu'activé l'estampille est apposé sur toutes les pages.
      toutePages: true 
#lignes permet de spécifier l'information à afficher dans l'estampille dans l'ordre désiré
      lignes:
        - 'Numéro de référence : {{NoConfirmation}}'
        - 'Date de transmission : {{FormatterDate DateTransmission "yyyy-MM-dd HH:mm:ss"}}'
        - '{{{DonneesFormulaire.form.NomFamille}}}, {{{DonneesFormulaire.form.Prenom}}}'
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
  #La valeur du champ doit correspondre au nom du champ (name) que vous voulez exclure dans votre formulaire.
  # IMPORTANT: L'exclusion des champs se fait sur tous les champs qui débutent (startswith) par le nom du champ spécifié.
    - champ: TypesRevenusEmploi
    - champ: RevenuEmploiSalaireNet
````

## Créer votre premier fichier bind avec un gabarit PDF avec champs de saisie dynamique
La solution FRW permet d'envoyer les données du formulaire dans un gabarit PDF avec champs de saisie dynamique. 

Pour que FRW l'utilise, vous devez créer un répertoire "Gabarits" dans le même répertoire que votre formulaire en cours et y déposer votre gabarit en vous assurant qu'il soit déverrouillé.

Vous pouvez ensuite modifier le fichier bind que vous avez créé précédemment en utilisant l'un des exemples suivants :
* Exemple 3 : configuration de base
* Exemple 4 : configuration avancée

### 3- Exemple de configuration de base avec un gabarit PDF avec champs de saisie dynamique

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
    
#la section bind permet, en fonction des instructions de la configuration du formulaire, d’associer les bonnes valeurs du formulaire Web aux champs des gabarits PDF et d’appliquer un formatage si nécessaire.
bind:
  test1:
    E1_Nom:
      champs: [Enfants.0.Nom]
    adulte1_nom:
      champs: [adulte1NomFamille]
    adulte1_prenom:
      champs: [adulte1Prenom]
    A1_CP12:
      champs: [adulte1Cp12]
    adulte2_nom:
      champs: [adulte2NomFamille]
    adulte2_prenom:
      champs: [adulte2Prenom]
    A2_CP12:
      champs: [adulte2Cp12]
    E1_CP12:
      champs: [Enfants.0.Cp12]
    E1_Prenom:
      champs: [Enfants.0.Prenom]    
````

### 4- Exemple de configuration plus complexe, avec plusieurs bundles et plusieurs gabarit PDF avec champs de saisie dynamique

Il est possible de produire plusieurs fichiers en sortie, qui peuvent être produits à partir d’un éventail de gabarits personnalisés, selon une ou des conditions configurées.

Pour ce faire, votre fichier bind doit définir plusieurs « bundles ». Un bundle consiste en un regroupement de gabarits qui doivent être produits dans un fichier PDF distinct en sortie. Chaque bundle doit définir les caractéristiques suivantes : 
* **Nom en sortie** : nom du fichier qui sera produit.
* **Gabarit (template)** : quel(s) gabarit(s) utiliser pour ce fichier. Chaque bundle peut utiliser un ou des gabarits différents.
* **Condition** : Il est possible de spécifier une ou des conditions pour déterminer si le bundle est applicable. Pour ce faire, il faut utiliser les propriétés « conditionsEt » et « conditionsOu ». Le système vérifie si la ou les valeurs concernées du formulaire respectent la ou les conditions.

Chaque gabarit (template) définit les caractéristiques suivantes : 
* **Nom de fichier du gabarit (anglais et français)** : Il est obligatoire de spécifier votre gabarit, il n'y a pas de gabarit par défaut avec champs de saisie dynamiques;
* **Champs à ignorer** : Fonctionne uniquement avec gabarit word (exemples 1 et 2);
* **Condition** : Il est possible de spécifier une condition pour déterminer si le gabarit est applicable à l’aide des propriétés « conditionsEt » et « conditionsOu ». Le système vérifie si les valeurs du formulaire respectent les conditions.

Pour chaque gabarit (template) défini, il doit y avoir un bloc de config « bind : » défini. Cette section permet, en fonction des instructions de la configuration du formulaire, d’associer les bonnes valeurs du formulaire Web aux champs des gabarits PDF et d’appliquer un formatage si nécessaire.

La section bind consiste en la liste des noms de champs du PDF. Pour chacun, la valeur correspondante du formulaire doit être associée à l’aide de la propriété "champs". De plus il est possible de spécifier une formule.

Il est recommandé d’utiliser l’outil de binding pour produire cette section. Consulter le [guide de l’outil de binding](guide-outil-binding.md) pour produire votre premier fichier bind à l’aide de l’outil de binding. 

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
  # 1er fichier produit
  - nomSortie: FormTest1
    # si la condition est true, retourne la valeur après le :
    # sinon (la condition est false), ne retourne rien; lorsqu'il n'y a rien, il n'y a pas de condition à respecter, donc le bloc s'exécute 
    conditionsEt: '{TypeDemande:neContientPas(Afdr):false}'    
    templates:
      - template1
    estampille:
      positionX: 400
      positionY: 710
      tailleFont: 9
      lignes:
        - 'Numéro de référence : {{NoConfirmation}}'
        - 'Date de transmission : {{FormatterDate DateTransmission "yyyy-MM-dd HH:mm:ss"}}'
  # 2e fichier produit
  - nomSortie: FormTest2
    #Conjoint est une valeur booléenne provenant du formulaire
    conditionsEt: '{Conjoint}'    
    templates:
      - template2
    estampille:
      positionX: 400
      positionY: 710
      tailleFont: 9
      lignes:
        - 'Numéro de référence : {{NoConfirmation}}'
        - 'Date de transmission : {{FormatterDate DateTransmission "yyyy-MM-dd HH:mm:ss"}}'
  # 3e fichier produit; Il est possible, comme dans cet exemple, de produire en sortie un document informatif, c'est-à-dire sans qu'aucune information provenant du formulaire n'y soit affiché.  
  - nomSortie: DocumentInformatif
    conditionsEt: '{TypeDemande:neContientPas(Afdr):false}'
    templates:
      - DI1     

templates:
- id: template1
  name: NomInutile1
  gabarit:
    fr: FormTest1.v1.FR
    en: FormTest1.v1.EN
- id: template2
  name: NomInutile2
  gabarit:
    fr: FormTest2.v1.FR
    en: FormTest2.v1.EN
- id: DI1
  name: Document Informatif
  pdf:
    fr: DocumentInformatif.v1.FR
    en: DocumentInformatif.v1.EN
  # La propriété "toujoursProduire" s'applique aux gabarits informationnels seulement et sert à forcer le traitement à produire le document même s'il n'y a aucun champs du formulaire qui y sont associés.
  toujoursProduire: true

#la section bind permet, en fonction des instructions de la configuration du formulaire, d’associer les bonnes valeurs du formulaire Web aux champs des gabarits PDF et d’appliquer un formatage si nécessaire.
bind:
  template1:
    E1_Nom:
      champs: [Enfants.0.Nom]
    adulte1_nom:
      champs: [adulte1NomFamille]
    adulte1_prenom:
      champs: [adulte1Prenom]
    A1_CP12:
      champs: [adulte1Cp12]
    adulte2_nom:
      champs: [adulte2NomFamille]
    adulte2_prenom:
      champs: [adulte2Prenom]
    A2_CP12:
      champs: [adulte2Cp12]
    E1_CP12:
      champs: [Enfants.0.Cp12]
    E1_Prenom:
      champs: [Enfants.0.Prenom]
  template2:
    E1_Nom:
      champs: [Enfants.0.Nom]
    adulte1_nom:
      champs: [adulte1NomFamille]
    adulte1_prenom:
      champs: [adulte1Prenom]
    A1_CP12:
      champs: [adulte1Cp12]
    adulte2_nom:
      champs: [adulte2NomFamille]
    adulte2_prenom:
      champs: [adulte2Prenom]
    A2_CP12:
      champs: [adulte2Cp12]
    E1_CP12:
      champs: [Enfants.0.Cp12]
    E1_Prenom:
      champs: [Enfants.0.Prenom]    
````
