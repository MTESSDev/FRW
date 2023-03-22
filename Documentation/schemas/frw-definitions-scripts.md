# scripts Schema

```txt
https://example.com/schemas/custom#/definitions/Scripts
```

(Avancé) Paramètres d'injection de javascript.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Scripts Type

`object` ([scripts](frw-definitions-scripts.md))

# Scripts Properties

| Property                                | Type     | Required | Nullable       | Defined by                                                                                                                                                        |
| :-------------------------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [outilStatistiques](#outilstatistiques) | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-scripts-properties-outilstatistiques.md "https://example.com/schemas/custom#/definitions/Scripts/properties/outilStatistiques") |

## outilStatistiques

Javascript servant à une solution d'outil statistiques (ex. Google Analytics ou Matomo). Injecté dans toutes les pages à la fin du body.

`outilStatistiques`

*   is optional

*   Type: `string` ([outilStatistiques](frw-definitions-scripts-properties-outilstatistiques.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-scripts-properties-outilstatistiques.md "https://example.com/schemas/custom#/definitions/Scripts/properties/outilStatistiques")

### outilStatistiques Type

`string` ([outilStatistiques](frw-definitions-scripts-properties-outilstatistiques.md))

### outilStatistiques Examples

```json
"<script> // Votre js ici... </script>"
```
