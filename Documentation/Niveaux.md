# Les divers fichiers de configuration et leurs niveaux

## Les niveaux 
Il existe 3 niveaux de configuration, Global, Système et Formulaire, plusieurs section de configuration peuvent être définies et redéfinies à différents niveaux.

1. **Global**\
   Ce niveau ***n'est pas définissable par un système autorisé***, il est géré par l'équipe FRW et permet de configurer la base de l'application.

1. **Système**\
   Ce niveau est en réalité la racine de votre déploiement, c'est au même niveau que vos différents répertoires de formulaires, c'est à cet endroit que vous pouvez configurer certaines options que vous désirez appliquées par défaut à ***tous vos formulaires***.

1. **Formulaire**\
   Ce niveau se situe un répertoire plus creux, c'est le répertoire portant le nom de votre formulaire, celui-ci permet de configurer certaines options ***spécifiques***.


## Les types de configuration

1. **Formulaire**\
   C'est le fichier le plus important, le pilier de votre formulaire, il contient la configuration de l'interface de l'outil et du formulaire lui même

1. **Transmission**\
   Votre formulaire est prêt à transmettre quelque part? Vous désirez traiter les données? C'est le fichier de configuration pour cela, il vous permettra de définir les différentes tâches à exécuter en sortie pour traiter vos données à votre goût. Parfois, il aura besoin de l'aide du fichier `Bind`.

1. **Binding**\
   C'est le fichier qui permet de gérer le comportement voulu lors de la préparation d'un fichier PDF avec champs de saisies (il est primordial pour assigner à chaque champs du PDF une "source" de donnée provenant du formulaire FRW) ou encore de la génération automatique d'un fichier PDF de type Questions/Réponses à partir d'un gabarit Word, dans ce cas, il servira à empêcher certains champs d'apparaître sur le document final.\
   Il est aussi le responsable de la création des "bundles" qui permettent de produire plusieurs fois certains PDF avec plus ou moins de données ou en appliquant quelques variantes, assez utile pour par exemple produire une version interne et une version citoyenne d'un document.

## Quels fichiers à quels niveaux

Ci-dessous, un tableau des différents noms que doivent porter vos fichiers de configuration, selon leur type et selon leur emplacement (niveau). `NOM_DU_FORM` doit être remplacer par le nom du formulaire (donc du répertoire dans lequel il se trouve).
| Configuration | Nom fichier Niveau Global | Nom fichier Niveau Système | Nom fichier niveau Formulaire|
|---|---|---|---|
| Formulaire | default.v0.form.yml | default.v0.form.yml | NOM_DU_FORM.v1.form.yml |
| Transmission |  | default.v0.transmission.yml | NOM_DU_FORM.v0.transmission.yml |
| Binding |  |  | NOM_DU_FORM.v1.bind.yml |

