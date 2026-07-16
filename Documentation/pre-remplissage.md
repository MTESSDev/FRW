# Pré-remplir les données d'un formulaire

## Qu'est-ce que le pré-remplissage?

Le pré-remplissage permet d'initialiser automatiquement certaines données d'un formulaire à partir d'informations déjà connues par un système.

Lors de la création du formulaire, un système peut fournir un objet JSON contenant des valeurs qui seront automatiquement appliquées aux champs du formulaire.

Le pré-remplissage peut notamment être utilisé pour :

- éviter à l'utilisateur de saisir des informations déjà connues;
- réduire les erreurs de saisie;
- accélérer le remplissage du formulaire;
- transmettre des informations provenant d'autres systèmes;
- protéger certaines données qui ne doivent pas être modifiées par l'utilisateur.

Ce guide explique les grandes étapes recommandée pour construire un pré-remplissage.

## Paramètres possibles du JSON de pré-remplissage

Exemple à haut niveau de structure de pré-remplissage : 
```json
{
  "form": { ... },
  "formProtege": { ... },
  "config": { ... }, 
  "informationsSupplementaires": { ... }
}
```

Le JSON de pré-remplissage peut contenir différentes propriétés selon les besoins de l'intégration. 

Voici quelques exemples : 

<table>
<tr> 
<td> Propriété </td> 
<td> Description </td> 
<td> Exemple </td> </tr>
<tr> <td> <pre>form</pre> </td> 
<td>Contient les données qui seront utilisées pour pré-remplir les champs du formulaire. Les valeurs peuvent être modifiées par l'utilisateur. </td>
<td>

```json
{
  "form": {
    "Conjoint": "false",
    "TypeDemande": [
      "Afdr",
      "AideEmploi"
    ],
    "HabiteAvecAutreAdulte": "false",
    "TypeDomicile": "propriete",
    "DomicileDateDebut": "2022-04-13",
    "adulte1Nas1": "123456789",
    // [...]
  }
}
```

</td>

</tr>
<tr>
<td> <pre>formProtege</pre> </td>
<td> Contient les données dont la valeur doit obligatoirement provenir du système autorisé. Les champs présents dans cet objet ne peuvent pas être modifiés par l'utilisateur. Si un même champ existe dans `form` et `formProtege`, la valeur de `formProtege` a préséance. </td>
<td>

```json
{
  // Dans cet exemple, la valeur du champ "adulte1Nas1" 
  // de l'objet "form" sera écrasée par celle de l'objet 
  // "formProtege" à la transmission et le champs 
  // "adulte1estRoux" sera ajouté dans l'objet "form" également. 
  "formProtege": {
    "adulte1Nas1": "888888880",
    "adulte1estRoux" : true
  }
}
```

</td>
</tr>
<tr>
<td> <pre>config</pre> </td>
<td> Permet notamment de fournir des domaines de valeurs personnalisés. </td>
<td>

```json
{
  "config": {
    // Exemple de pré-remplissage d'une domaine de valeurs
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
  }
}
```

</td>
</tr>

<tr> <td> <pre>informationsSupplementaires</pre> </td> 
<td>Permet d'enregistrer des informations supplémentaires associées au formulaire, par exemple un contexte affiché à l'utilisateur. Ces données ne sont pas chiffrées et ne doivent pas contenir d'informations sensibles. <br><br> Pour plus de détails, voir le guide utilisateur P700 aux sections <a href="https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=pageContexte" target="blank">Contexte</a> et <a href="https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=pageBasPage" target="blank">Bas de page</a>. </td>
<td>

```json
{
	"informationsSupplementaires": {
    "contexte": "Année financière 2023-2024",
    "basPage" : "PDF Version 3.4"
        // [...]
    }
}
```

</td>
</tr>

<tr> <td> Propriétés personnalisées  </td> 
<td>Il est possible d'ajouter des objets personnalisés propres à votre intégration, par exemple pour un contexte applicatif, une estampille ou d'autres besoins techniques. Ces informations sont redonnés en sortie au moment de la transmission, pouvant ainsi être exploitées par votre API de réception de formulaire (le cas échéant). </td>
<td>

```json
{
	"estampille": {
		"texteAuthentification": "TexteAuthentification"
  },
  "contexteECS": " ... contenu en base  64 ... "
}
```

</td>
</tr>

</table>

## Obtenir la structure d'un formulaire

Disponible à partir de la release [2026.x](https://github.com/MTESSDev/FRW/releases).

Afin de pouvoir construire un pré-remplissage, il est recommandé d'utiliser le service **FRW119 - Obtenir la structure d'un formulaire**.

Paramètres d'entrée :
- type formulaire
- vide : détermine si des indications permettant de comprendre le format attendu pour chaque champ est présenté dans le retour ou non

Ce service retourne :

- la structure JSON attendue par FRW;
- la liste des champs du formulaire;
- le type de chaque champ;
- les groupes répétables;
- les valeurs permises pour les champs de sélection;
- les métadonnées nécessaires à la validation des données.

### Exemple de structure retournée

> Dans cet exemple le service a été appelé avec le paramètre "vide" à `false`.  

```json
{
  "typeFormulaire": "3003",
  "structurePreRemplissage": {
    "form": {
    
      // Champ texte
      "adulte1NomFamille": "<texte>",
      // Champ date
      "adulte1DateNaissance": "<date: AAAA-MM-JJ>",
      // Champ numérique
      "revenuAnnuel": "<nombre>",
      // Champ de sélection simple (select)
      "TypeDomicile": "<sélection: propriete|chambre|logement|subventionne|familiale|autre>",
      // Champ radio ou booléen
      "HabiteAvecAutreAdulte": "<sélection: true|false>",
      // Liste de sélection
      "adulte1Genre": "<sélection: Feminin|Masculin>",
      // Champ multi-sélection : plusieurs valeurs peuvent être sélectionnées
      "TypeDemande": [
        "<sélection: Afdr|AideEmploi>"
      ],
      // Groupe répétable : le tableau contient un exemple d'occurrence
      "adulte1Emplois": [
        {
          "NomEntreprise": "<texte>",
          "PeriodeDu": "<date: AAAA-MM-JJ>",
          "PeriodeAu": "<date: AAAA-MM-JJ>"
        }
      ]
	  },
  },
  "champs": // détaillé à la section suivante
}
```

### Section "champs"

En complément de `structurePreRemplissage`, le service retourne une collection `champs`.

Cette collection permet notamment de connaître :

- le nom du champ;
- le type du champ;
- le groupe auquel il appartient;
- son caractère répétable;
- le nombre maximal d'occurrences;
- ses valeurs permises;
- ses libellés;
- son caractère obligatoire.

Exemple :

```json
{
  // [...]
  "champs": [
    {
      "nom": "TypeDomicile",
      "type": "select",
      "obligatoire": true,
      "repetable": false,
      "valeursPossibles": {
        "propriete": {                  // <---- utiliser cette valeur dans le pré-remplissage
          "fr": "Dans votre propriété"  // <---- ceci est le libellé visible à l'écran
        },
        "chambre": {
          "fr": "Dans une chambre ou en pension"
        },
        "logement": {
          "fr": "Dans un logement"
        }
      }
    },
    {
      "nom": "NomEntreprise",
      "groupe": "adulte1Emplois",
      "repetable": true,               // <---- ici il s'agit d'un groupe répétable
      "maxOccurrences": 2,             // <---- max 2 occurrences
      // [...]      
    }
  ]
}
```

## Séquence recommandée

Idéalement un développement est réalisé de votre côté afin d'automatiser les étapes de construction du pré-remplissage, afin d'éviter à faire du manuel à chaque fois.

Les grandes étapes sont : 

1. Appeler FRW119 pour obtenir la structure du formulaire.
2. Utiliser le gabarit `form` sous `structurePreRemplissage` comme modèle de départ.
3. Utiliser la collection `champs` pour comprendre les types, les valeurs permises et les groupes répétables.
4. Remplacer les valeurs du modèle par les données provenant de votre système.
5. Utiliser ce JSON lors de la création du formulaire avec FRW.

Cette approche permet de toujours travailler à partir de la structure réellement configurée dans FRW sans devoir maintenir manuellement une définition de formulaire.

## Idées d'implémentation

Plusieurs approches peuvent être utilisées pour fusionner les données provenant de votre système avec la structure retournée par FRW119.

Par exemple :
- génération programmatique du JSON;
- moteurs de gabarits Mustache; permet le remplacement de variables avec la syntaxe `mustache`
- [HandleBars.Net](https://github.com/Handlebars-Net/Handlebars.Net), ou encore mieux le produit 
- [YamlHttpClient](https://github.com/anisite/YamlHttpClient); permet d'appeler un API par configuration ``Yaml`` et l'outil s'occupe lui-même de remplacer vos variables. 

Vous pouvez communiquer avec nous si vous souhaitez en savoir plus.

Le choix de la technologie utilisée demeure à la discrétion du système intégrateur.

## Accès au service

Exemples d'appel à l'API (`structureFormulaire` - FRW119) :

```http
GET /api/v1/SIS/structureFormulaire/{typeFormulaire}

GET /api/v1/SIS/structureFormulaire/{typeFormulaire}?vide=true
```

**Authentification** 

Deux possibilités :
  - *Par clé d'API de Système autorisé :* Fournir le numéro public de votre système autorisé ainsi que la clé d'API; 
    - entêtes HTTP `X-NoPublicSystemeAutorise` et `X-ApiKey`.
  - *Par clé d'API de Partenaire externe :* Fournir la clé de partenaire externe dans l'entête HTTP `X-ClePartenaire`.

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
