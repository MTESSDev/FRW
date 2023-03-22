# Display Schema

```txt
https://example.com/schemas/custom#/definitions/Display
```

Display component

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Display Type

`object` ([Display](frw-definitions-display.md))

# Display Properties

| Property                              | Type      | Required | Nullable       | Defined by                                                                                                                                                      |
| :------------------------------------ | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [type](#type)                         | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-type.md "https://example.com/schemas/custom#/definitions/Display/properties/type")                         |
| [classes](#classes)                   | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-classes.md "https://example.com/schemas/custom#/definitions/Display/properties/classes")                   |
| [afficherBlocCode](#afficherbloccode) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Display/properties/afficherBlocCode") |
| [tag](#tag)                           | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-tag.md "https://example.com/schemas/custom#/definitions/Display/properties/tag")                           |
| [src](#src)                           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/src")                                      |
| [base64](#base64)                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/base64")                                   |
| [text](#text)                         | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/text")                                     |
| [title](#title)                       | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/title")                                    |
| [additionals](#additionals)           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-additionals.md "https://example.com/schemas/custom#/definitions/Display/properties/additionals")           |
| [alt](#alt)                           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/alt")                                      |
| [v-if](#v-if)                         | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-v-if.md "https://example.com/schemas/custom#/definitions/Display/properties/v-if")                         |
| [components](#components)             | `array`   | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-components.md "https://example.com/schemas/custom#/definitions/Display/properties/components")             |

## type

Types from custom templates list.

`type`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-type.md "https://example.com/schemas/custom#/definitions/Display/properties/type")

### type Type

`string`

### type Examples

```json
"inline"
```

```json
"dynamic"
```

```json
"bandeau"
```

```json
"bandeau-notification"
```

```json
"image"
```

```json
"avis"
```

```json
"accordeon"
```

## classes



`classes`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-classes.md "https://example.com/schemas/custom#/definitions/Display/properties/classes")

### classes Type

`string`

## afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   is optional

*   Type: `boolean` ([afficherBlocCode](frw-definitions-display-properties-afficherbloccode.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Display/properties/afficherBlocCode")

### afficherBlocCode Type

`boolean` ([afficherBlocCode](frw-definitions-display-properties-afficherbloccode.md))

## tag



`tag`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-tag.md "https://example.com/schemas/custom#/definitions/Display/properties/tag")

### tag Type

`string`

## src

Multilingue

`src`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/src")

### src Type

`object` ([Translation](frw-definitions-translation.md))

### src Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## base64

Multilingue

`base64`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/base64")

### base64 Type

`object` ([Translation](frw-definitions-translation.md))

### base64 Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## text

Multilingue

`text`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/text")

### text Type

`object` ([Translation](frw-definitions-translation.md))

### text Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/title")

### title Type

`object` ([Translation](frw-definitions-translation.md))

### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## additionals



`additionals`

*   is optional

*   Type: `object` ([Details](frw-definitions-display-properties-additionals.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-additionals.md "https://example.com/schemas/custom#/definitions/Display/properties/additionals")

### additionals Type

`object` ([Details](frw-definitions-display-properties-additionals.md))

## alt

Multilingue

`alt`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/alt")

### alt Type

`object` ([Translation](frw-definitions-translation.md))

### alt Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-v-if.md "https://example.com/schemas/custom#/definitions/Display/properties/v-if")

### v-if Type

`string`

## components



`components`

*   is optional

*   Type: an array of merged types ([Details](frw-definitions-display-properties-components-items.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-components.md "https://example.com/schemas/custom#/definitions/Display/properties/components")

### components Type

an array of merged types ([Details](frw-definitions-display-properties-components-items.md))
