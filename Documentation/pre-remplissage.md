# Pré-remplir les données d'un formulaire 

Ce guide explique comment fournir des données en pré-remplissage au moment de la création du formulaire.

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
