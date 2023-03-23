# Schéma de Page de révision

```txt
https://example.com/schemas/custom#/definitions/Revision
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Revision

`object` ([Page de révision](frw-definitions-page-de-révision.md))

# Propriétés de Revision

| Propriété                                       | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                          |
| :---------------------------------------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [validationAutomatique](#validationautomatique) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-page-de-révision-properties-validationautomatique.md "https://example.com/schemas/custom#/definitions/Revision/properties/validationAutomatique") |

## validationAutomatique

Indique si la fenêtre modale permettant la saisie d'une adresse courriel pour le courriel de confirmation est affichée ou non.

`validationAutomatique`

*   est optionnel

*   ne peut être nul

### Type de validationAutomatique

`boolean`
