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

Ce guide explique les grandes étapes recommandées pour construire un pré-remplissage.

## Paramètres possibles du JSON de pré-remplissage

Exemple de structure de pré-remplissage à haut niveau :

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
<td>Propriété</td>
<td>Description</td>
<td>Exemple</td>
</tr>

<tr>
<td><code>form</code></td>
<td>Contient les données qui seront utilisées pour pré-remplir les champs du formulaire. Les valeurs peuvent être modifiées par l'utilisateur.</td>
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
    "adulte1Nas1": "123456789"
  }
}
```

</td>
</tr>

<tr>
<td><code>formProtege</code></td>
<td>Contient les données dont la valeur doit obligatoirement provenir du système autorisé. Les champs présents dans cet objet ne peuvent pas être modifiés par l'utilisateur. Si un même champ existe dans <code>form</code> et <code>formProtege</code>, la valeur de <code>formProtege</code> a préséance.</td>
<td>

```json
{
  // Dans cet exemple, la valeur du champ "adulte1Nas1"
  // de l'objet "form" sera écrasée par celle de l'objet
  // "formProtege" à la transmission et le champ
  // "adulte1estRoux" sera également ajouté à l'objet "form".
  "formProtege": {
    "adulte1Nas1": "888888880",
    "adulte1estRoux": true
  }
}
```

</td>
</tr>

<tr>
<td><code>config</code></td>
<td>Permet notamment de fournir des domaines de valeurs personnalisés.<br><br> Pour plus de détails, voir le guide utilisateur P700 à la section <a href="https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=DomainesValeurs" target="blank">Domaines de valeurs</a>.</td>
<td>

```json
{
  "config": {
    // Exemple de pré-remplissage d'un domaine de valeurs
    "domaines": {
      "sportsPreRemplissage": {
        "Course": {
          "label": {
            "fr": "Course à pied",
            "en": "(EN) Course à pied"
          },
          "mots-cles": {
            "fr": "chaussure",
            "en": "shoe"
          }
        },
        "Hache": {
          "label": {
            "fr": "Lancer de la hache",
            "en": "Axe throwing"
          },
          "mots-cles": {
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

<tr>
<td><code>informationsSupplementaires</code></td>
<td>Permet d'enregistrer des informations supplémentaires associées au formulaire, par exemple un contexte affiché à l'utilisateur. Ces données ne sont pas chiffrées et ne doivent pas contenir d'informations sensibles.<br><br> Pour plus de détails, voir le guide utilisateur P700 aux sections <a href="https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=pageContexte" target="blank">Contexte</a> et <a href="https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=pageBasPage" target="blank">Bas de page</a>. </td>
<td>

```json
{
  "informationsSupplementaires": {
    "contexte": "Année financière 2023-2024",
    "basPage": "PDF Version 3.4"
  }
}
```

</td>
</tr>

<tr>
<td>Propriétés personnalisées</td>
<td>Il est possible d'ajouter des objets personnalisés propres à votre intégration, par exemple pour un contexte applicatif, une estampille ou d'autres besoins techniques. Ces informations sont retournées lors de la transmission et peuvent ainsi être exploitées par votre API de réception de formulaire (le cas échéant).</td>
<td>

```json
{
  "estampille": {
    "texteAuthentification": "TexteAuthentification"
  },
  "contexteECS": " ... contenu en base 64 ... "
}
```

</td>
</tr>

</table>

## Obtenir la structure d'un formulaire

Disponible à partir de la release [2026.7](https://github.com/MTESSDev/FRW/releases).
Afin de pouvoir construire un pré-remplissage, il est recommandé d'utiliser le service **FRW119 - Obtenir la structure d'un formulaire**.

Ce service retourne :
- la structure JSON attendue par FRW;
- la liste des champs du formulaire;
- le type de chaque champ;
- les groupes répétables;
- les valeurs permises pour les champs de sélection;
- les métadonnées nécessaires à la validation des données.

Paramètres d'entrée :
- Type de formulaire;
- Booléen `vide` : détermine si le gabarit retourné contient des valeurs vides (vrai) ou des indications permettant de comprendre le format attendu pour chaque champ (faux).

Exemples d'appel à l'API (`structureFormulaire` - FRW119) :

```http
GET /api/v1/SIS/structureFormulaire/{typeFormulaire}

GET /api/v1/SIS/structureFormulaire/{typeFormulaire}?vide=true
```

| Méthode d'authentification | En-tête HTTP |
|--|--|
| Authentification par clé d'API de Système autorisé | Fournir le numéro public de votre système autorisé ainsi que la clé d'API dans les en-têtes HTTP `X-NoPublicSystemeAutorise` et `X-ApiKey`.
| Par clé d'API de Partenaire externe                | Fournir la clé de partenaire externe dans l'en-tête HTTP `X-ClePartenaire`.


### Exemple de structure retournée

> Dans cet exemple, le service a été appelé avec le paramètre `vide` à `false`.

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
      // Champ à sélection multiple : plusieurs valeurs peuvent être sélectionnées
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
    }
  },
  "champs": // détaillé à la section suivante
}
```

### Section champs

En complément de `structurePreRemplissage`, le service retourne une collection `champs`.

Cette collection permet notamment de connaître :

- le nom du champ;
- le type du champ;
- le groupe auquel il appartient;
- son caractère répétable;
- le nombre maximal d'occurrences;
- les valeurs permises;
- les libellés;
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
        "propriete": {                  // <---- utiliser cette clé dans le pré-remplissage
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

Idéalement, un développement est réalisé de votre côté afin d'automatiser les étapes de construction du pré-remplissage et d'éviter d'effectuer ces opérations manuellement à chaque fois.

Les grandes étapes sont :

1. Appeler FRW119 pour obtenir la structure du formulaire.
2. Utiliser le gabarit `form` sous `structurePreRemplissage` comme modèle de départ.
3. Utiliser la collection `champs` pour comprendre les types, les valeurs permises et les groupes répétables.
4. Remplacer les valeurs du modèle par les données provenant de votre système.
5. Utiliser ce JSON lors de la création du formulaire avec FRW.

Cette approche permet de toujours travailler à partir de la structure réellement configurée dans FRW sans devoir maintenir manuellement une définition du formulaire.

## Idées d'implémentation

Plusieurs approches peuvent être utilisées pour fusionner les données provenant de votre système avec la structure retournée par FRW119.

Par exemple :

- génération programmatique du JSON;
- moteur de gabarits Mustache permettant le remplacement de variables avec la syntaxe `mustache`;
- https://github.com/Handlebars-Net/Handlebars.Net;
- https://github.com/anisite/YamlHttpClient, qui permet d'appeler une API par configuration YAML et de remplacer automatiquement les variables.

Vous pouvez communiquer avec nous si vous souhaitez en savoir plus.

Le choix de la technologie utilisée demeure à la discrétion du système intégrateur.

## Création versus modification

Certaines informations peuvent être prises en compte seulement au moment de la création du formulaire. D'autres peuvent également être modifiées lors de la reprise (reprise authentifiée seulement).

Le tableau suivant résume les possibilités :

| Type d'information pré-remplie | Création | Reprise |
|----------|----------|----------|
| Champs de formulaire (`form`) | ✔ | |
| Champs de formulaire protégés (`formProtege`) | ✔ | ✔ |
| Propriétés personnalisées | ✔ | ✔ |
| Informations supplémentaires | ✔ | |
| Domaines de valeurs personnalisés | ✔ | ✔ |

## Pré-remplissage anonyme

> À partir de la version `2025.10`

Le pré-remplissage est maintenant disponible pour les formulaires anonymes. Toutefois, vous devez préalablement autoriser les champs concernés dans la configuration `form.yml` de votre formulaire ou de votre système autorisé.

> Important :
>
> - Ne pas autoriser le pré-remplissage de données sensibles.
> - Le système prend en charge des données de pré-remplissage d'une longueur maximale d'environ 1 000 caractères.

Pour plus de détails, voir la section [Personnalisation des formulaires - Concepts de base](https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=personnalisationBase) du P700.

### Formulaire de préremplissage

> Disponible à partir de la release [2026.x](https://github.com/MTESSDev/FRW/releases)

Plutôt que de construire le lien de pré-remplissage dans un système, un formulaire anonyme peut offrir son propre **formulaire de préremplissage**. Une personne (ex. un agent) y saisit une partie des champs du formulaire, puis obtient un lien. Ce lien peut être donné à n'importe qui : la personne qui l'ouvre débute le formulaire avec ces informations déjà inscrites.

Le formulaire de préremplissage est accessible à l'adresse suivante :

`{Adresse du site FRW}/{langue}/Form/{No Systeme Autorisé}/{Type Formulaire}/0/P`

Aucune instance de formulaire ni aucune session n'est créée par le formulaire de préremplissage.

#### Configuration

Le formulaire de préremplissage se définit dans la section racine `formPreremplissage` du fichier `form.yml`, au même niveau que `form:`. La présence de la section active le préremplissage. Ses composants ont la même structure que ceux du formulaire.

```yaml
form:
  sectionsGroup:
    - sections:
        - id: infos
          components:
            - name: nom
              type: text
              label:
                fr: Nom
            - name: courrielAgent        # déclaré dans le formulaire, caché
              type: hidden

formPreremplissage:
  title:                                 # titre de la page (le titre du formulaire ne change pas)
    fr: Générer un lien prérempli
  lienDirect: false                      # optionnel (faux par défaut)
  exigerPreremplissage: true             # optionnel (vrai par défaut)
  components:
    - name: nom                          # hérite de tout du composant du formulaire
      validations:
        optional:                        # facultatif dans le préremplissage seulement
    - name: courrielAgent                # caché dans le formulaire : type et label obligatoires ici
      type: email
      label:
        fr: Courriel de l'agent
```

| Propriété | Description |
|----------|-------------|
| `title` | Titre de la page de préremplissage. À défaut, un titre générique piloté au niveau du système est utilisé, puis sinon (si non piloté), le titre du formulaire. <!-- preremplissage.titrePage -->|
| `components` | Composants à saisir dans le formulaire de préremplissage (obligatoire, au moins un). |
| `exigerPreremplissage` | Vrai par défaut. Le formulaire ne peut alors être débuté qu'à partir d'un lien prérempli. Mettre à `false` pour que le formulaire reste ouvrable normalement. |
| `lienDirect` | Faux par défaut. Voir [Le lien généré](#le-lien-généré). |

Les règles suivantes s'appliquent aux composants du `formPreremplissage` :

- `name` est le nom du composant dans le formulaire, `prefixId` inclus. Un composant groupe est repris en entier; un champ à l'intérieur d'un groupe ne peut pas être déclaré seul.
- Chaque composant est fusionné avec le composant du même nom dans le formulaire : les propriétés déclarées dans `formPreremplissage` l'emportent (ex. `validations` remplace toutes les validations du composant). Le formulaire lui-même n'est pas modifié.
- Un champ `hidden` du formulaire doit préciser un `type` **et** un `label` dans `formPreremplissage`, sans quoi il ne peut pas être affiché.
- Un champ qui ne sert qu'à porter une donnée, sans être affiché dans le formulaire, doit y être déclaré `type: hidden`.
- Les `v-if` et `requisSi` du composant du formulaire ne sont pas repris (ils dépendent de champs absents du préremplissage), sauf s'ils sont redéclarés.
- Un composant sans `name` (affichage seulement, ex. `dynamic`, `avis`) est repris tel quel.
- Un champ est obligatoire par défaut. Utiliser `validations: optional:` pour le rendre facultatif.
- Un `name` ne peut pas être déclaré plus d'une fois.

Les champs déclarés dans `formPreremplissage` sont **autorisés automatiquement** pour le pré-remplissage anonyme : il n'est pas nécessaire de les ajouter à la liste `securite.whitelistPreremplissageAnonyme`. Pour un champ `nom`, les chemins `form.nom` et `form.nom.*` sont autorisés.

<!-- 

Note pour les admins FRW : Les textes de l'interface (`preremplissage.titrePage`, `boutonGenerer`, `titreLien`, `texteLien`, `libelleLien`, `boutonCopier`) sont des textes pilotables : ils peuvent être surchargés dans la section racine `textes`. 

-->

#### Le lien généré

Lorsque la personne clique sur `Générer le lien`, le formulaire est validé. Si tout est correct, les données saisies sont encodées en base 64 et un lien est affiché dans une fenêtre, avec un bouton pour le copier.

- **Par défaut**, le lien pointe vers la page de départ du formulaire :
  `{Adresse du site FRW}/{langue}/DebuterFormulaire/{No Systeme Autorisé}/{Type Formulaire}?donnees={Préremplissage}`
  L'instance n'est créée qu'au clic sur `Commencer`, et non à chaque ouverture du lien (aperçus de liens, analyse des liens par les antivirus de courriel).
- **Avec `lienDirect: true`**, le lien ouvre directement le formulaire :
  `{Adresse du site FRW}/{langue}/Form/{No Systeme Autorisé}/{Type Formulaire}/0/N?donnees={Préremplissage}`
  Chaque ouverture du lien crée alors une instance.

#### Exiger le pré-remplissage

Par défaut (`exigerPreremplissage` vrai), un formulaire qui a une section `formPreremplissage` ne peut être débuté qu'à partir d'un lien prérempli. Si le paramètre `donnees` est absent, invalide, vide ou ne contient que des propriétés non autorisées, l'utilisateur est redirigé vers la page de session invalide.

> Attention : ajouter `formPreremplissage` à un formulaire existant sans mettre `exigerPreremplissage: false` empêche de le débuter sans lien prérempli.

#### Conditions et erreurs

Le formulaire de préremplissage n'est disponible que si l'accès anonyme (`securite:AccesAnonyme`) est activé pour le formulaire et si l'intégration en iframe est autorisée; sinon, ou si la section `formPreremplissage` est absente, l'utilisateur est redirigé vers la page de session invalide.

Une configuration invalide produit une erreur 500 qui détaille les problèmes détectés, par exemple :

- un composant qui n'est pas un objet, ou une section sans composants;
- un `name` absent du formulaire;
- un `name` déclaré plus d'une fois;
- un champ `hidden` du formulaire sans `type` ni `label` dans `formPreremplissage`.

> Important : les mêmes restrictions que le pré-remplissage anonyme s'appliquent. Ne pas faire saisir ni autoriser de données sensibles, et la longueur des données est limitée à environ 1 000 caractères.
