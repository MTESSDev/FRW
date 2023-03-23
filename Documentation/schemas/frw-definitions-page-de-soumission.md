# Schéma de Page de soumission

```txt
https://example.com/schemas/custom#/definitions/Soumission
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Soumission

`object` ([Page de soumission](frw-definitions-page-de-soumission.md))

# Propriétés de Soumission

| Propriété                                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                     |
| :-------------------------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteBoutonSoumettre](#texteboutonsoumettre) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Soumission/properties/texteBoutonSoumettre") |

## texteBoutonSoumettre

Multilingue

`texteBoutonSoumettre`

*   est optionnel

*   ne peut être nul

### Type de texteBoutonSoumettre

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de texteBoutonSoumettre

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
