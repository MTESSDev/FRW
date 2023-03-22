# sessionInvalide Schema

```txt
https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide
```

Paramètres associés à la page de session invalide.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## sessionInvalide Type

`object` ([sessionInvalide](frw-definitions-pages-properties-sessioninvalide.md))

# sessionInvalide Properties

| Property                                                | Type     | Required | Nullable       | Defined by                                                                                                                                                                |
| :------------------------------------------------------ | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [titrePage](#titrepage)                                 | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide/properties/titrePage")                 |
| [corpsMessageAvertissement](#corpsmessageavertissement) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide/properties/corpsMessageAvertissement") |

## titrePage

Multilingue

`titrePage`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide/properties/titrePage")

### titrePage Type

`object` ([Translation](frw-definitions-translation.md))

### titrePage Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## corpsMessageAvertissement

Multilingue

`corpsMessageAvertissement`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide/properties/corpsMessageAvertissement")

### corpsMessageAvertissement Type

`object` ([Translation](frw-definitions-translation.md))

### corpsMessageAvertissement Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
