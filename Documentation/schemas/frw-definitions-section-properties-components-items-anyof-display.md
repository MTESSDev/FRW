# Schéma de Display

```txt
https://example.com/schemas/custom#/definitions/Section/properties/components/items/anyOf/1
```

Display component

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de 1

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

*   Type: `string`

*   ne peut être nul

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

*   Type: `string`

*   ne peut être nul

## afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   est optionnel

*   Type: `boolean` ([afficherBlocCode](frw-definitions-display-properties-afficherbloccode.md))

*   ne peut être nul

## tag



`tag`

*   est optionnel

*   Type: `string`

*   ne peut être nul

## src

Multilingue

`src`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

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

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

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

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

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

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## additionals



`additionals`

*   est optionnel

*   Type: `object` ([Détails](frw-definitions-display-properties-additionals.md))

*   ne peut être nul

## alt

Multilingue

`alt`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

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

*   Type: `string`

*   ne peut être nul

## components



`components`

*   est optionnel

*   Type: an array of merged types ([Détails](frw-definitions-display-properties-components-items.md))

*   ne peut être nul
