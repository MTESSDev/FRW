# Exemple json de l'appel API d'un service externe

Exemple réel avec de vrais fichiers base64 binaires et contenu réel.

````json
{
	"langue": "fr",
	"noFormulaire": 16894,
	"typeFormulaire": "3003",
	"noConfirmation": 122222311,
	"noExecution": null,
	"documentsProduits": [
		{
			"fichier": "AA==",
			"nom": "3003_01_FICHIER_NULL_POUR_ALLEGER"
		},
		{
			"fichier": "AA==",
			"nom": "3003_02_FICHIER_NULL_POUR_ALLEGER"
		}
	],
	"donneesFormulaire": {
		"form": {
			"EtatRevision": "initial",
			"validAll": false,
			"adulte1Cp12": null,
			"Conjoint": "false",
			"TypeDemande": [
				"Afdr"
			],
			"HabiteAvecAutreAdulte": "true",
			"adulte1NeQC": "false",
			"adulte1NeCanada": "true",
			"adulte1AjoutPJCertificatNaissance": "true",
			"adulte1GrpPJCertificatNaissance": [
				{
					"TypeDocument": "INFOPERS",
					"LigneAffaire": "ASF",
					"PJCertificatNaissance": [
						{
							"url": "wwogkwqn8DUnD19LqkrMfnJQAv1LEju76q0ADoZwFZRLKgoLO2INgony4VNK.pdf",
							"name": "ECS - Schéma solution formulaires dynamiques_2021-07-05.pdf",
							"_type": "customFile"
						}
					]
				}
			],
			"adulte1Nas2": null,
			"adulte1EstValidePourTravailler": null,
			"adulte1Telephone2": null,
			"adulte1Handicap": null,
			"adulte1LanguesParlees": null,
			"adulte1LanguesEcrites": null,
			"adulte1CasierJudiciaire": null,
			"adulte1MinoriteVisible": null,
			"DestinataireAutrePersonne": null,
			"TexteRenseignementsAdditionnels": null,
			"Procuration": null
		},
		"systeme": {},
		"X-NoConfirmation": -1,
		"X-DateTransmission": "2023-03-13T21:04:32.5490054-04:00"
	},
	"configDev": {
		"etatrevision": "",
		"validall": "False",
		"pjmanquantes": "System.Object[]",
		"codent": "mes\\cotda05"
	},
	"fichiersExternes": null,
	"idUtilisateur": "TestUtil",
	"dateTransmission": "2023-03-13T21:04:32.5490054-04:00",
	"modeSimulation": true,
	"documentsSoumis": {
		"adulte1GrpPJCertificatNaissance_0_PJCertificatNaissance": [
			{
				"url": "ol3JOlgA9rhm7zZXg5WNFGk7mZOBvwcn81ByPlYkcjowKxkwJqT67mvkXW60IzmWOEGxQ4c59y.pdf",
				"name": "adulte1GrpPJCertificatNaissance_0_PJCertificatNaissance.pdf",
				"TypeDocument": "INFOPERS",
				"LigneAffaire": "ASF"
			}
		]
	},
	"questionsFormulaire": {
		"TypeDemande": {
			"label": {
				"fr": "Quel type de demande voulez-vous effectuer?",
				"en": "Which type of application do you want to submit?"
				},
			"options": {
			"Afdr": {
				"fr": "Demande d'aide financière de dernier recours (aide sociale)",
				"en": "Application for last-resort financial assistance (social assistance)"
				},
			"AideEmploi": {
				"fr": "Demande de services d'emploi",
				"en": "Application for employment services"
				}
			}
		},
		"HabiteAvecAutreAdulte": {
			"label": {
				"fr": "Habitez-vous avec un autre adulte?",
				"en": "Are you living with another adult?"
				},
			"options": {
				"true": {
					"fr": "Oui",
					"en": "Yes"
				},
				"false": {
					"fr": "Non",
					"en": "No"
				}
			}
		},
		"adulte1NeQC": {
			"label": {
				"fr": "Êtes-vous né au Québec?",
				"en": "Were you born in Québec?"
			},
			"options": {
				"true": {
					"fr": "Oui",
					"en": "Yes"
				},
				"false": {
					"fr": "Non",
					"en": "No"
				}
			}
		}
	},
	"informationsSupplementaires": {
		"inutile1": "ben oui maxi",
		"contexte": "Marc Lalancette test - Demande #736553 - Année financière 2023"
	}
}
````
