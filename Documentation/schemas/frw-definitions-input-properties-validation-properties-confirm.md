# Untitled schema Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/confirm
```

Checks if the field value matches the value of another field. Mostly used for hidden fields - like password confirmations. By default, a confirm rule will look for other fields in the same FormulateForm with the suffix \_confirm. If you’d like the rule to use a different field as the confirmation, simply pass the other field name as an argument confirm:other\_field.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## confirm Type

`string`

## confirm Examples

```json
"confirm:other_field"
```
