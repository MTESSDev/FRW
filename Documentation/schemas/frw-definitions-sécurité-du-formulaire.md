# Schéma de Sécurité du formulaire

```txt
https://example.com/schemas/custom#/definitions/Securite
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de Securite

| Propriété                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                              |
| :---------------------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [accesAnonyme](#accesanonyme) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-sécurité-du-formulaire-properties-accesanonyme.md "https://example.com/schemas/custom#/definitions/Securite/properties/accesAnonyme") |

## accesAnonyme

Permet d'activer l'accès anonyme au formulaire.

`accesAnonyme`

*   est optionnel

*   Type: `boolean`

*   ne peut être nul
