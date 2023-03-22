# Page de soumission Schema

```txt
https://example.com/schemas/custom#/definitions/Soumission
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Soumission Type

`object` ([Page de soumission](frw-definitions-page-de-soumission.md))

# Soumission Properties

| Property                                      | Type     | Required | Nullable       | Defined by                                                                                                                                     |
| :-------------------------------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteBoutonSoumettre](#texteboutonsoumettre) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Soumission/properties/texteBoutonSoumettre") |

## texteBoutonSoumettre

Multilingue

`texteBoutonSoumettre`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Soumission/properties/texteBoutonSoumettre")

### texteBoutonSoumettre Type

`object` ([Translation](frw-definitions-translation.md))

### texteBoutonSoumettre Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
