# Untitled schema Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/max
```

Checks that the value of a Number, or length of a String or Array is less than a maximum length or value. The maximum value/length defaults to 10.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## max Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-validation-properties-max.md))

## max Examples

```json
"5,length"
```

```json
3
```

```json
"10,value"
```
