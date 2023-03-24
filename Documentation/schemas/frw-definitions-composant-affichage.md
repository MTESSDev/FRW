## Type de ComposantAffichage

`object` ([Composant affichage](frw-definitions-composant-affichage.md))

## Valeur par défaut de ComposantAffichage

La valeur par défaut est:

```yaml
type: dynamic

```

# Propriétés de ComposantAffichage

| Propriété                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                          |
| :------------------------------------ | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [type](#type)                         | `string`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-definitions-composant-affichage-properties-type.md "schemas/form#/definitions/ComposantAffichage/properties/type")                         |
| [classes](#classes)                   | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-composant-affichage-properties-classes.md "schemas/form#/definitions/ComposantAffichage/properties/classes")                   |
| [afficherBlocCode](#afficherbloccode) | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-composant-affichage-properties-afficherbloccode.md "schemas/form#/definitions/ComposantAffichage/properties/afficherBlocCode") |
| [tag](#tag)                           | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-composant-affichage-properties-tag.md "schemas/form#/definitions/ComposantAffichage/properties/tag")                           |
| [src](#src)                           | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/src")                                                   |
| [base64](#base64)                     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/base64")                                                |
| [text](#text)                         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/text")                                                  |
| [title](#title)                       | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/title")                                                 |
| [additionals](#additionals)           | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-composant-affichage-properties-additionals.md "schemas/form#/definitions/ComposantAffichage/properties/additionals")           |
| [alt](#alt)                           | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/alt")                                                   |
| [v-if](#v-if)                         | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-composant-affichage-properties-v-if.md "schemas/form#/definitions/ComposantAffichage/properties/v-if")                         |
| [components](#components)             | `array`   | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-composant-affichage-properties-components.md "schemas/form#/definitions/ComposantAffichage/properties/components")             |

## type

Types from custom templates list.

`type`

*   est requis

*   ne peut être nul

### Type de type

`string`

### Contraintes de type

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                   | Explication |
| :----------------------- | :---------- |
| `"inline"`               |             |
| `"dynamic"`              |             |
| `"bandeau"`              |             |
| `"bandeau-notification"` |             |
| `"image"`                |             |
| `"avis"`                 |             |
| `"accordeon"`            |             |

### Exemple de type

```yaml
inline

```

```yaml
dynamic

```

```yaml
bandeau

```

```yaml
bandeau-notification

```

```yaml
image

```

```yaml
avis

```

```yaml
accordeon

```

## classes



`classes`

*   est optionnel

*   ne peut être nul

### Type de classes

`string`

## afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   est optionnel

*   ne peut être nul

### Type de afficherBlocCode

`boolean` ([afficherBlocCode](frw-definitions-composant-affichage-properties-afficherbloccode.md))

## tag



`tag`

*   est optionnel

*   ne peut être nul

### Type de tag

`string`

## src

Textes multilingue (fr et en supportés seulement)

`src`

*   est optionnel

*   ne peut être nul

### Type de src

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de src

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## base64

Textes multilingue (fr et en supportés seulement)

`base64`

*   est optionnel

*   ne peut être nul

### Type de base64

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de base64

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## text

Textes multilingue (fr et en supportés seulement)

`text`

*   est optionnel

*   ne peut être nul

### Type de text

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de text

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## title

Textes multilingue (fr et en supportés seulement)

`title`

*   est optionnel

*   ne peut être nul

### Type de title

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## additionals



`additionals`

*   est optionnel

*   ne peut être nul

### Type de additionals

`object` ([Détails](frw-definitions-composant-affichage-properties-additionals.md))

## alt

Textes multilingue (fr et en supportés seulement)

`alt`

*   est optionnel

*   ne peut être nul

### Type de alt

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de alt

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

### Type de v-if

`string`

## components



`components`

*   est optionnel

*   ne peut être nul

### Type de components

`object[]` ([Détails](frw-definitions-component.md))
