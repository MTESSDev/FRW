# Schéma de Schéma sans nom

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/confirm
```

Checks if the field value matches the value of another field. Mostly used for hidden fields - like password confirmations. By default, a confirm rule will look for other fields in the same FormulateForm with the suffix \_confirm. If you’d like the rule to use a different field as the confirmation, simply pass the other field name as an argument confirm:other\_field.

| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de confirm

`string`

## Exemple de confirm

```yaml
confirm:other_field

```
