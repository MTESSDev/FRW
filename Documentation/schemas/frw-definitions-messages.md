# Schéma de messages

```txt
https://example.com/schemas/custom#/definitions/Messages
```

Paramètres associés aux différents messages.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Messages

`object` ([messages](frw-definitions-messages.md))

# Propriétés de Messages

| Propriété                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                      |
| :---------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [erreurTechnique](#erreurtechnique) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-messages-properties-erreurtechnique.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique") |

## erreurTechnique

Paramètres du message d'erreur technique.

`erreurTechnique`

*   est optionnel

*   ne peut être nul

### Type de erreurTechnique

`object` ([erreurTechnique](frw-definitions-messages-properties-erreurtechnique.md))
