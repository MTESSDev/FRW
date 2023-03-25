## Type de ComposantInteraction

`object` ([Composant interaction](frw-form-definitions-composant-interaction.md))

## Valeur par défaut de ComposantInteraction

La valeur par défaut est:

```yaml
type: radio

```

## Exemple de ComposantInteraction

```yaml
validations

```

# Propriétés de ComposantInteraction

| Propriété                                   | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                   |
| :------------------------------------------ | :-------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                               | `string`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-name.md "schemas/form#/definitions/ComposantInteraction/properties/name")                         |
| [type](#type)                               | `string`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-type.md "schemas/form#/definitions/ComposantInteraction/properties/type")                         |
| [value](#value)                             | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-value.md "schemas/form#/definitions/ComposantInteraction/properties/value")                       |
| [limit](#limit)                             | `number`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-limit.md "schemas/form#/definitions/ComposantInteraction/properties/limit")                       |
| [validation-name](#validation-name)         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/validation-name")                                         |
| [validation-messages](#validation-messages) | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-messages-de-validation.md "schemas/form#/definitions/ComposantInteraction/properties/validation-messages")                         |
| [label](#label)                             | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/label")                                                   |
| [placeholder](#placeholder)                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/placeholder")                                             |
| [inputClasses](#inputclasses)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-inputclasses.md "schemas/form#/definitions/ComposantInteraction/properties/inputClasses")         |
| [inputmode](#inputmode)                     | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-inputmode.md "schemas/form#/definitions/ComposantInteraction/properties/inputmode")               |
| [pattern](#pattern)                         | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-pattern.md "schemas/form#/definitions/ComposantInteraction/properties/pattern")                   |
| [outerClasses](#outerclasses)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-outerclasses.md "schemas/form#/definitions/ComposantInteraction/properties/outerClasses")         |
| [help](#help)                               | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/help")                                                    |
| [pdfBind](#pdfbind)                         | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-pdfbind.md "schemas/form#/definitions/ComposantInteraction/properties/pdfBind")                   |
| [additionals](#additionals)                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-additionals.md "schemas/form#/definitions/ComposantInteraction/properties/additionals")           |
| [v-if](#v-if)                               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-v-if.md "schemas/form#/definitions/ComposantInteraction/properties/v-if")                         |
| [v-else-value](#v-else-value)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-v-else-value.md "schemas/form#/definitions/ComposantInteraction/properties/v-else-value")         |
| [helpPosition](#helpposition)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-helpposition.md "schemas/form#/definitions/ComposantInteraction/properties/helpPosition")         |
| [min](#min)                                 | Plusieurs | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-min.md "schemas/form#/definitions/ComposantInteraction/properties/min")                           |
| [max](#max)                                 | Plusieurs | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-max.md "schemas/form#/definitions/ComposantInteraction/properties/max")                           |
| [addLabel](#addlabel)                       | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/addLabel")                                                |
| [removeLabel](#removelabel)                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/removeLabel")                                             |
| [instanceLabel](#instancelabel)             | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/instanceLabel")                                           |
| [tooltip](#tooltip)                         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-infobulle.md "schemas/form#/definitions/ComposantInteraction/properties/tooltip")                                                  |
| [options](#options)                         | Plusieurs | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-options.md "schemas/form#/definitions/ComposantInteraction/properties/options")                   |
| [nomDocument](#nomdocument)                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/nomDocument")                                             |
| [afficherBlocCode](#afficherbloccode)       | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-afficherbloccode.md "schemas/form#/definitions/ComposantInteraction/properties/afficherBlocCode") |
| [validations](#validations)                 | `object`  | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation.md "schemas/form#/definitions/ComposantInteraction/properties/validations")            |
| [repeatable](#repeatable)                   | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-repeatable.md "schemas/form#/definitions/ComposantInteraction/properties/repeatable")             |
| [minimum](#minimum)                         | `number`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-minimum.md "schemas/form#/definitions/ComposantInteraction/properties/minimum")                   |
| [components](#components)                   | `array`   | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-components.md "schemas/form#/definitions/ComposantInteraction/properties/components")             |
| [disabled](#disabled)                       | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-disabled.md "schemas/form#/definitions/ComposantInteraction/properties/disabled")                 |

## name

Adds a name attribute, and when used with <FormulateForm> this is the key of the field. If no name is defined a random hash will be assigned

`name`

*   est requis

*   ne peut être nul

### Type de name

`string`

## type

Required. The type of input element. See the input library for a full range of options.

> **test**

`type`

*   est requis

*   ne peut être nul

### Type de type

`string`

### Contraintes de type

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                   | Explication                |
| :----------------------- | :------------------------- |
| `"listeDeroulante"`      |                            |
| `"text"`                 | Champ texte                |
| `"codePostal"`           |                            |
| `"cp12"`                 |                            |
| `"nam"`                  | Numéro d'assurance maladie |
| `"nas"`                  |                            |
| `"montant"`              |                            |
| `"adresse"`              |                            |
| `"button"`               |                            |
| `"submit"`               |                            |
| `"customfile"`           |                            |
| `"customfileUlterieure"` |                            |
| `"file"`                 |                            |
| `"group"`                |                            |
| `"repeatableGroup"`      |                            |
| `"radio"`                |                            |
| `"checkbox"`             |                            |
| `"select"`               |                            |
| `"number"`               |                            |
| `"range"`                |                            |
| `"textarea"`             |                            |
| `"color"`                |                            |
| `"date"`                 |                            |
| `"datetime-local"`       |                            |
| `"email"`                |                            |
| `"hidden"`               |                            |
| `"month"`                |                            |
| `"password"`             |                            |
| `"search"`               |                            |
| `"tel"`                  |                            |
| `"time"`                 |                            |
| `"url"`                  |                            |
| `"week"`                 |                            |

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

Textes multilingue (fr et en supportés seulement)

`validation-name`

*   est optionnel

*   ne peut être nul

### Type de validation-name

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Messages de validation](frw-form-definitions-messages-de-validation.md))

## label

Textes multilingue (fr et en supportés seulement)

`label`

*   est optionnel

*   ne peut être nul

### Type de label

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de label

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## placeholder

Textes multilingue (fr et en supportés seulement)

`placeholder`

*   est optionnel

*   ne peut être nul

### Type de placeholder

`object` ([Traduction](frw-form-definitions-traduction.md))

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

Textes multilingue (fr et en supportés seulement)

`help`

*   est optionnel

*   ne peut être nul

### Type de help

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Détails](frw-form-definitions-composant-interaction-properties-additionals.md))

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

l'un des éléments suivants :`string` ou `number` ([Détails](frw-form-definitions-composant-interaction-properties-min.md))

## max



`max`

*   est optionnel

*   ne peut être nul

### Type de max

l'un des éléments suivants :`string` ou `number` ([Détails](frw-form-definitions-composant-interaction-properties-max.md))

## addLabel

Textes multilingue (fr et en supportés seulement)

`addLabel`

*   est optionnel

*   ne peut être nul

### Type de addLabel

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de addLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## removeLabel

Textes multilingue (fr et en supportés seulement)

`removeLabel`

*   est optionnel

*   ne peut être nul

### Type de removeLabel

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de removeLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## instanceLabel

Textes multilingue (fr et en supportés seulement)

`instanceLabel`

*   est optionnel

*   ne peut être nul

### Type de instanceLabel

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Infobulle](frw-form-definitions-infobulle.md))

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

l'un des éléments suivants :`object` ou `string` ou `array` ([Détails](frw-form-definitions-composant-interaction-properties-options.md))

### Exemple de options

```yaml
yesno

```

## nomDocument

Textes multilingue (fr et en supportés seulement)

`nomDocument`

*   est optionnel

*   ne peut être nul

### Type de nomDocument

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`boolean` ([afficherBlocCode](frw-form-definitions-composant-interaction-properties-afficherbloccode.md))

## validations



`validations`

*   est optionnel

*   peut être nul

### Type de validations

`object` ([Validation](frw-form-definitions-composant-interaction-properties-validation.md))

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

`object[]` ([Détails](frw-form-definitions-component.md))

## disabled



`disabled`

*   est optionnel

*   ne peut être nul

### Type de disabled

`boolean`
