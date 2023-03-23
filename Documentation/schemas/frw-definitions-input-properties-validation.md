# Schéma de Validation

```txt
https://example.com/schemas/custom#/definitions/Input/properties/validations
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de validations

`object` ([Validation](frw-definitions-input-properties-validation.md))

## Valeur par défaut de validations

La valeur par défaut est:

```yaml
{}

```

# Propriétés de validations

| Propriété                     | Type         | Obligatoire | Nullable         | Défini par                                                                                                                                                                                       |
| :---------------------------- | :----------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [required](#required)         | `string`     | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-required.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/required")         |
| [accepted](#accepted)         | Non spécifié | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-accepted.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/accepted")         |
| [before](#before)             | `string`     | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-before.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/before")             |
| [after](#after)               | `string`     | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-after.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/after")               |
| [alpha](#alpha)               | `string`     | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-alpha.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alpha")               |
| [alphanumeric](#alphanumeric) | `string`     | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-alphanumeric.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alphanumeric") |
| [between](#between)           | `string`     | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-between.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/between")           |
| [confirm](#confirm)           | `string`     | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-confirm.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/confirm")           |
| [bail](#bail)                 | Non spécifié | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-bail.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/bail")                 |
| [email](#email)               | Non spécifié | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-email.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/email")               |
| [starts\_with](#starts_with)  | `string`     | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-starts_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/starts_with")   |
| [avant](#avant)               | `string`     | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-avant.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/avant")               |
| [ends\_with](#ends_with)      | `string`     | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-ends_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/ends_with")       |
| [in](#in)                     | `string`     | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-in.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/in")                     |
| [matches](#matches)           | `string`     | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-matches.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/matches")           |
| [min](#min)                   | Plusieurs    | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/min")                   |
| [max](#max)                   | Plusieurs    | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/max")                   |
| [mime](#mime)                 | `string`     | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-mime.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/mime")                 |
| [not](#not)                   | `string`     | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-not.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/not")                   |
| [number](#number)             | Non spécifié | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-number.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/number")             |
| [optional](#optional)         | Non spécifié | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-optional.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/optional")         |
| [url](#url)                   | Non spécifié | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation-properties-url.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/url")                   |
| [nas](#nas)                   | `boolean`    | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-properties-nas.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/nas")                   |

## required

Checks if the input is empty.

`required`

*   est optionnel

*   Type: `string`

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-required.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/required")

### Type de required

`string`

### Contraintes de required

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur   | Explication |
| :------- | :---------- |
| `"trim"` |             |
| `null`   |             |

### Valeur par défaut de required

La valeur par défaut est:

```yaml
trim

```

## accepted

The value must be yes, on, 1 or true. Useful for box inputs, often where you need to validate if someone has accepted terms.

`accepted`

*   est optionnel

*   Type: `null`, la valeur doit être nulle

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-accepted.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/accepted")

### Type de accepted

`null`, la valeur doit être nulle

## before

Checks if a date comes before another date. If no date argument is provided the current time will be used. The value must be a Date object or a string that can be evaluated by Date.parse.

`before`

*   est optionnel

*   Type: `string`

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-before.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/before")

### Type de before

`string`

### Exemple de before

```yaml
'2020-12-31'

```

## after

Checks if a date comes after another date. If no date argument is provided the current time will be used. The value must be a Date object or a string that can be evaluated by Date.parse.

`after`

*   est optionnel

*   Type: `string`

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-after.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/after")

### Type de after

`string`

### Exemple de after

```yaml
'2020-12-31'

```

## alpha

Checks if a value is only alphabetical characters. There are two character sets latin and default. Latin characters are strictly \[a-zA-Z] while the default set includes most accented characters as well like: ä, ù, or ś.

`alpha`

*   est optionnel

*   Type: `string`

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-alpha.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alpha")

### Type de alpha

`string`

### Contraintes de alpha

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur      | Explication |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |

### Exemple de alpha

```yaml
latin

```

## alphanumeric

Checks if a value is only made of alphabetical characters or numeric digits. For the alphabetical portion you can pass default or latin - see alpha.

`alphanumeric`

*   est optionnel

*   Type: `string`

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-alphanumeric.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/alphanumeric")

### Type de alphanumeric

`string`

### Contraintes de alphanumeric

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur      | Explication |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |
| `null`      |             |

## between

Checks if a number or string length is between a minimum or maximum. Both the maximum and minimum are exclusive. If the value being validated is a string the string’s length is used for comparison. If a number is used, the numeric value is used for comparison. In v2.2.4+ you can force it to always check the numeric value or string length by setting an optional third argument to value or length.

`between`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-between.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/between")

### Type de between

`string`

### Exemple de between

```yaml
10,18,value

```

```yaml
8,20,length

```

## confirm

Checks if the field value matches the value of another field. Mostly used for hidden fields - like password confirmations. By default, a confirm rule will look for other fields in the same FormulateForm with the suffix \_confirm. If you’d like the rule to use a different field as the confirmation, simply pass the other field name as an argument confirm:other\_field.

`confirm`

*   est optionnel

*   Type: `string`

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-confirm.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/confirm")

### Type de confirm

`string`

### Exemple de confirm

```yaml
confirm:other_field

```

## bail

Used to logically stop validation on the first subsequent validation error.

`bail`

*   est optionnel

*   Type: `null`, la valeur doit être nulle

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-bail.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/bail")

### Type de bail

`null`, la valeur doit être nulle

## email

Checks if the input is a valid email address format.

`email`

*   est optionnel

*   Type: `null`, la valeur doit être nulle

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-email.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/email")

### Type de email

`null`, la valeur doit être nulle

## starts\_with

Checks if the input starts with one of the provided options.

`starts_with`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-starts_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/starts_with")

### Type de starts\_with

`string`

## avant

Pour une date qui doit être AVANT la date du jour.

`avant`

*   est optionnel

*   Type: `string`

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-avant.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/avant")

### Type de avant

`string`

## ends\_with

Checks if the input ends with one of the provided options.

`ends_with`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-ends_with.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/ends_with")

### Type de ends\_with

`string`

## in

Checks if the input is included in an array of options.

`in`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-in.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/in")

### Type de in

`string`

## matches

Checks if the input matches a particular value or pattern. If you pass multiple arguments, it checks each until a match is found.

`matches`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-matches.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/matches")

### Type de matches

`string`

### Exemple de matches

```yaml
val1,val2

```

```yaml
/[0-9]/

```

## min

Checks the value of a Number, or length of a String or Array is more than a maximum length or value. The minimum value/length defaults to 1. You can force the validator to evaluate length or value by passing a second argument of either length or value.

`min`

*   est optionnel

*   Type: l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-validation-properties-min.md))

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/min")

### Type de min

l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-validation-properties-min.md))

### Exemple de min

```yaml
9,length

```

```yaml
'3'

```

```yaml
10,value

```

## max

Checks that the value of a Number, or length of a String or Array is less than a maximum length or value. The maximum value/length defaults to 10.

`max`

*   est optionnel

*   Type: l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-validation-properties-max.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/max")

### Type de max

l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-validation-properties-max.md))

### Exemple de max

```yaml
5,length

```

```yaml
3

```

```yaml
10,value

```

## mime

Checks if the type of file selected is an allowed value. This validator uses the file’s extension to determine the mime type. Back-end validation of the file’s content is still strongly encouraged as front-end validation can be bypassed by savvy users.

`mime`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-mime.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/mime")

### Type de mime

`string`

### Exemple de mime

```yaml
image/png

```

```yaml
image/jpeg

```

## not

Checks to ensure the input data does not match a set of predefined values.

`not`

*   est optionnel

*   Type: `string`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-not.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/not")

### Type de not

`string`

### Exemple de not

```yaml
val1,val2

```

## number

Checks if the input is a valid number as evaluated by isNaN().

`number`

*   est optionnel

*   Type: `null`, la valeur doit être nulle

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-number.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/number")

### Type de number

`null`, la valeur doit être nulle

## optional

Use this rule to make a field optional. When used all validation rules pass until the field is no longer empty. Its location in the list of validation rules has no effect.

`optional`

*   est optionnel

*   Type: `null`, la valeur doit être nulle

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-optional.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/optional")

### Type de optional

`null`, la valeur doit être nulle

## url

Checks if the input value appears to be a properly formatted URL including the protocol. This does not check if the URL actually resolves.

`url`

*   est optionnel

*   Type: `null`, la valeur doit être nulle

*   peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-url.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/url")

### Type de url

`null`, la valeur doit être nulle

## nas

Valider le NAS, si true valide vraiment que le NAS est valide, si false valide que c'est un nombre de 9 de long seulement.

`nas`

*   est optionnel

*   Type: `boolean`

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-input-properties-validation-properties-nas.md "https://example.com/schemas/custom#/definitions/Input/properties/validations/properties/nas")

### Type de nas

`boolean`
