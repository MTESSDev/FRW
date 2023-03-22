# erreurTechnique Schema

```txt
https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique
```

Paramètres du message d'erreur technique.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## erreurTechnique Type

`object` ([erreurTechnique](frw-definitions-messages-properties-erreurtechnique.md))

# erreurTechnique Properties

| Property        | Type     | Required | Nullable       | Defined by                                                                                                                                               |
| :-------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [titre](#titre) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique/properties/titre") |
| [corps](#corps) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique/properties/corps") |

## titre

Multilingue

`titre`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique/properties/titre")

### titre Type

`object` ([Translation](frw-definitions-translation.md))

### titre Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## corps

Multilingue

`corps`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique/properties/corps")

### corps Type

`object` ([Translation](frw-definitions-translation.md))

### corps Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
