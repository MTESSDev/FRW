# Schéma de Schéma sans nom

```txt
https://example.com/schemas/custom#/definitions/Input/dependencies/addLabel
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de addLabel

| Propriété     | Type         | Obligatoire | Nullable         | Défini par                                                                                                                                                                      |
| :------------ | :----------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [type](#type) | Non spécifié | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-dependencies-addlabel-properties-type.md "https://example.com/schemas/custom#/definitions/Input/dependencies/addLabel/properties/type") |

## type



`type`

*   est optionnel

*   Type: inconnu

*   ne peut être nul

### Contraintes de type

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur              | Explication |
| :------------------ | :---------- |
| `"group"`           |             |
| `"file"`            |             |
| `"repeatableGroup"` |             |
