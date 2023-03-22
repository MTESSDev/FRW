# Untitled schema Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alpha
```

Checks if a value is only alphabetical characters. There are two character sets latin and default. Latin characters are strictly \[a-zA-Z] while the default set includes most accented characters as well like: ä, ù, or ś.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## alpha Type

`string`

## alpha Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value       | Explanation |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |

## alpha Examples

```json
"latin"
```
