## Type de erreurTechnique

`object` ([erreurTechnique](frw-definitions-messages-properties-erreurtechnique.md))

# Propriétés de erreurTechnique

| Propriété       | Type     | Obligatoire | Nullable         | Défini par                                                                                                                           |
| :-------------- | :------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------- |
| [titre](#titre) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/Messages/properties/erreurTechnique/properties/titre") |
| [corps](#corps) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/Messages/properties/erreurTechnique/properties/corps") |

## titre

Textes multilingue (fr et en supportés seulement)

`titre`

*   est optionnel

*   ne peut être nul

### Type de titre

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de titre

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## corps

Textes multilingue (fr et en supportés seulement)

`corps`

*   est optionnel

*   ne peut être nul

### Type de corps

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de corps

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
