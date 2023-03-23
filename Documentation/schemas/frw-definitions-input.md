## Type de Input

`object` ([Input](frw-definitions-input.md))

## Valeur par défaut de Input

La valeur par défaut est:

```yaml
type: radio
validations:
  required: trim

```

## Exemple de Input

```yaml
validations

```

# Propriétés de Input

| Propriété                                   | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :------------------------------------------ | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                               | `string`  | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-name.md "https://example.com/schemas/custom#/definitions/Input/properties/name")                         |
| [type](#type)                               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-type.md "https://example.com/schemas/custom#/definitions/Input/properties/type")                         |
| [value](#value)                             | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-value.md "https://example.com/schemas/custom#/definitions/Input/properties/value")                       |
| [limit](#limit)                             | `number`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-limit.md "https://example.com/schemas/custom#/definitions/Input/properties/limit")                       |
| [validation-name](#validation-name)         | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-name")                        |
| [validation-messages](#validation-messages) | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-validationmessages.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-messages")             |
| [label](#label)                             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/label")                                  |
| [placeholder](#placeholder)                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/placeholder")                            |
| [inputClasses](#inputclasses)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-inputclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/inputClasses")         |
| [inputmode](#inputmode)                     | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-inputmode.md "https://example.com/schemas/custom#/definitions/Input/properties/inputmode")               |
| [pattern](#pattern)                         | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-pattern.md "https://example.com/schemas/custom#/definitions/Input/properties/pattern")                   |
| [outerClasses](#outerclasses)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-outerclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/outerClasses")         |
| [help](#help)                               | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/help")                                   |
| [pdfBind](#pdfbind)                         | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-pdfbind.md "https://example.com/schemas/custom#/definitions/Input/properties/pdfBind")                   |
| [additionals](#additionals)                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-additionals.md "https://example.com/schemas/custom#/definitions/Input/properties/additionals")           |
| [v-if](#v-if)                               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-v-if.md "https://example.com/schemas/custom#/definitions/Input/properties/v-if")                         |
| [v-else-value](#v-else-value)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-v-else-value.md "https://example.com/schemas/custom#/definitions/Input/properties/v-else-value")         |
| [helpPosition](#helpposition)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-helpposition.md "https://example.com/schemas/custom#/definitions/Input/properties/helpPosition")         |
| [min](#min)                                 | Plusieurs | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/min")                           |
| [max](#max)                                 | Plusieurs | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/max")                           |
| [addLabel](#addlabel)                       | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/addLabel")                               |
| [removeLabel](#removelabel)                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/removeLabel")                            |
| [instanceLabel](#instancelabel)             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/instanceLabel")                          |
| [tooltip](#tooltip)                         | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation-1.md "https://example.com/schemas/custom#/definitions/Input/properties/tooltip")                              |
| [options](#options)                         | Plusieurs | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-options.md "https://example.com/schemas/custom#/definitions/Input/properties/options")                   |
| [nomDocument](#nomdocument)                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/nomDocument")                            |
| [afficherBlocCode](#afficherbloccode)       | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Input/properties/afficherBlocCode") |
| [validations](#validations)                 | `object`  | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation.md "https://example.com/schemas/custom#/definitions/Input/properties/validations")            |
| [repeatable](#repeatable)                   | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-repeatable.md "https://example.com/schemas/custom#/definitions/Input/properties/repeatable")             |
| [minimum](#minimum)                         | `number`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-minimum.md "https://example.com/schemas/custom#/definitions/Input/properties/minimum")                   |
| [components](#components)                   | `array`   | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-components.md "https://example.com/schemas/custom#/definitions/Input/properties/components")             |
| [disabled](#disabled)                       | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-disabled.md "https://example.com/schemas/custom#/definitions/Input/properties/disabled")                 |

## name

Adds a name attribute, and when used with <FormulateForm> this is the key of the field. If no name is defined a random hash will be assigned

`name`

*   est requis

*   ne peut être nul

### Type de name

`string`

## type

Required. The type of input element. See the input library for a full range of options.

`type`

*   est optionnel

*   ne peut être nul

### Type de type

`string`

### Contraintes de type

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                   | Explication |
| :----------------------- | :---------- |
| `"listeDeroulante"`      |             |
| `"text"`                 |             |
| `"codePostal"`           |             |
| `"cp12"`                 |             |
| `"nam"`                  |             |
| `"nas"`                  |             |
| `"montant"`              |             |
| `"adresse"`              |             |
| `"button"`               |             |
| `"submit"`               |             |
| `"customfile"`           |             |
| `"customfileUlterieure"` |             |
| `"file"`                 |             |
| `"group"`                |             |
| `"repeatableGroup"`      |             |
| `"radio"`                |             |
| `"checkbox"`             |             |
| `"select"`               |             |
| `"number"`               |             |
| `"range"`                |             |
| `"textarea"`             |             |
| `"color"`                |             |
| `"date"`                 |             |
| `"datetime-local"`       |             |
| `"email"`                |             |
| `"hidden"`               |             |
| `"month"`                |             |
| `"password"`             |             |
| `"search"`               |             |
| `"tel"`                  |             |
| `"time"`                 |             |
| `"url"`                  |             |
| `"week"`                 |             |

### Valeur par défaut de type

La valeur par défaut est:

```yaml
text

```

## value



`value`

*   est optionnel

*   ne peut être nul

### Type de value

`string`

## limit



`limit`

*   est optionnel

*   ne peut être nul

### Type de limit

`number`

## validation-name

Multilingue

`validation-name`

*   est optionnel

*   ne peut être nul

### Type de validation-name

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de validation-name

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## validation-messages



`validation-messages`

*   est optionnel

*   ne peut être nul

### Type de validation-messages

`object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-validationmessages.md))

## label

Multilingue

`label`

*   est optionnel

*   ne peut être nul

### Type de label

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de label

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## placeholder

Multilingue

`placeholder`

*   est optionnel

*   ne peut être nul

### Type de placeholder

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de placeholder

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## inputClasses



`inputClasses`

*   est optionnel

*   ne peut être nul

### Type de inputClasses

`string`

## inputmode

Text field inputmode (html)

`inputmode`

*   est optionnel

*   ne peut être nul

### Type de inputmode

`string`

### Contraintes de inputmode

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur     | Explication |
| :--------- | :---------- |
| `"number"` |             |

## pattern

Regex pattern (html)

`pattern`

*   est optionnel

*   ne peut être nul

### Type de pattern

`string`

## outerClasses



`outerClasses`

*   est optionnel

*   ne peut être nul

### Type de outerClasses

`string`

## help

Multilingue

`help`

*   est optionnel

*   ne peut être nul

### Type de help

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de help

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## pdfBind



`pdfBind`

*   est optionnel

*   ne peut être nul

### Type de pdfBind

`string`

## additionals



`additionals`

*   est optionnel

*   ne peut être nul

### Type de additionals

`object` ([Détails](frw-definitions-input-properties-additionals.md))

## v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

### Type de v-if

`string`

## v-else-value

Valeur de remplacement lorsque le v-if n'affiche pas le champ. Supporté CÔTÉ SERVEUR UNIQUEMENT.

`v-else-value`

*   est optionnel

*   ne peut être nul

### Type de v-else-value

`string`

## helpPosition



`helpPosition`

*   est optionnel

*   ne peut être nul

### Type de helpPosition

`string`

### Contraintes de helpPosition

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur     | Explication |
| :--------- | :---------- |
| `"before"` |             |
| `"after"`  |             |

## min



`min`

*   est optionnel

*   ne peut être nul

### Type de min

l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-min.md))

## max



`max`

*   est optionnel

*   ne peut être nul

### Type de max

l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-max.md))

## addLabel

Multilingue

`addLabel`

*   est optionnel

*   ne peut être nul

### Type de addLabel

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de addLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## removeLabel

Multilingue

`removeLabel`

*   est optionnel

*   ne peut être nul

### Type de removeLabel

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de removeLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## instanceLabel

Multilingue

`instanceLabel`

*   est optionnel

*   ne peut être nul

### Type de instanceLabel

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de instanceLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## tooltip



`tooltip`

*   est optionnel

*   ne peut être nul

### Type de tooltip

`object` ([Translation](frw-definitions-translation-1.md))

### Valeur par défaut de tooltip

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## options

Array or object of options (select or box classifications)

`options`

*   est optionnel

*   peut être nul

### Type de options

l'un des éléments suivants :`object` ou `string` ou `array` ([Détails](frw-definitions-input-properties-options.md))

### Exemple de options

```yaml
yesno

```

## nomDocument

Multilingue

`nomDocument`

*   est optionnel

*   ne peut être nul

### Type de nomDocument

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de nomDocument

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   est optionnel

*   ne peut être nul

### Type de afficherBlocCode

`boolean` ([afficherBlocCode](frw-definitions-input-properties-afficherbloccode.md))

## validations



`validations`

*   est optionnel

*   peut être nul

### Type de validations

`object` ([Validation](frw-definitions-input-properties-validation.md))

### Valeur par défaut de validations

La valeur par défaut est:

```yaml
{}

```

## repeatable



`repeatable`

*   est optionnel

*   ne peut être nul

### Type de repeatable

`boolean`

## minimum



`minimum`

*   est optionnel

*   ne peut être nul

### Type de minimum

`number`

## components



`components`

*   est optionnel

*   ne peut être nul

### Type de components

an array of merged types ([Détails](frw-definitions-input-properties-components-items.md))

## disabled



`disabled`

*   est optionnel

*   ne peut être nul

### Type de disabled

`boolean`
