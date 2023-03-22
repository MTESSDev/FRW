# Untitled schema Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/required
```

Checks if the input is empty.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## required Type

`string`

## required Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value    | Explanation |
| :------- | :---------- |
| `"trim"` |             |
| `null`   |             |

## required Default Value

The default value is:

```json
"trim"
```
