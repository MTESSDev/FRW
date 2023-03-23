# Schéma de Scripts Vue.js à injecter au formulaire.

```txt
https://example.com/schemas/custom#/definitions/InjecterJs
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de InjecterJs

| Propriété             | Type     | Obligatoire | Nullable         | Défini par                                                                                                                         |
| :-------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| [method](#method)     | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/method")   |
| [computed](#computed) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/computed") |
| [watch](#watch)       | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/watch")    |

## method

Méthodes de type 'method' à injecter au code au modèle vue.js du formulaire.

`method`

*   est optionnel

*   Type: `object` ([method](frw-definitions-nomfonction.md))

*   ne peut être nul

## computed

Méthodes de type 'computed' à injecter au code au modèle vue.js du formulaire.

`computed`

*   est optionnel

*   Type: `object` ([computed](frw-definitions-nomfonction.md))

*   ne peut être nul

## watch

Méthodes de type 'watch' à injecter au code au modèle vue.js du formulaire.

`watch`

*   est optionnel

*   Type: `object` ([watch](frw-definitions-nomfonction.md))

*   ne peut être nul
