## Type de Form

`object` ([Form](frw-form-definitions-form.md))

# Propriétés de Form

| Propriété                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                |
| :------------------------------------------ | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sectionsGroup](#sectionsgroup)             | `array`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-groupes-de-sections.md "schemas/form#/definitions/Form/properties/sectionsGroup")               |
| [templates](#templates)                     | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-réservé-frw---templates-de-composants.md "schemas/form#/definitions/Form/properties/templates") |
| [title](#title)                             | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Form/properties/title")                                                |
| [inputDefaultClasses](#inputdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-inputdefaultclasses.md "schemas/form#/definitions/Form/properties/inputDefaultClasses")         |
| [defaults](#defaults)                       | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-valeurs-par-défaut.md "schemas/form#/definitions/Form/properties/defaults")                                     |
| [outerDefaultClasses](#outerdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-outerdefaultclasses.md "schemas/form#/definitions/Form/properties/outerDefaultClasses")         |

## sectionsGroup



`sectionsGroup`

*   est optionnel

*   ne peut être nul

### Type de sectionsGroup

`object[]` ([Section Group](frw-form-definitions-section-group.md))

## templates



`templates`

*   est optionnel

*   ne peut être nul

### Type de templates

`object` ([RÉSERVÉ FRW - Templates de composants](frw-form-definitions-form-properties-réservé-frw---templates-de-composants.md))

### Limites d'accès de templates

La valeur de cette propriété est gérée exclusivement par l'autorité propriétaire, et les tentatives d'une demande de modification de la valeur de cette propriété devraient être ignorées ou rejetées par cette autorité propriétaire.

## title

Textes multilingue (fr et en supportés seulement)

`title`

*   est optionnel

*   ne peut être nul

### Type de title

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Détails](frw-form-definitions-form-properties-inputdefaultclasses.md))

## defaults



`defaults`

*   est optionnel

*   ne peut être nul

### Type de defaults

`object` ([Valeurs par défaut](frw-form-definitions-valeurs-par-défaut.md))

## outerDefaultClasses



`outerDefaultClasses`

*   est optionnel

*   ne peut être nul

### Type de outerDefaultClasses

`object` ([Détails](frw-form-definitions-form-properties-outerdefaultclasses.md))
