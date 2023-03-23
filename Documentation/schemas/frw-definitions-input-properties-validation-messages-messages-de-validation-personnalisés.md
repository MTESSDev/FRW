# Schéma de validation-messages (Messages de validation personnalisés)

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validation-messages
```



| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de validation-messages

`object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md))

# Propriétés de validation-messages

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                               |
| :--------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$") |

## Modèle:`^[a-zA-Z0-9]+$`

Multilingue

`^[a-zA-Z0-9]+$`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$")

### Type de ^\[a-zA-Z0-9]+$

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de ^\[a-zA-Z0-9]+$

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
