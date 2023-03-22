# Section Group Schema

```txt
https://example.com/schemas/custom#/definitions/SectionsGroup
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## SectionsGroup Type

`object` ([Section Group](frw-definitions-section-group.md))

# SectionsGroup Properties

| Property                      | Type     | Required | Nullable       | Defined by                                                                                                                                                  |
| :---------------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sections](#sections)         | `array`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-sections.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sections") |
| [prefixId](#prefixid)         | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-prefixid.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/prefixId") |
| [classes](#classes)           | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-classes.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/classes")   |
| [v-if](#v-if)                 | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-v-if.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/v-if")         |
| [sectionGroup](#sectiongroup) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sectionGroup")                   |

## sections



`sections`

*   is optional

*   Type: `object[]` ([Section](frw-definitions-section.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-sections.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sections")

### sections Type

`object[]` ([Section](frw-definitions-section.md))

## prefixId



`prefixId`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-prefixid.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/prefixId")

### prefixId Type

`string`

## classes



`classes`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-classes.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/classes")

### classes Type

`string`

## v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-v-if.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/v-if")

### v-if Type

`string`

## sectionGroup

Multilingue

`sectionGroup`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sectionGroup")

### sectionGroup Type

`object` ([Translation](frw-definitions-translation.md))

### sectionGroup Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
