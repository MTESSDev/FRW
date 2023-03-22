# Confirmation de transmission Schema

```txt
https://example.com/schemas/custom#/definitions/ConfirmationTransmission
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## ConfirmationTransmission Type

`object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

# ConfirmationTransmission Properties

| Property                                                    | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                  |
| :---------------------------------------------------------- | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteSupplementaire](#textesupplementaire)                 | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/texteSupplementaire")                                                                 |
| [nomChampCourrielUtilisateur](#nomchampcourrielutilisateur) | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur") |
| [modaleCourrielConfirmation](#modalecourrielconfirmation)   | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")                           |

## texteSupplementaire

Multilingue

`texteSupplementaire`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/texteSupplementaire")

### texteSupplementaire Type

`object` ([Translation](frw-definitions-translation.md))

### texteSupplementaire Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## nomChampCourrielUtilisateur

Nom du champ courriel qui contient l'adresse courriel à utiliser pour le courriel de confirmation de transmission.

`nomChampCourrielUtilisateur`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur")

### nomChampCourrielUtilisateur Type

`string`

## modaleCourrielConfirmation



`modaleCourrielConfirmation`

*   is optional

*   Type: `object` ([Fenêtre modale de courriel de confirmation](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")

### modaleCourrielConfirmation Type

`object` ([Fenêtre modale de courriel de confirmation](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md))
