# Untitled schema Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/matches
```

Checks if the input matches a particular value or pattern. If you pass multiple arguments, it checks each until a match is found.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## matches Type

`string`

## matches Examples

```json
"val1,val2"
```

```json
"/[0-9]/"
```
