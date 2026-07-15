# Pré-remplir les données d'un formulaire 

Ce guide explique comment préparer et fournir des données en pré-remplissage au moment de la création du formulaire.

Ce guide couvre les opérations suivantes : 
- Obtenir la structure d'un formulaire
- Développement d'un service de préparation de pré-remplissage 

## Obtenir la structure d'un formulaire

> Disponible à partir de la release [2026.x](https://github.com/MTESSDev/FRW/releases)

Avant de construire un mécanisme de pré-remplissage pour un formulaire, il est recommandé d'utiliser le service **FRW119 - Obtenir la structure d'un formulaire**.

Ce service permet d'obtenir dynamiquement la définition complète d'un formulaire ainsi qu'un gabarit JSON de pré-remplissage prêt à être utilisé. 

### Pourquoi utiliser FRW119 ?

Traditionnellement, un système doit connaître à l'avance :

- les noms exacts des champs du formulaire;
- les groupes répétables;
- les champs obligatoires;
- les domaines de valeurs disponibles;
- la structure JSON attendue par FRW.

Le service **FRW119** permet plutôt de récupérer ces informations directement à partir de la configuration réelle du formulaire. 

Cela évite :

- les erreurs de nommage de champs;
- le maintien manuel de structures JSON;
- les ajustements nécessaires lors des évolutions d'un formulaire.

### Ce que retourne le service

Le service retourne notamment :

- la liste complète des champs du formulaire;
- le type de chaque champ (texte, date, nombre, case à cocher, liste déroulante, etc.);
- les informations sur les groupes répétables;
- les valeurs possibles pour les champs à choix;
- un objet `structurePreRemplissage`. 


<!-- 


Exemple simplifié :

```json
{
  "typeFormulaire": "1212",
  "champs": [
    {
      "nom": "NomComplet",
      "type": "text",
      "obligatoire": true
    }
  ],
  "structurePreRemplissage": {
    "form": {
      "NomComplet": ""
    }
  }
}
``` 

-->

### Comprendre les valeurs possibles retournées par FRW119

Lorsque le service est appelé avec le paramètre `vide=false` (valeur par défaut), le gabarit retourné dans `structurePreRemplissage` ne contient pas uniquement des valeurs vides. Il fournit également des indications sur le format attendu et les valeurs autorisées pour les champs de sélection.

Par exemple :

```json
{
  "form": {
    "TypeDomicile": "<sélection: propriete|chambre|logement|subventionne|familiale|autre>",
    "adulte1Genre": "<sélection: Feminin|Masculin>",
    "HabiteAvecAutreAdulte": "<sélection: true|false>",
    "adulte1DateNaissance": "<date: AAAA-MM-JJ>",
    "adulte1NomFamille": "<texte>"
  }
}
```

Ces indications permettent de comprendre rapidement :

- qu'un champ attend du texte (`<texte>`);
- qu'un champ attend une date au format `AAAA-MM-JJ`;
- qu'un champ attend une valeur numérique (`<nombre>`);
- qu'un champ attend une ou plusieurs valeurs parmi une liste prédéfinie (`<sélection: ...>`).

Le gabarit constitue donc un excellent point de départ pour construire ou valider une structure de pré-remplissage.

### Obtenir le détail des choix disponibles

En complément du gabarit, la propriété `champs` fournit les métadonnées détaillées de chaque champ.

Pour les champs de type :

- `select`
- `radio`
- `checkbox`

la propriété `valeursPossibles` contient la liste complète des codes acceptés et leur libellé.

Exemple :

```json
{
  "nom": "TypeDomicile",
  "type": "select",
  "valeursPossibles": {
    "propriete": {
      "fr": "Dans votre propriété"
    },
    "chambre": {
      "fr": "Dans une chambre ou en pension"
    },
    "logement": {
      "fr": "Dans un logement"
    }
  }
}
```

Dans cet exemple :

- les valeurs pouvant être transmises sont `propriete`, `chambre` ou `logement`;
- les libellés affichés à l'utilisateur sont obtenus à partir de `valeursPossibles`;
- le pré-remplissage doit utiliser la clé technique et non le libellé.

Exemple de pré-remplissage valide :

```json
{
  "form": {
    "TypeDomicile": "propriete"
  }
}
```

et non :

```json
{
  "form": {
    "TypeDomicile": "Dans votre propriété"
  }
}
```




### Cas des champs multisélection

Certains champs permettent plusieurs choix simultanément. Ils sont généralement représentés sous forme de tableaux dans `structurePreRemplissage`.

Par exemple :

```json
{
  "TypeDemande": [
    "<sélection: Afdr|AideEmploi>"
  ]
}
```

Une valeur pré-remplie pourrait être :

```json
{
  "form": {
    "TypeDemande": [
      "Afdr"
    ]
  }
}
```

ou encore :

```json
{
  "form": {
    "TypeDemande": [
      "Afdr",
      "AideEmploi"
    ]
  }
}
```

selon les règles du formulaire.

### Cas des groupes répétables

FRW119 permet aussi d'identifier les groupes répétables.

Dans le gabarit, ceux-ci apparaissent sous forme de tableaux contenant un objet exemple :

```json
{
  "form": {
    "adulte1Emplois": [
      {
        "NomEntreprise": "<texte>",
        "PeriodeDu": "<date: AAAA-MM-JJ>"
      }
    ]
  }
}
```

Dans la collection `champs`, les propriétés `groupe`, `repetable` et `maxOccurrences` permettent de déterminer si plusieurs occurrences sont autorisées.

Exemple :

```json
{
  "nom": "NomEntreprise",
  "groupe": "adulte1Emplois",
  "repetable": true,
  "maxOccurrences": 2
}
```

Cette information peut être utilisée par un système appelant pour générer dynamiquement un écran de configuration de pré-remplissage ou pour valider les données avant leur transmission.

### Recommandation

Pour une intégration complète, il est recommandé d'utiliser les deux parties de la réponse :

| Élément | Utilisation |
|----------|-------------|
| `structurePreRemplissage` | Obtenir rapidement la structure JSON attendue |
| `champs` | Obtenir les types, libellés, groupes répétables, champs obligatoires et valeurs permises |

Cette approche permet de bâtir un mécanisme de pré-remplissage robuste sans devoir maintenir manuellement la structure des formulaires ou les listes de valeurs autorisées.

### Comment utiliser le résultat

Le contenu de `structurePreRemplissage` représente le gabarit de pré-remplissage attendu par FRW. 

L'approche recommandée est :

1. Appeler FRW119 pour obtenir la structure du formulaire.
2. Conserver ou générer le gabarit retourné.
3. Remplacer les valeurs vides par les données provenant de votre système.
4. Retourner ce JSON comme résultat de votre service de pré-remplissage.
5. Utiliser ensuite cette structure lors de la création du formulaire avec FRW. 

Par exemple, à partir du gabarit :

```json
{
  "form": {
    "NomComplet": "",
    "DateNaissance": ""
  }
}
```

Votre service de pré-remplissage pourrait produire :

```json
{
  "form": {
    "NomComplet": "Jean Tremblay",
    "DateNaissance": "1980-01-15"
  }
}
```

### Paramètre `vide=true`

Le service FRW119 peut être appelé avec le paramètre optionnel `vide=true`. 

Dans ce mode, le gabarit retourné contient directement des valeurs utilisables :

```json
{
  "form": {
    "NomComplet": "",
    "AccepteConditions": false,
    "SportsPreferences": []
  }
}
```

Ce mode simplifie la génération d'un modèle de pré-remplissage dans les systèmes consommateurs.

### Accès au service

Le service est disponible dans le Swagger SIS de FRW. 

Exemple d'appel :

```http
GET /api/v1/SIS/structureFormulaire/{typeFormulaire}
GET /api/v1/SIS/structureFormulaire/{typeFormulaire}?vide=true
```

Une fois authentifié dans Swagger :

1. Sélectionner l'opération **FRW119 - Obtenir la structure d'un formulaire**.
2. Saisir le `typeFormulaire`.
3. Exécuter la requête.
4. Copier le contenu de `structurePreRemplissage`.
5. Utiliser cette structure comme base de votre mécanisme de pré-remplissage. 

### Séquence recommandée

```text
FRW119
  ↓
Obtention de la structure du formulaire
  ↓
Construction du pré-remplissage par le système
  ↓
FRW111 (création du formulaire)
```

L'utilisation de FRW119 est particulièrement utile lors du développement initial d'une intégration ou lorsqu'un formulaire évolue, puisqu'elle permet de toujours travailler à partir de la structure réelle configurée dans FRW. 

Vous devez créer un service de pré remplissage dans votre système qui fait cette opération.

Le but de ce service est de préparer les données afin qu'elles correspondent au format attendu par FRW en y ajoutant les valeurs déterminées par votre système.

Voici comment nous suggérons de procéder :

## Paramètres d'entrée du service de pré remplissage

| Nom du paramètre | Description |
| ---- | ---------- |
| Type formulaire | Correspond au nom du répertoire FRW de votre formulaire |
| Dictionnaire d'objet | Dictionnaire clé-valeur qui contiendra toutes les valeurs que vous désirez fournir au formulaire. <br><br> Ces données peuvent être contenues dans des objets dont le nom est réservé :<br>`form` : des informations pour renseigner des champs du formulaire comme le nom ou l'adresse<br>`formProtege (à partir de 2023.7)` : des informations pour renseigner des champs du formulaire qui ne pourront pas être altérées par l'utilisateur. Le contenu de cet objet s'ajoute au contenu de l'objet `form` et lorsqu'un champ existe dans les deux objets, la valeur de l'objet `formProtege`a préséance. <br> L'objet `formProtege` remplace celui qui était présent dans la BD même si celui-ci a été fourni null ou vide. <br> S'il n'est pas fourni, l'objet présent dans la BD demeure intouché. <br>`config` : un ou des domaines de valeurs personnalisés<br>`systeme` : des informations réservées au système FRW actuellement l’adresse courriel pour l’enregistrement du formulaire<br>`informationsSupplementaires` : des informations supplémentaires, pouvant contenir un contexte ou un texte de bas de page de formulaire (propriétés `contexte` et `basPage`)<br><br>Il est aussi possible d’utiliser des objets personnalisés réutilisables durant le traitement, qui sont redonnées en sortie au moment de la transmission, par exemple :<br>- Des informations pour l’estampille, qui sont récupérées au moment de la création de l’estampille<br>- un contexte applicatif appartenant à votre système|

## Traitement à effectuer

1. Définir la structure des données de pré remplissage pour chaque type de formulaire\
  Vous pouvez utiliser des fichiers de configuration pour gérer cette partie.
  Voici un exemple de configuration de pré remplissage dans lequel on défini les noms des champs du formulaire (à gauche) et les valeurs reçues en paramètre d'entrée (à droite):

````json
{
	"form": {
		"adulte1NomFamille": {{{Json GD_NM_INDV}}},
		"adulte1Prenom": {{{Json GD_NM_PREN_INDV}}},
		"adulte1DateNaissance": {{{Json GD_D_NAIS}}},
		"adulte1Nas1": {{{Json GD_N_NAS}}},
		"adulte1Sexe": "{{#ifCond GD_C_SEXE '=' "M"}}Masculin{{else}}Feminin{{/ifCond}}",
		"adulte1Cp12": {{{Json GD_N_CP10 GD_N_CP12_JUM}}},
		"adulte1Nam": {{{Json GD_N_NAM}}}
	},
	// L'objet formProtege sert à s'assurer que la source du champ proviendra du système autorisé. 
	// Un utilisateur ne pourra jamais altérer le contenu d'un champ présent dans cet objet.
	// Dans cet exemple, la valeur du champ "adulte1NAS1" de l'objet "form" sera écrasée par celle de l'objet "formProtege" et les champs de "adulte1Adresse" s'ajouteront à l'objet "form" également. 
	"formProtege": {
		"adulte1Nas1": {{{Json GD_N_NAS}}},
		"adulte1Adresse": [
			{
				"NoCivique": {{{Json GD_A_NUMR_CIVQ}}},
				"Appartement": {{{Json GD_A_NUMR_APPR}}},
				"CodePostal": {{{Json GD_A_COD_POST}}},
				"Rue": {{{Json GD_A_RUE_RANG_CASR}}},
				"Municipalite": {{{Json GD_A_NOM_MUNC}}},
				"Province": "Québec"
			}
		]
	},
	 "config": {
	      "domaines": {
	    "sportsPreRemplissage": {
	      "Course": {
		"label": {
		  "fr": "Course à pied",
		  "en": "(EN) Course à pied"
		},
		"mots-cle": {
		  "fr": "chaussure",
		  "en": "shoe"
		}
	      },
	      "Hache": {
		"label": {
		  "fr": "Lancer de la hache",
		  "en": "Axe throwing"
		},
		"mots-cle": {
		  "fr": "Hache",
		  "en": "Axe"
		}
	      },
	      "Saut": {
		"label": {
		  "fr": "Saut en hauteur",
		  "en": "(EN) Saut en hauteur"
		},
		"mots-cles": {
		  "fr": "Haut",
		  "en": "High"
		}
	      }  
	    }
	  }
	},	
	// La partie estampille permet d'envoyer des données du système dans l'estampille apposée sur le fichier produit par FRW lorsqu'applicable.
	"estampille": {
		"texteAuthentification": "TexteAuthentification"
	},
	// La propriété informationsSupplementaires permet de sauvegarder des informations supplémentaires dans la BD. Ces données peuvent contenir un contexte de formulaire, qui sera affiché en évidence dans une zone prévue à cet effet dans chaque section du formulaire. Ces données ne sont pas chiffrées et ne doivent pas contenir d'informations sensibles.
	"informationsSupplementaires": {
		"Cle1": {{{Valeur1}}},
		"contexte": {{{ContexteFormulaire}}}
	}
}
````

2. Le service de pré-remplissage doit récupérer la structure définie au point précédent et remplacer les balises par les valeurs reçues en paramètre d'entrée.
	- Le remplacement des variables dans l'exemple ci-haut se fait grâce à un outil de syntaxe ``mustache``, nous recommandons d'utiliser [HandleBars.Net](https://github.com/Handlebars-Net/Handlebars.Net), ou encore mieux le produit [YamlHttpClient](https://github.com/anisite/YamlHttpClient) qui permet d'appeler un API par configuration ``Yaml`` et s'occupera lui-même de remplacer vos variables. 
3. Le service de pré-remplissage retourne l'information en sortie.

## Paramètres de sortie du service de pré remplissage

| Nom du paramètre | Description |
| ---- | ---------- |
| Contenu formulaire | Contient la structure de pré remplissage avec les valeurs remplacées en format JSON |


## Création versus modification

Certaines informations peuvent être prises en compte seulement au moment de la création du formulaire, d’autres peuvent aussi être modifiées lors de la reprise (reprise "authentifiée" seulement). Le tableau suivant résume les possibilités : 

| Type  d'information pré-remplie | Création | Reprise |
| ---- | ---------- | ---------- |
| Champs de formulaire (form) | ✔ |  |
| Champs de formulaire protégés (formProtege) | ✔ | ✔ |
| Propriétés personnalisées | ✔ | ✔ |
| Informations supplémentaires | ✔ |  |
| Domaine de valeurs personnalisées | ✔ | ✔ |

## Pré-remplissage anonyme
> À partir de la version ``2025.10``

Le pré-remplissage est maintenant disponible pour les formulaires anonymes, toutefois vous devez préalablement autoriser les champs concernés dans la config "form.yml" de votre formulaire ou de votre système autorisé.

> Important : 
> - Ne pas autoriser le pré-remplissage de données sensibles.
> - Le système supporte des données en pré-remplissage d'une longueur jusqu'à environ 1000 caractères maximum.

Pour plus de détails, voir la section [Personnalisation des formulaires - Concepts de base](https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=personnalisationBase) du P700.
