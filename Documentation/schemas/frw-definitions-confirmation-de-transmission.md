# Schéma de Confirmation de transmission

```txt
https://example.com/schemas/custom#/definitions/ConfirmationTransmission
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de ConfirmationTransmission

`object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

# Propriétés de ConfirmationTransmission

| Propriété                                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                                  |
| :---------------------------------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteSupplementaire](#textesupplementaire)                 | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/texteSupplementaire")                                                                 |
| [nomChampCourrielUtilisateur](#nomchampcourrielutilisateur) | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur") |
| [modaleCourrielConfirmation](#modalecourrielconfirmation)   | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")                           |

## texteSupplementaire

Multilingue

`texteSupplementaire`

*   est optionnel

*   ne peut être nul

### Type de texteSupplementaire

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de texteSupplementaire

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## nomChampCourrielUtilisateur

Nom du champ courriel qui contient l'adresse courriel à utiliser pour le courriel de confirmation de transmission.

`nomChampCourrielUtilisateur`

*   est optionnel

*   ne peut être nul

### Type de nomChampCourrielUtilisateur

`string`

## modaleCourrielConfirmation



`modaleCourrielConfirmation`

*   est optionnel

*   ne peut être nul

### Type de modaleCourrielConfirmation

`object` ([Fenêtre modale de courriel de confirmation](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md))
