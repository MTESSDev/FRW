# Schéma de debuterFormulaire

```txt
https://example.com/schemas/custom#/definitions/DebuterFormulaire
```

Paramètres de la page permettant de débuter un formulaire.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de DebuterFormulaire

| Propriété                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                |
| :-------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [authentifie](#authentifie) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-debuterformulaire-properties-authentifie.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie") |
| [anonyme](#anonyme)         | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-debuterformulaire-properties-anonyme.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme")         |

## authentifie

Paramètres de la page permettant de débuter un formulaire authentifié.

`authentifie`

*   est optionnel

*   Type: `object` ([authentifie](frw-definitions-debuterformulaire-properties-authentifie.md))

*   ne peut être nul

## anonyme

Paramètres de la page permettant de débuter un formulaire anonyme.

`anonyme`

*   est optionnel

*   Type: `object` ([anonyme](frw-definitions-debuterformulaire-properties-anonyme.md))

*   ne peut être nul
