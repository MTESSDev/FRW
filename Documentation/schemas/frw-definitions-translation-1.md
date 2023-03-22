# Translation Schema

```txt
https://example.com/schemas/custom#/definitions/Tooltip
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Tooltip Type

`object` ([Translation](frw-definitions-translation-1.md))

## Tooltip Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

# Tooltip Properties

| Property              | Type     | Required | Nullable       | Defined by                                                                                                                   |
| :-------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| [title](#title)       | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/title") |
| [text](#text)         | `object` | Required | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/text")  |
| Additional Properties | Any      | Optional | can be null    |                                                                                                                              |

## title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/title")

### title Type

`object` ([Translation](frw-definitions-translation.md))

### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## text

Multilingue

`text`

*   is required

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/text")

### text Type

`object` ([Translation](frw-definitions-translation.md))

### text Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## Additional Properties

Additional properties are allowed and do not have to follow a specific schema
