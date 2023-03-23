# Schéma de Translation

```txt
https://example.com/schemas/custom#/definitions/Translation
```

Multilingue

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Valeur par défaut de Translation

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

# Propriétés de Translation

| Propriété                 | Type     | Obligatoire | Nullable      | Défini par                                                                                                                                  |
| :------------------------ | :------- | :---------- | :------------ | :------------------------------------------------------------------------------------------------------------------------------------------ |
| [fr](#fr)                 | `string` | Obligatoire | peut être nul | [Schéma sans nom](frw-definitions-translation-properties-fr.md "https://example.com/schemas/custom#/definitions/Translation/properties/fr") |
| [en](#en)                 | `string` | Optionnel   | peut être nul | [Schéma sans nom](frw-definitions-translation-properties-en.md "https://example.com/schemas/custom#/definitions/Translation/properties/en") |
| Propriétés Additionnelles | Any      | Optionnel   | can be null   |                                                                                                                                             |

## fr

Texte de langue française.

`fr`

*   est requis

*   Type: `string` ([fr](frw-definitions-translation-properties-fr.md))

*   peut être nul

## en

Texte de langue anglaise.

`en`

*   est optionnel

*   Type: `string` ([en](frw-definitions-translation-properties-en.md))

*   peut être nul

## Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
