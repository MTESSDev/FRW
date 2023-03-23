# Schéma de Schéma sans nom

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/after
```

Checks if a date comes after another date. If no date argument is provided the current time will be used. The value must be a Date object or a string that can be evaluated by Date.parse.

| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Exemple de after

```yaml
'2020-12-31'

```
