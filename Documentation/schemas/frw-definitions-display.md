## Type de Display

`object` ([Display](frw-definitions-display.md))

# Propriétés de Display

| Propriété                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                      |
| :------------------------------------ | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [type](#type)                         | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-type.md "https://example.com/schemas/custom#/definitions/Display/properties/type")                         |
| [classes](#classes)                   | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-classes.md "https://example.com/schemas/custom#/definitions/Display/properties/classes")                   |
| [afficherBlocCode](#afficherbloccode) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Display/properties/afficherBlocCode") |
| [tag](#tag)                           | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-tag.md "https://example.com/schemas/custom#/definitions/Display/properties/tag")                           |
| [src](#src)                           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/src")                                      |
| [base64](#base64)                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/base64")                                   |
| [text](#text)                         | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/text")                                     |
| [title](#title)                       | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/title")                                    |
| [additionals](#additionals)           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-additionals.md "https://example.com/schemas/custom#/definitions/Display/properties/additionals")           |
| [alt](#alt)                           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/alt")                                      |
| [v-if](#v-if)                         | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-v-if.md "https://example.com/schemas/custom#/definitions/Display/properties/v-if")                         |
| [components](#components)             | `array`   | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-components.md "https://example.com/schemas/custom#/definitions/Display/properties/components")             |

## type

Types from custom templates list.

`type`

*   est optionnel

*   ne peut être nul

### Type de type

`string`

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

`boolean` ([afficherBlocCode](frw-definitions-display-properties-afficherbloccode.md))

## tag



`tag`

*   est optionnel

*   ne peut être nul

### Type de tag

`string`

## src

Multilingue

`src`

*   est optionnel

*   ne peut être nul

### Type de src

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de src

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## base64

Multilingue

`base64`

*   est optionnel

*   ne peut être nul

### Type de base64

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de base64

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## text

Multilingue

`text`

*   est optionnel

*   ne peut être nul

### Type de text

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de text

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## title

Multilingue

`title`

*   est optionnel

*   ne peut être nul

### Type de title

`object` ([Translation](frw-definitions-translation.md))

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

`object` ([Détails](frw-definitions-display-properties-additionals.md))

## alt

Multilingue

`alt`

*   est optionnel

*   ne peut être nul

### Type de alt

`object` ([Translation](frw-definitions-translation.md))

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

an array of merged types ([Détails](frw-definitions-display-properties-components-items.md))
