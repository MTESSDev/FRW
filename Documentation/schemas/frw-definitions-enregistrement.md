# enregistrement Schema

```txt
https://example.com/schemas/custom#/definitions/Enregistrement
```

Paramètres associés à l'enregistrement d'un formulaire

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Enregistrement Type

`object` ([enregistrement](frw-definitions-enregistrement.md))

# Enregistrement Properties

| Property                                                                      | Type      | Required | Nullable       | Defined by                                                                                                                                                                                    |
| :---------------------------------------------------------------------------- | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)                                                               | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-enregistrement-properties-actif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/actif")                                       |
| [afficherMessageIncitatif](#affichermessageincitatif)                         | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-enregistrement-properties-affichermessageincitatif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/afficherMessageIncitatif") |
| [texteModaleEnregistrementAuthentifie](#textemodaleenregistrementauthentifie) | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")                            |

## actif

Indique si l'enregistrement du formulaire est actif (bouton enregistré présent et enregistrement au changement de page).

`actif`

*   is optional

*   Type: `boolean` ([actif](frw-definitions-enregistrement-properties-actif.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-enregistrement-properties-actif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/actif")

### actif Type

`boolean` ([actif](frw-definitions-enregistrement-properties-actif.md))

## afficherMessageIncitatif

Indique si le message (avis avertissement en haut de chaque page) incitant l'enregistrement est affiché ou non.

`afficherMessageIncitatif`

*   is optional

*   Type: `boolean` ([afficherMessageIncitatif](frw-definitions-enregistrement-properties-affichermessageincitatif.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-enregistrement-properties-affichermessageincitatif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/afficherMessageIncitatif")

### afficherMessageIncitatif Type

`boolean` ([afficherMessageIncitatif](frw-definitions-enregistrement-properties-affichermessageincitatif.md))

## texteModaleEnregistrementAuthentifie

Multilingue

`texteModaleEnregistrementAuthentifie`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")

### texteModaleEnregistrementAuthentifie Type

`object` ([Translation](frw-definitions-translation.md))

### texteModaleEnregistrementAuthentifie Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
