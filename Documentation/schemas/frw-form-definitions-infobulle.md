## Type de Tooltip

`object` ([Infobulle](frw-form-definitions-infobulle.md))

## Valeur par défaut de Tooltip

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

# Propriétés de Tooltip

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                    |
| :------------------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------ |
| [title](#title)           | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Tooltip/properties/title") |
| [text](#text)             | `object` | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Tooltip/properties/text")  |
| Propriétés Additionnelles | Any      | Optionnel   | can be null      |                                                                                                               |

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

## text

Textes multilingue (fr et en supportés seulement)

`text`

*   est requis

*   ne peut être nul

### Type de text

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de text

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
