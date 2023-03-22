# authentifie Schema

```txt
https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie
```

Paramètres de la page permettant de débuter un formulaire authentifié.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## authentifie Type

`object` ([authentifie](frw-definitions-debuterformulaire-properties-authentifie.md))

# authentifie Properties

| Property                                                            | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                  |
| :------------------------------------------------------------------ | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)                                                     | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/actif") |
| [urlAuthentification](#urlauthentification)                         | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/urlAuthentification")                                 |
| [texte](#texte)                                                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/texte")                                               |
| [boutonDebuter](#boutondebuter)                                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuter")                                       |
| [boutonDebuterTitreAccessibilite](#boutondebutertitreaccessibilite) | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuterTitreAccessibilite")                     |

## actif

Indique si la page d'initialisation d'un formulaire est active ou non.

`actif`

*   is optional

*   Type: `boolean` ([actif](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/actif")

### actif Type

`boolean` ([actif](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md))

## urlAuthentification

Multilingue

`urlAuthentification`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/urlAuthentification")

### urlAuthentification Type

`object` ([Translation](frw-definitions-translation.md))

### urlAuthentification Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## texte

Multilingue

`texte`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/texte")

### texte Type

`object` ([Translation](frw-definitions-translation.md))

### texte Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## boutonDebuter

Multilingue

`boutonDebuter`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuter")

### boutonDebuter Type

`object` ([Translation](frw-definitions-translation.md))

### boutonDebuter Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## boutonDebuterTitreAccessibilite

Multilingue

`boutonDebuterTitreAccessibilite`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuterTitreAccessibilite")

### boutonDebuterTitreAccessibilite Type

`object` ([Translation](frw-definitions-translation.md))

### boutonDebuterTitreAccessibilite Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
