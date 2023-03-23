# Schéma de Section

```txt
https://example.com/schemas/custom#/definitions/Section
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de Section

| Propriété                                                                           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                    |
| :---------------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [section](#section)                                                                 | `object`  | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Section/properties/section")                                                                                |
| [id](#id)                                                                           | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-id.md "https://example.com/schemas/custom#/definitions/Section/properties/id")                                                                           |
| [cacherTexteExplicatifChampsObligatoires](#cachertexteexplicatifchampsobligatoires) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "https://example.com/schemas/custom#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires") |
| [classes](#classes)                                                                 | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-classes.md "https://example.com/schemas/custom#/definitions/Section/properties/classes")                                                                 |
| [v-if](#v-if)                                                                       | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-v-if.md "https://example.com/schemas/custom#/definitions/Section/properties/v-if")                                                                       |
| [components](#components)                                                           | `array`   | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-components.md "https://example.com/schemas/custom#/definitions/Section/properties/components")                                                           |

## section

Multilingue

`section`

*   est requis

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

### Valeur par défaut de section

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## id



`id`

*   est optionnel

*   Type: `string`

*   ne peut être nul

## cacherTexteExplicatifChampsObligatoires

Permet d'afficher l'indication de champs obligatoires.

`cacherTexteExplicatifChampsObligatoires`

*   est optionnel

*   Type: `boolean`

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

## components



`components`

*   est optionnel

*   Type: an array of merged types ([Détails](frw-definitions-section-properties-components-items.md))

*   ne peut être nul
