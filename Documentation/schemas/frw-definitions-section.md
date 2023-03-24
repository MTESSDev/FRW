## Type de Section

`object` ([Section](frw-definitions-section.md))

# Propriétés de Section

| Propriété                                                                           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                 |
| :---------------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [section](#section)                                                                 | `object`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/Section/properties/section")                                                                                 |
| [id](#id)                                                                           | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-properties-id.md "schemas/form#/definitions/Section/properties/id")                                                                           |
| [cacherTexteExplicatifChampsObligatoires](#cachertexteexplicatifchampsobligatoires) | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "schemas/form#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires") |
| [classes](#classes)                                                                 | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-properties-classes.md "schemas/form#/definitions/Section/properties/classes")                                                                 |
| [v-if](#v-if)                                                                       | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-properties-v-if.md "schemas/form#/definitions/Section/properties/v-if")                                                                       |
| [components](#components)                                                           | `array`   | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-section-properties-components.md "schemas/form#/definitions/Section/properties/components")                                                           |

## section

Textes multilingue (fr et en supportés seulement)

`section`

*   est requis

*   ne peut être nul

### Type de section

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de section

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## id



`id`

*   est optionnel

*   ne peut être nul

### Type de id

`string`

## cacherTexteExplicatifChampsObligatoires

Permet d'afficher l'indication de champs obligatoires.

`cacherTexteExplicatifChampsObligatoires`

*   est optionnel

*   ne peut être nul

### Type de cacherTexteExplicatifChampsObligatoires

`boolean`

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

## components



`components`

*   est optionnel

*   ne peut être nul

### Type de components

`object[]` ([Détails](frw-definitions-component.md))
