# Schéma de erreurTechnique

```txt
https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique
```

Paramètres du message d'erreur technique.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de erreurTechnique

`object` ([erreurTechnique](frw-definitions-messages-properties-erreurtechnique.md))

# Propriétés de erreurTechnique

| Propriété       | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                               |
| :-------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [titre](#titre) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique/properties/titre") |
| [corps](#corps) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique/properties/corps") |

## titre

Multilingue

`titre`

*   est optionnel

*   ne peut être nul

### Type de titre

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de titre

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## corps

Multilingue

`corps`

*   est optionnel

*   ne peut être nul

### Type de corps

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de corps

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
