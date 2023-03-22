# Section Schema

```txt
https://example.com/schemas/custom#/definitions/Section
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Section Type

`object` ([Section](frw-definitions-section.md))

# Section Properties

| Property                                                                            | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                    |
| :---------------------------------------------------------------------------------- | :-------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [section](#section)                                                                 | `object`  | Required | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Section/properties/section")                                                                                |
| [id](#id)                                                                           | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-id.md "https://example.com/schemas/custom#/definitions/Section/properties/id")                                                                           |
| [cacherTexteExplicatifChampsObligatoires](#cachertexteexplicatifchampsobligatoires) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "https://example.com/schemas/custom#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires") |
| [classes](#classes)                                                                 | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-classes.md "https://example.com/schemas/custom#/definitions/Section/properties/classes")                                                                 |
| [v-if](#v-if)                                                                       | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-v-if.md "https://example.com/schemas/custom#/definitions/Section/properties/v-if")                                                                       |
| [components](#components)                                                           | `array`   | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-components.md "https://example.com/schemas/custom#/definitions/Section/properties/components")                                                           |

## section

Multilingue

`section`

*   is required

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Section/properties/section")

### section Type

`object` ([Translation](frw-definitions-translation.md))

### section Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## id



`id`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-id.md "https://example.com/schemas/custom#/definitions/Section/properties/id")

### id Type

`string`

## cacherTexteExplicatifChampsObligatoires

Permet d'afficher l'indication de champs obligatoires.

`cacherTexteExplicatifChampsObligatoires`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "https://example.com/schemas/custom#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires")

### cacherTexteExplicatifChampsObligatoires Type

`boolean`

## classes



`classes`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-classes.md "https://example.com/schemas/custom#/definitions/Section/properties/classes")

### classes Type

`string`

## v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-v-if.md "https://example.com/schemas/custom#/definitions/Section/properties/v-if")

### v-if Type

`string`

## components



`components`

*   is optional

*   Type: an array of merged types ([Details](frw-definitions-section-properties-components-items.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-components.md "https://example.com/schemas/custom#/definitions/Section/properties/components")

### components Type

an array of merged types ([Details](frw-definitions-section-properties-components-items.md))
