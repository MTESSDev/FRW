# Pré-remplir les données d'un formulaire

Ce guide explique comment fournir des données en pré-remplissage au moment de la création du formulaire.

Vous devez créer un service de pré remplissage dans votre système qui fait cette opération.

Le but de ce service est de préparer les données afin qu'elles correspondent au format attendu par FRW en y ajoutant les valeurs déterminées par votre système.

Voici comment nous suggérons de procéder:

## Paramètres d'entrée du service de pré remplissage

| Nom du paramètre | Description |
| ---- | ---------- |
| Type formulaire | Correspond au nom du répertoire FRW de votre formulaire |
| Dictionnaire d'objet | Dictionnaire clé-valeur qui contiendra toutes les valeurs que vous désirez fournir au formulaire. <br><br> Ces données peuvent être contenues dans des objets dont le nom est réservé :<br>`form` : des informations pour renseigner des champs du formulaire, comme par exemple le nom ou l'adresse<br>`config` : un ou des domaines de valeurs personnalisés<br>`systeme` : des informations réservées au système FRW actuellement l’adresse courriel pour l’enregistrement du formulaire<br>`informationsSupplementaires` : des informations supplémentaires, pouvant contenir un contexte de formulaire (dans la propriété `contexte`)<br><br>Il est aussi possible d’utiliser des objets personnalisés réutilisables durant le traitement, qui sont redonnées en sortie au moment de la transmission, par exemple :<br>- Des informations pour l’estampille, qui sont récupérées au moment de la création de l’estampille<br>- un contexte applicatif appartenant à votre système|

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
		"adulte1Nam": {{{Json GD_N_NAM}}},
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

3. Le service de pré-remplissage retourne l'information en sortie.


## Paramètres de sortie du service de pré remplissage

| Nom du paramètre | Description |
| ---- | ---------- |
| Contenu formulaire | Contient la structure de pré remplissage avec les valeurs remplacées en format JSON |


## Création versus modification

Certaines informations peuvent être prises en compte seulement au moment de la création du formulaire, d’autres peuvent aussi être modifiées lors de la reprise. Le tableau suivant résume les possibilités : 

| Type  d'information pré-remplie | Création | Reprise |
| ---- | ---------- | ---------- |
| Champs de formulaire | ✔ |  |
| Propriétés personnalisées | ✔ | ✔ |
| Informations supplémentaires | ✔ |  |
| Domaine de valeurs personnalisées | ✔ | ✔ |
