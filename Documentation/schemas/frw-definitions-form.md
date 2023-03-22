# Form Schema

```txt
https://example.com/schemas/custom#/definitions/Form
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Form Type

`object` ([Form](frw-definitions-form.md))

# Form Properties

| Property                                    | Type     | Required | Nullable       | Defined by                                                                                                                                                      |
| :------------------------------------------ | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sectionsGroup](#sectionsgroup)             | `array`  | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-sectionsgroup.md "https://example.com/schemas/custom#/definitions/Form/properties/sectionsGroup")             |
| [templates](#templates)                     | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-templates.md "https://example.com/schemas/custom#/definitions/Form/properties/templates")                     |
| [title](#title)                             | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Form/properties/title")                                       |
| [inputDefaultClasses](#inputdefaultclasses) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-inputdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/inputDefaultClasses") |
| [defaults](#defaults)                       | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-defaults-values.md "https://example.com/schemas/custom#/definitions/Form/properties/defaults")                                |
| [outerDefaultClasses](#outerdefaultclasses) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-outerdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/outerDefaultClasses") |

## sectionsGroup



`sectionsGroup`

*   is optional

*   Type: `object[]` ([Section Group](frw-definitions-section-group.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-sectionsgroup.md "https://example.com/schemas/custom#/definitions/Form/properties/sectionsGroup")

### sectionsGroup Type

`object[]` ([Section Group](frw-definitions-section-group.md))

## templates



`templates`

*   is optional

*   Type: `object` ([Details](frw-definitions-form-properties-templates.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-templates.md "https://example.com/schemas/custom#/definitions/Form/properties/templates")

### templates Type

`object` ([Details](frw-definitions-form-properties-templates.md))

## title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Form/properties/title")

### title Type

`object` ([Translation](frw-definitions-translation.md))

### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## inputDefaultClasses



`inputDefaultClasses`

*   is optional

*   Type: `object` ([Details](frw-definitions-form-properties-inputdefaultclasses.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-inputdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/inputDefaultClasses")

### inputDefaultClasses Type

`object` ([Details](frw-definitions-form-properties-inputdefaultclasses.md))

## defaults



`defaults`

*   is optional

*   Type: `object` ([Defaults values](frw-definitions-defaults-values.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-defaults-values.md "https://example.com/schemas/custom#/definitions/Form/properties/defaults")

### defaults Type

`object` ([Defaults values](frw-definitions-defaults-values.md))

## outerDefaultClasses



`outerDefaultClasses`

*   is optional

*   Type: `object` ([Details](frw-definitions-form-properties-outerdefaultclasses.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-outerdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/outerDefaultClasses")

### outerDefaultClasses Type

`object` ([Details](frw-definitions-form-properties-outerdefaultclasses.md))
