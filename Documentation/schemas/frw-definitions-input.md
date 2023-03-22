# Input Schema

```txt
https://example.com/schemas/custom#/definitions/Input
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Input Type

`object` ([Input](frw-definitions-input.md))

## Input Default Value

The default value is:

```json
{
  "type": "radio",
  "validations": {
    "required": "trim"
  }
}
```

## Input Examples

```json
"validations"
```

# Input Properties

| Property                                    | Type      | Required | Nullable       | Defined by                                                                                                                                                  |
| :------------------------------------------ | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                               | `string`  | Required | cannot be null | [Untitled schema](frw-definitions-input-properties-name.md "https://example.com/schemas/custom#/definitions/Input/properties/name")                         |
| [type](#type)                               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-type.md "https://example.com/schemas/custom#/definitions/Input/properties/type")                         |
| [value](#value)                             | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-value.md "https://example.com/schemas/custom#/definitions/Input/properties/value")                       |
| [limit](#limit)                             | `number`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-limit.md "https://example.com/schemas/custom#/definitions/Input/properties/limit")                       |
| [validation-name](#validation-name)         | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-name")                        |
| [validation-messages](#validation-messages) | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-validationmessages.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-messages")             |
| [label](#label)                             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/label")                                  |
| [placeholder](#placeholder)                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/placeholder")                            |
| [inputClasses](#inputclasses)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-inputclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/inputClasses")         |
| [inputmode](#inputmode)                     | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-inputmode.md "https://example.com/schemas/custom#/definitions/Input/properties/inputmode")               |
| [pattern](#pattern)                         | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-pattern.md "https://example.com/schemas/custom#/definitions/Input/properties/pattern")                   |
| [outerClasses](#outerclasses)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-outerclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/outerClasses")         |
| [help](#help)                               | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/help")                                   |
| [pdfBind](#pdfbind)                         | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-pdfbind.md "https://example.com/schemas/custom#/definitions/Input/properties/pdfBind")                   |
| [additionals](#additionals)                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-additionals.md "https://example.com/schemas/custom#/definitions/Input/properties/additionals")           |
| [v-if](#v-if)                               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-v-if.md "https://example.com/schemas/custom#/definitions/Input/properties/v-if")                         |
| [v-else-value](#v-else-value)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-v-else-value.md "https://example.com/schemas/custom#/definitions/Input/properties/v-else-value")         |
| [helpPosition](#helpposition)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-helpposition.md "https://example.com/schemas/custom#/definitions/Input/properties/helpPosition")         |
| [min](#min)                                 | Multiple  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/min")                           |
| [max](#max)                                 | Multiple  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/max")                           |
| [addLabel](#addlabel)                       | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/addLabel")                               |
| [removeLabel](#removelabel)                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/removeLabel")                            |
| [instanceLabel](#instancelabel)             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/instanceLabel")                          |
| [tooltip](#tooltip)                         | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation-1.md "https://example.com/schemas/custom#/definitions/Input/properties/tooltip")                              |
| [options](#options)                         | Multiple  | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-options.md "https://example.com/schemas/custom#/definitions/Input/properties/options")                   |
| [nomDocument](#nomdocument)                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/nomDocument")                            |
| [afficherBlocCode](#afficherbloccode)       | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Input/properties/afficherBlocCode") |
| [validations](#validations)                 | `object`  | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation.md "https://example.com/schemas/custom#/definitions/Input/properties/validations")            |
| [repeatable](#repeatable)                   | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-repeatable.md "https://example.com/schemas/custom#/definitions/Input/properties/repeatable")             |
| [minimum](#minimum)                         | `number`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-minimum.md "https://example.com/schemas/custom#/definitions/Input/properties/minimum")                   |
| [components](#components)                   | `array`   | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-components.md "https://example.com/schemas/custom#/definitions/Input/properties/components")             |
| [disabled](#disabled)                       | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-disabled.md "https://example.com/schemas/custom#/definitions/Input/properties/disabled")                 |

## name

Adds a name attribute, and when used with <FormulateForm> this is the key of the field. If no name is defined a random hash will be assigned

`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-name.md "https://example.com/schemas/custom#/definitions/Input/properties/name")

### name Type

`string`

## type

Required. The type of input element. See the input library for a full range of options.

`type`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-type.md "https://example.com/schemas/custom#/definitions/Input/properties/type")

### type Type

`string`

### type Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value                    | Explanation |
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

### type Default Value

The default value is:

```json
"text"
```

## value



`value`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-value.md "https://example.com/schemas/custom#/definitions/Input/properties/value")

### value Type

`string`

## limit



`limit`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-limit.md "https://example.com/schemas/custom#/definitions/Input/properties/limit")

### limit Type

`number`

## validation-name

Multilingue

`validation-name`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-name")

### validation-name Type

`object` ([Translation](frw-definitions-translation.md))

### validation-name Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## validation-messages



`validation-messages`

*   is optional

*   Type: `object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-validationmessages.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-validationmessages.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-messages")

### validation-messages Type

`object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-validationmessages.md))

## label

Multilingue

`label`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/label")

### label Type

`object` ([Translation](frw-definitions-translation.md))

### label Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## placeholder

Multilingue

`placeholder`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/placeholder")

### placeholder Type

`object` ([Translation](frw-definitions-translation.md))

### placeholder Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## inputClasses



`inputClasses`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-inputclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/inputClasses")

### inputClasses Type

`string`

## inputmode

Text field inputmode (html)

`inputmode`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-inputmode.md "https://example.com/schemas/custom#/definitions/Input/properties/inputmode")

### inputmode Type

`string`

### inputmode Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value      | Explanation |
| :--------- | :---------- |
| `"number"` |             |

## pattern

Regex pattern (html)

`pattern`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-pattern.md "https://example.com/schemas/custom#/definitions/Input/properties/pattern")

### pattern Type

`string`

## outerClasses



`outerClasses`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-outerclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/outerClasses")

### outerClasses Type

`string`

## help

Multilingue

`help`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/help")

### help Type

`object` ([Translation](frw-definitions-translation.md))

### help Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## pdfBind



`pdfBind`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-pdfbind.md "https://example.com/schemas/custom#/definitions/Input/properties/pdfBind")

### pdfBind Type

`string`

## additionals



`additionals`

*   is optional

*   Type: `object` ([Details](frw-definitions-input-properties-additionals.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-additionals.md "https://example.com/schemas/custom#/definitions/Input/properties/additionals")

### additionals Type

`object` ([Details](frw-definitions-input-properties-additionals.md))

## v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-v-if.md "https://example.com/schemas/custom#/definitions/Input/properties/v-if")

### v-if Type

`string`

## v-else-value

Valeur de remplacement lorsque le v-if n'affiche pas le champ. Supporté CÔTÉ SERVEUR UNIQUEMENT.

`v-else-value`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-v-else-value.md "https://example.com/schemas/custom#/definitions/Input/properties/v-else-value")

### v-else-value Type

`string`

## helpPosition



`helpPosition`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-helpposition.md "https://example.com/schemas/custom#/definitions/Input/properties/helpPosition")

### helpPosition Type

`string`

### helpPosition Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value      | Explanation |
| :--------- | :---------- |
| `"before"` |             |
| `"after"`  |             |

## min



`min`

*   is optional

*   Type: any of the following: `string` or `number` ([Details](frw-definitions-input-properties-min.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/min")

### min Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-min.md))

## max



`max`

*   is optional

*   Type: any of the following: `string` or `number` ([Details](frw-definitions-input-properties-max.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/max")

### max Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-max.md))

## addLabel

Multilingue

`addLabel`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/addLabel")

### addLabel Type

`object` ([Translation](frw-definitions-translation.md))

### addLabel Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## removeLabel

Multilingue

`removeLabel`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/removeLabel")

### removeLabel Type

`object` ([Translation](frw-definitions-translation.md))

### removeLabel Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## instanceLabel

Multilingue

`instanceLabel`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/instanceLabel")

### instanceLabel Type

`object` ([Translation](frw-definitions-translation.md))

### instanceLabel Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## tooltip



`tooltip`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation-1.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation-1.md "https://example.com/schemas/custom#/definitions/Input/properties/tooltip")

### tooltip Type

`object` ([Translation](frw-definitions-translation-1.md))

### tooltip Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## options

Array or object of options (select or box classifications)

`options`

*   is optional

*   Type: any of the following: `object` or `string` or `array` ([Details](frw-definitions-input-properties-options.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-options.md "https://example.com/schemas/custom#/definitions/Input/properties/options")

### options Type

any of the following: `object` or `string` or `array` ([Details](frw-definitions-input-properties-options.md))

### options Examples

```json
"yesno"
```

## nomDocument

Multilingue

`nomDocument`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/nomDocument")

### nomDocument Type

`object` ([Translation](frw-definitions-translation.md))

### nomDocument Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   is optional

*   Type: `boolean` ([afficherBlocCode](frw-definitions-input-properties-afficherbloccode.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Input/properties/afficherBlocCode")

### afficherBlocCode Type

`boolean` ([afficherBlocCode](frw-definitions-input-properties-afficherbloccode.md))

## validations



`validations`

*   is optional

*   Type: `object` ([Validation](frw-definitions-input-properties-validation.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation.md "https://example.com/schemas/custom#/definitions/Input/properties/validations")

### validations Type

`object` ([Validation](frw-definitions-input-properties-validation.md))

### validations Default Value

The default value is:

```json
{}
```

## repeatable



`repeatable`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-repeatable.md "https://example.com/schemas/custom#/definitions/Input/properties/repeatable")

### repeatable Type

`boolean`

## minimum



`minimum`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-minimum.md "https://example.com/schemas/custom#/definitions/Input/properties/minimum")

### minimum Type

`number`

## components



`components`

*   is optional

*   Type: an array of merged types ([Details](frw-definitions-input-properties-components-items.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-components.md "https://example.com/schemas/custom#/definitions/Input/properties/components")

### components Type

an array of merged types ([Details](frw-definitions-input-properties-components-items.md))

## disabled



`disabled`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-disabled.md "https://example.com/schemas/custom#/definitions/Input/properties/disabled")

### disabled Type

`boolean`
