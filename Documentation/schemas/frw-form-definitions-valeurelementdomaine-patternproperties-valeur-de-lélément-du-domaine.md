## Type de ^\[a-zA-Z0-9]+$

`object` ([Valeur de l'élément du domaine](frw-form-definitions-valeurelementdomaine-patternproperties-valeur-de-lélément-du-domaine.md))

## Contraintes de ^\[a-zA-Z0-9]+$

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

# Propriétés de ^\[a-zA-Z0-9]+$

| Propriété               | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                                            |
| :---------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [label](#label)         | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ValeurElementDomaine/patternProperties/^\[a-zA-Z0-9]+$/properties/label")                                                                          |
| [mots-cles](#mots-cles) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ValeurElementDomaine/patternProperties/^\[a-zA-Z0-9]+$/properties/mots-cles")                                                                      |
| [v-if](#v-if)           | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-valeurelementdomaine-patternproperties-valeur-de-lélément-du-domaine-properties-v-if.md "schemas/form#/definitions/ValeurElementDomaine/patternProperties/^\[a-zA-Z0-9]+$/properties/v-if") |

## label

Textes multilingue (fr et en supportés seulement)

`label`

*   est optionnel

*   ne peut être nul

### Type de label

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de label

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## mots-cles

Textes multilingue (fr et en supportés seulement)

`mots-cles`

*   est optionnel

*   ne peut être nul

### Type de mots-cles

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de mots-cles

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

### Type de v-if

`string`
