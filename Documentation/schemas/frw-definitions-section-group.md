# Schéma de Section Group

```txt
https://example.com/schemas/custom#/definitions/SectionsGroup
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

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

## prefixId



`prefixId`

*   est optionnel

*   Type: `string`

*   ne peut être nul

## classes



`classes`

*   est optionnel

*   Type: `string`

*   ne peut être nul

## v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   Type: `string`

*   ne peut être nul

## sectionGroup

Multilingue

`sectionGroup`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

### Valeur par défaut de sectionGroup

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
