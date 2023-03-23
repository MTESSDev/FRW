# Schéma de Schéma sans nom

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alpha
```

Checks if a value is only alphabetical characters. There are two character sets latin and default. Latin characters are strictly \[a-zA-Z] while the default set includes most accented characters as well like: ä, ù, or ś.

| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de alpha

`string`

## Contraintes de alpha

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur      | Explication |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |

## Exemple de alpha

```yaml
latin

```
