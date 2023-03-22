# Translation Schema

```txt
https://example.com/schemas/custom#/definitions/Translation
```

Multilingue

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Translation Type

`object` ([Translation](frw-definitions-translation.md))

## Translation Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

# Translation Properties

| Property              | Type     | Required | Nullable    | Defined by                                                                                                                                  |
| :-------------------- | :------- | :------- | :---------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| [fr](#fr)             | `string` | Required | can be null | [Untitled schema](frw-definitions-translation-properties-fr.md "https://example.com/schemas/custom#/definitions/Translation/properties/fr") |
| [en](#en)             | `string` | Optional | can be null | [Untitled schema](frw-definitions-translation-properties-en.md "https://example.com/schemas/custom#/definitions/Translation/properties/en") |
| Additional Properties | Any      | Optional | can be null |                                                                                                                                             |

## fr

Texte de langue française.

`fr`

*   is required

*   Type: `string` ([fr](frw-definitions-translation-properties-fr.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-translation-properties-fr.md "https://example.com/schemas/custom#/definitions/Translation/properties/fr")

### fr Type

`string` ([fr](frw-definitions-translation-properties-fr.md))

## en

Texte de langue anglaise.

`en`

*   is optional

*   Type: `string` ([en](frw-definitions-translation-properties-en.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-translation-properties-en.md "https://example.com/schemas/custom#/definitions/Translation/properties/en")

### en Type

`string` ([en](frw-definitions-translation-properties-en.md))

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
