## Type de ConfirmationTransmission

`object` ([Confirmation de transmission](frw-form-definitions-confirmation-de-transmission.md))

# Propriétés de ConfirmationTransmission

| Propriété                                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                    |
| :---------------------------------------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [texteSupplementaire](#textesupplementaire)                 | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ConfirmationTransmission/properties/texteSupplementaire")                                                                  |
| [nomChampCourrielUtilisateur](#nomchampcourrielutilisateur) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "schemas/form#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur") |
| [modaleCourrielConfirmation](#modalecourrielconfirmation)   | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-fenêtre-modale-de-courriel-de-confirmation.md "schemas/form#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")                           |

## texteSupplementaire

Textes multilingue (fr et en supportés seulement)

`texteSupplementaire`

*   est optionnel

*   ne peut être nul

### Type de texteSupplementaire

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Fenêtre modale de courriel de confirmation](frw-form-definitions-fenêtre-modale-de-courriel-de-confirmation.md))
