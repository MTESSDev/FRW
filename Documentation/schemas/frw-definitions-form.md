# Schéma de Form

```txt
https://example.com/schemas/custom#/definitions/Form
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Form

`object` ([Form](frw-definitions-form.md))

# Propriétés de Form

| Propriété                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                      |
| :------------------------------------------ | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sectionsGroup](#sectionsgroup)             | `array`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-sectionsgroup.md "https://example.com/schemas/custom#/definitions/Form/properties/sectionsGroup")             |
| [templates](#templates)                     | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-templates.md "https://example.com/schemas/custom#/definitions/Form/properties/templates")                     |
| [title](#title)                             | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Form/properties/title")                                       |
| [inputDefaultClasses](#inputdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-inputdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/inputDefaultClasses") |
| [defaults](#defaults)                       | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-defaults-values.md "https://example.com/schemas/custom#/definitions/Form/properties/defaults")                                |
| [outerDefaultClasses](#outerdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-outerdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/outerDefaultClasses") |

## sectionsGroup



`sectionsGroup`

*   est optionnel

*   ne peut être nul

### Type de sectionsGroup

`object[]` ([Section Group](frw-definitions-section-group.md))

## templates



`templates`

*   est optionnel

*   ne peut être nul

### Type de templates

`object` ([Détails](frw-definitions-form-properties-templates.md))

## title

Multilingue

`title`

*   est optionnel

*   ne peut être nul

### Type de title

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## inputDefaultClasses



`inputDefaultClasses`

*   est optionnel

*   ne peut être nul

### Type de inputDefaultClasses

`object` ([Détails](frw-definitions-form-properties-inputdefaultclasses.md))

## defaults



`defaults`

*   est optionnel

*   ne peut être nul

### Type de defaults

`object` ([Defaults values](frw-definitions-defaults-values.md))

## outerDefaultClasses



`outerDefaultClasses`

*   est optionnel

*   ne peut être nul

### Type de outerDefaultClasses

`object` ([Détails](frw-definitions-form-properties-outerdefaultclasses.md))
