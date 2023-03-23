# Schéma de Schéma sans nom

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/matches
```

Checks if the input matches a particular value or pattern. If you pass multiple arguments, it checks each until a match is found.

| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Exemple de matches

```yaml
val1,val2

```

```yaml
/[0-9]/

```
