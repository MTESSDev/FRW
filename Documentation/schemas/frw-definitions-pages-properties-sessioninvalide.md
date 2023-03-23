# Schéma de sessionInvalide

```txt
https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide
```

Paramètres associés à la page de session invalide.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de sessionInvalide

| Propriété                                               | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                |
| :------------------------------------------------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [titrePage](#titrepage)                                 | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide/properties/titrePage")                 |
| [corpsMessageAvertissement](#corpsmessageavertissement) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide/properties/corpsMessageAvertissement") |

## titrePage

Multilingue

`titrePage`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

### Valeur par défaut de titrePage

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## corpsMessageAvertissement

Multilingue

`corpsMessageAvertissement`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

### Valeur par défaut de corpsMessageAvertissement

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
