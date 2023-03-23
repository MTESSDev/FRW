# Schéma de Schéma sans nom

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/required
```

Checks if the input is empty.

| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de required

`string`

## Contraintes de required

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur   | Explication |
| :------- | :---------- |
| `"trim"` |             |
| `null`   |             |

## Valeur par défaut de required

La valeur par défaut est:

```yaml
trim

```
