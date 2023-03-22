# anonyme Schema

```txt
https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme
```

Paramètres de la page permettant de débuter un formulaire anonyme.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## anonyme Type

`object` ([anonyme](frw-definitions-debuterformulaire-properties-anonyme.md))

# anonyme Properties

| Property                                                            | Type     | Required | Nullable       | Defined by                                                                                                                                                                          |
| :------------------------------------------------------------------ | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [texte](#texte)                                                     | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/texte")                           |
| [boutonDebuter](#boutondebuter)                                     | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/boutonDebuter")                   |
| [boutonDebuterTitreAccessibilite](#boutondebutertitreaccessibilite) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/boutonDebuterTitreAccessibilite") |

## texte

Multilingue

`texte`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/texte")

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

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/boutonDebuter")

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

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/boutonDebuterTitreAccessibilite")

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
