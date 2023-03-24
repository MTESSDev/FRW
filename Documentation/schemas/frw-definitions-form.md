## Type de Form

`object` ([Form](frw-definitions-form.md))

# Propriétés de Form

| Propriété                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                   |
| :------------------------------------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------- |
| [sectionsGroup](#sectionsgroup)             | `array`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-form-properties-sectionsgroup.md "schemas/form#/definitions/Form/properties/sectionsGroup")             |
| [templates](#templates)                     | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-form-properties-templates.md "schemas/form#/definitions/Form/properties/templates")                     |
| [title](#title)                             | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-translation.md "schemas/form#/definitions/Form/properties/title")                                       |
| [inputDefaultClasses](#inputdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-form-properties-inputdefaultclasses.md "schemas/form#/definitions/Form/properties/inputDefaultClasses") |
| [defaults](#defaults)                       | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-defaults-values.md "schemas/form#/definitions/Form/properties/defaults")                                |
| [outerDefaultClasses](#outerdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-form-properties-outerdefaultclasses.md "schemas/form#/definitions/Form/properties/outerDefaultClasses") |

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
