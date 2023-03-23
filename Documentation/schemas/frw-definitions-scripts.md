# Schéma de scripts

```txt
https://example.com/schemas/custom#/definitions/Scripts
```

(Avancé) Paramètres d'injection de javascript.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Scripts

`object` ([scripts](frw-definitions-scripts.md))

# Propriétés de Scripts

| Propriété                               | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                        |
| :-------------------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [outilStatistiques](#outilstatistiques) | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-scripts-properties-outilstatistiques.md "https://example.com/schemas/custom#/definitions/Scripts/properties/outilStatistiques") |

## outilStatistiques

Javascript servant à une solution d'outil statistiques (ex. Google Analytics ou Matomo). Injecté dans toutes les pages à la fin du body.

`outilStatistiques`

*   est optionnel

*   ne peut être nul

### Type de outilStatistiques

`string` ([outilStatistiques](frw-definitions-scripts-properties-outilstatistiques.md))

### Exemple de outilStatistiques

```yaml
<script> // Votre js ici... </script>

```
