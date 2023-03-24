## Type de SectionsGroup

`object` ([Section Group](frw-definitions-section-group.md))

# Propriétés de SectionsGroup

| Propriété                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                               |
| :---------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------- |
| [sections](#sections)         | `array`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-group-properties-sections.md "schemas/form#/definitions/SectionsGroup/properties/sections") |
| [prefixId](#prefixid)         | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-group-properties-prefixid.md "schemas/form#/definitions/SectionsGroup/properties/prefixId") |
| [classes](#classes)           | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-group-properties-classes.md "schemas/form#/definitions/SectionsGroup/properties/classes")   |
| [v-if](#v-if)                 | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-group-properties-v-if.md "schemas/form#/definitions/SectionsGroup/properties/v-if")         |
| [sectionGroup](#sectiongroup) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-translation.md "schemas/form#/definitions/SectionsGroup/properties/sectionGroup")                   |

## sections



`sections`

*   est optionnel

*   ne peut être nul

### Type de sections

`object[]` ([Section](frw-definitions-section.md))

## prefixId



`prefixId`

*   est optionnel

*   ne peut être nul

### Type de prefixId

`string`

## classes



`classes`

*   est optionnel

*   ne peut être nul

### Type de classes

`string`

## v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

### Type de v-if

`string`

## sectionGroup

Multilingue

`sectionGroup`

*   est optionnel

*   ne peut être nul

### Type de sectionGroup

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de sectionGroup

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
