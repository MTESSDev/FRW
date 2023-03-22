# validation-messages (Messages de validation personnalisés) Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validation-messages
```



| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## validation-messages Type

`object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md))

# validation-messages Properties

| Property         | Type     | Required | Nullable       | Defined by                                                                                                                                               |
| :--------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$") |

## Pattern: `^[a-zA-Z0-9]+$`

Multilingue

`^[a-zA-Z0-9]+$`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$")

### ^\[a-zA-Z0-9]+$ Type

`object` ([Translation](frw-definitions-translation.md))

### ^\[a-zA-Z0-9]+$ Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
