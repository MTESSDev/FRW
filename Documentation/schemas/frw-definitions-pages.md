# Schéma de pages

```txt
https://example.com/schemas/custom#/definitions/Pages
```

Paramètres associés à différentes pages.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Pages

`object` ([pages](frw-definitions-pages.md))

# Propriétés de Pages

| Propriété                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                |
| :---------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sessionInvalide](#sessioninvalide) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-pages-properties-sessioninvalide.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide") |

## sessionInvalide

Paramètres associés à la page de session invalide.

`sessionInvalide`

*   est optionnel

*   ne peut être nul

### Type de sessionInvalide

`object` ([sessionInvalide](frw-definitions-pages-properties-sessioninvalide.md))
