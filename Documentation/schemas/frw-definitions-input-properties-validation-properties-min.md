# Untitled schema Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/min
```

Checks the value of a Number, or length of a String or Array is more than a maximum length or value. The minimum value/length defaults to 1. You can force the validator to evaluate length or value by passing a second argument of either length or value.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## min Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-validation-properties-min.md))

## min Examples

```json
"9,length"
```

```json
"3"
```

```json
"10,value"
```
