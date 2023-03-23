# Schéma de Translation

```txt
https://example.com/schemas/custom#/definitions/Tooltip
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Tooltip

`object` ([Translation](frw-definitions-translation-1.md))

## Valeur par défaut de Tooltip

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

# Propriétés de Tooltip

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                   |
| :------------------------ | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| [title](#title)           | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/title") |
| [text](#text)             | `object` | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/text")  |
| Propriétés Additionnelles | Any      | Optionnel   | can be null      |                                                                                                                              |

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

## text

Multilingue

`text`

*   est requis

*   ne peut être nul

### Type de text

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de text

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
