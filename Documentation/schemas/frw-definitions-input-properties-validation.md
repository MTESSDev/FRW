# Validation Schema

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## validations Type

`object` ([Validation](frw-definitions-input-properties-validation.md))

## validations Default Value

The default value is:

```json
{}
```

# validations Properties

| Property                      | Type          | Required | Nullable       | Defined by                                                                                                                                                                                       |
| :---------------------------- | :------------ | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [required](#required)         | `string`      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-required.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/required")         |
| [accepted](#accepted)         | Not specified | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-accepted.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/accepted")         |
| [before](#before)             | `string`      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-before.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/before")             |
| [after](#after)               | `string`      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-after.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/after")               |
| [alpha](#alpha)               | `string`      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-alpha.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alpha")               |
| [alphanumeric](#alphanumeric) | `string`      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-alphanumeric.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alphanumeric") |
| [between](#between)           | `string`      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-between.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/between")           |
| [confirm](#confirm)           | `string`      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-confirm.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/confirm")           |
| [bail](#bail)                 | Not specified | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-bail.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/bail")                 |
| [email](#email)               | Not specified | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-email.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/email")               |
| [starts\_with](#starts_with)  | `string`      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-starts_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/starts_with")   |
| [avant](#avant)               | `string`      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-avant.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/avant")               |
| [ends\_with](#ends_with)      | `string`      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-ends_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/ends_with")       |
| [in](#in)                     | `string`      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-in.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/in")                     |
| [matches](#matches)           | `string`      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-matches.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/matches")           |
| [min](#min)                   | Multiple      | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/min")                   |
| [max](#max)                   | Multiple      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/max")                   |
| [mime](#mime)                 | `string`      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-mime.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/mime")                 |
| [not](#not)                   | `string`      | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-not.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/not")                   |
| [number](#number)             | Not specified | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-number.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/number")             |
| [optional](#optional)         | Not specified | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-optional.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/optional")         |
| [url](#url)                   | Not specified | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation-properties-url.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/url")                   |
| [nas](#nas)                   | `boolean`     | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-properties-nas.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/nas")                   |

## required

Checks if the input is empty.

`required`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-required.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/required")

### required Type

`string`

### required Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value    | Explanation |
| :------- | :---------- |
| `"trim"` |             |
| `null`   |             |

### required Default Value

The default value is:

```json
"trim"
```

## accepted

The value must be yes, on, 1 or true. Useful for box inputs, often where you need to validate if someone has accepted terms.

`accepted`

*   is optional

*   Type: `null`, the value must be null

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-accepted.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/accepted")

### accepted Type

`null`, the value must be null

## before

Checks if a date comes before another date. If no date argument is provided the current time will be used. The value must be a Date object or a string that can be evaluated by Date.parse.

`before`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-before.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/before")

### before Type

`string`

### before Examples

```json
"2020-12-31"
```

## after

Checks if a date comes after another date. If no date argument is provided the current time will be used. The value must be a Date object or a string that can be evaluated by Date.parse.

`after`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-after.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/after")

### after Type

`string`

### after Examples

```json
"2020-12-31"
```

## alpha

Checks if a value is only alphabetical characters. There are two character sets latin and default. Latin characters are strictly \[a-zA-Z] while the default set includes most accented characters as well like: ä, ù, or ś.

`alpha`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-alpha.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alpha")

### alpha Type

`string`

### alpha Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value       | Explanation |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |

### alpha Examples

```json
"latin"
```

## alphanumeric

Checks if a value is only made of alphabetical characters or numeric digits. For the alphabetical portion you can pass default or latin - see alpha.

`alphanumeric`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-alphanumeric.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alphanumeric")

### alphanumeric Type

`string`

### alphanumeric Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value       | Explanation |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |
| `null`      |             |

## between

Checks if a number or string length is between a minimum or maximum. Both the maximum and minimum are exclusive. If the value being validated is a string the string’s length is used for comparison. If a number is used, the numeric value is used for comparison. In v2.2.4+ you can force it to always check the numeric value or string length by setting an optional third argument to value or length.

`between`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-between.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/between")

### between Type

`string`

### between Examples

```json
"10,18,value"
```

```json
"8,20,length"
```

## confirm

Checks if the field value matches the value of another field. Mostly used for hidden fields - like password confirmations. By default, a confirm rule will look for other fields in the same FormulateForm with the suffix \_confirm. If you’d like the rule to use a different field as the confirmation, simply pass the other field name as an argument confirm:other\_field.

`confirm`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-confirm.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/confirm")

### confirm Type

`string`

### confirm Examples

```json
"confirm:other_field"
```

## bail

Used to logically stop validation on the first subsequent validation error.

`bail`

*   is optional

*   Type: `null`, the value must be null

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-bail.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/bail")

### bail Type

`null`, the value must be null

## email

Checks if the input is a valid email address format.

`email`

*   is optional

*   Type: `null`, the value must be null

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-email.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/email")

### email Type

`null`, the value must be null

## starts\_with

Checks if the input starts with one of the provided options.

`starts_with`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-starts_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/starts_with")

### starts\_with Type

`string`

## avant

Pour une date qui doit être AVANT la date du jour.

`avant`

*   is optional

*   Type: `string`

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-avant.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/avant")

### avant Type

`string`

## ends\_with

Checks if the input ends with one of the provided options.

`ends_with`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-ends_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/ends_with")

### ends\_with Type

`string`

## in

Checks if the input is included in an array of options.

`in`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-in.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/in")

### in Type

`string`

## matches

Checks if the input matches a particular value or pattern. If you pass multiple arguments, it checks each until a match is found.

`matches`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-matches.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/matches")

### matches Type

`string`

### matches Examples

```json
"val1,val2"
```

```json
"/[0-9]/"
```

## min

Checks the value of a Number, or length of a String or Array is more than a maximum length or value. The minimum value/length defaults to 1. You can force the validator to evaluate length or value by passing a second argument of either length or value.

`min`

*   is optional

*   Type: any of the following: `string` or `number` ([Details](frw-definitions-input-properties-validation-properties-min.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/min")

### min Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-validation-properties-min.md))

### min Examples

```json
"9,length"
```

```json
"3"
```

```json
"10,value"
```

## max

Checks that the value of a Number, or length of a String or Array is less than a maximum length or value. The maximum value/length defaults to 10.

`max`

*   is optional

*   Type: any of the following: `string` or `number` ([Details](frw-definitions-input-properties-validation-properties-max.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/max")

### max Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-validation-properties-max.md))

### max Examples

```json
"5,length"
```

```json
3
```

```json
"10,value"
```

## mime

Checks if the type of file selected is an allowed value. This validator uses the file’s extension to determine the mime type. Back-end validation of the file’s content is still strongly encouraged as front-end validation can be bypassed by savvy users.

`mime`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-mime.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/mime")

### mime Type

`string`

### mime Examples

```json
"image/png"
```

```json
"image/jpeg"
```

## not

Checks to ensure the input data does not match a set of predefined values.

`not`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-not.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/not")

### not Type

`string`

### not Examples

```json
"val1,val2"
```

## number

Checks if the input is a valid number as evaluated by isNaN().

`number`

*   is optional

*   Type: `null`, the value must be null

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-number.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/number")

### number Type

`null`, the value must be null

## optional

Use this rule to make a field optional. When used all validation rules pass until the field is no longer empty. Its location in the list of validation rules has no effect.

`optional`

*   is optional

*   Type: `null`, the value must be null

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-optional.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/optional")

### optional Type

`null`, the value must be null

## url

Checks if the input value appears to be a properly formatted URL including the protocol. This does not check if the URL actually resolves.

`url`

*   is optional

*   Type: `null`, the value must be null

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-url.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/url")

### url Type

`null`, the value must be null

## nas

Valider le NAS, si true valide vraiment que le NAS est valide, si false valide que c'est un nombre de 9 de long seulement.

`nas`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-properties-nas.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/nas")

### nas Type

`boolean`
