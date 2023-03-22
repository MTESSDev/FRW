# Untitled schema Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/mime
```

Checks if the type of file selected is an allowed value. This validator uses the file’s extension to determine the mime type. Back-end validation of the file’s content is still strongly encouraged as front-end validation can be bypassed by savvy users.

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## mime Type

`string`

## mime Examples

```json
"image/png"
```

```json
"image/jpeg"
```
