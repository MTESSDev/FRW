# Schéma de Section Group

```txt
https://example.com/schemas/custom#/definitions/SectionsGroup
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de SectionsGroup

`object` ([Section Group](frw-definitions-section-group.md))

# Propriétés de SectionsGroup

| Propriété                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :---------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sections](#sections)         | `array`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-sections.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sections") |
| [prefixId](#prefixid)         | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-prefixid.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/prefixId") |
| [classes](#classes)           | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-classes.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/classes")   |
| [v-if](#v-if)                 | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-v-if.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/v-if")         |
| [sectionGroup](#sectiongroup) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sectionGroup")                   |

## sections



`sections`

*   est optionnel

*   Type: `object[]` ([Section](frw-definitions-section.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-section-group-properties-sections.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sections")

### Type de sections

`object[]` ([Section](frw-definitions-section.md))

## prefixId



`prefixId`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-section-group-properties-prefixid.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/prefixId")

### Type de prefixId

`string`

## classes



`classes`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-section-group-properties-classes.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/classes")

### Type de classes

`string`

## v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-section-group-properties-v-if.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/v-if")

### Type de v-if

`string`

## sectionGroup

Multilingue

`sectionGroup`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sectionGroup")

### Type de sectionGroup

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de sectionGroup

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
