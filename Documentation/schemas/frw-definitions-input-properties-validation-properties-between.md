# Schéma de Schéma sans nom

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/between
```

Checks if a number or string length is between a minimum or maximum. Both the maximum and minimum are exclusive. If the value being validated is a string the string’s length is used for comparison. If a number is used, the numeric value is used for comparison. In v2.2.4+ you can force it to always check the numeric value or string length by setting an optional third argument to value or length.

| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de between

`string`

## Exemple de between

```yaml
10,18,value

```

```yaml
8,20,length

```
