## Type de validations

`object` ([Validation](frw-form-definitions-composant-interaction-properties-validation.md))

## Valeur par défaut de validations

La valeur par défaut est:

```yaml
{}

```

# Propriétés de validations

| Propriété                        | Type         | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                                                                   |
| :------------------------------- | :----------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [required](#required)            | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-required.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/required")                                                    |
| [accepted](#accepted)            | Non spécifié | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-accepted.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/accepted")                                                    |
| [after](#after)                  | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-after.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/after")                                                          |
| [alpha](#alpha)                  | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-alpha.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/alpha")                                                          |
| [alphanumeric](#alphanumeric)    | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-alphanumeric.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/alphanumeric")                                            |
| [bail](#bail)                    | Non spécifié | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-bail.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/bail")                                                            |
| [before](#before)                | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-before.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/before")                                                        |
| [between](#between)              | `string`     | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-between.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/between")                                                      |
| [confirm](#confirm)              | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-confirm.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/confirm")                                                      |
| [date](#date)                    | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-date.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/date")                                                            |
| [email](#email)                  | Non spécifié | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-email.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/email")                                                          |
| [endsWith](#endswith)            | `string`     | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-endswith.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/endsWith")                                                    |
| [in](#in)                        | `string`     | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-in.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/in")                                                                |
| [matches](#matches)              | `string`     | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-matches.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/matches")                                                      |
| [max](#max)                      | Plusieurs    | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-max.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/max")                                                              |
| [mime](#mime)                    | `string`     | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-mime.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/mime")                                                            |
| [min](#min)                      | Plusieurs    | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-min.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/min")                                                              |
| [not](#not)                      | `string`     | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-not.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/not")                                                              |
| [number](#number)                | Non spécifié | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-number.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/number")                                                        |
| [optional](#optional)            | Non spécifié | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-optional.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/optional")                                                    |
| [url](#url)                      | Non spécifié | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-url.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/url")                                                              |
| [startsWith](#startswith)        | `string`     | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-startswith.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/startsWith")                                                |
| [avant](#avant)                  | `string`     | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-avant.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/avant")                                                          |
| [nam](#nam)                      | `boolean`    | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-nam.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/nam")                                                              |
| [nas](#nas)                      | `boolean`    | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-properties-nas.md "schemas/form#/definitions/ComposantInteraction/properties/validations/properties/nas")                                                              |
| `^[a-z][a-z0-9A-Z]{1,99}Custom$` | Plusieurs    | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation-patternproperties-a-za-z0-9a-z199custom.md "schemas/form#/definitions/ComposantInteraction/properties/validations/patternProperties/^\[a-z]\[a-z0-9A-Z]{1,99}Custom$") |

## required

Checks if the input is empty.

`required`

*   est optionnel

*   peut être nul

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

*   peut être nul

### Type de accepted

`null`, la valeur doit être nulle

## after

Checks if a date comes after another date. If no date argument is provided the current time will be used. The value must be a Date object or a string that can be evaluated by Date.parse.

`after`

*   est optionnel

*   peut être nul

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

*   peut être nul

### Type de alpha

`string`

### Contraintes de alpha

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur      | Explication |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |
| `null`      |             |

### Exemple de alpha

```yaml
latin

```

## alphanumeric

Checks if a value is only made of alphabetical characters or numeric digits. For the alphabetical portion you can pass default or latin - see alpha.

`alphanumeric`

*   est optionnel

*   peut être nul

### Type de alphanumeric

`string`

### Contraintes de alphanumeric

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur      | Explication |
| :---------- | :---------- |
| `"latin"`   |             |
| `"default"` |             |
| `null`      |             |

## bail

Used to logically stop validation on the first subsequent validation error.

`bail`

*   est optionnel

*   peut être nul

### Type de bail

`null`, la valeur doit être nulle

## before

Checks if a date comes before another date. If no date argument is provided the current time will be used. The value must be a Date object or a string that can be evaluated by Date.parse.

`before`

*   est optionnel

*   peut être nul

### Type de before

`string`

### Exemple de before

```yaml
'2020-12-31'

```

## between

Checks if a number or string length is between a minimum or maximum. Both the maximum and minimum are exclusive. If the value being validated is a string the string’s length is used for comparison. If a number is used, the numeric value is used for comparison. In v2.2.4+ you can force it to always check the numeric value or string length by setting an optional third argument to value or length.

`between`

*   est optionnel

*   ne peut être nul

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

*   peut être nul

### Type de confirm

`string`

### Exemple de confirm

```yaml
confirm:other_field

```

## date

Checks if the input is a valid date according to Date.parse(), or if a format argument is provided, it will validate according to the given format.

`date`

*   est optionnel

*   peut être nul

### Type de date

`string`

### Exemple de date

```yaml
YYYY

```

```yaml
YY

```

```yaml
MM

```

```yaml
M

```

```yaml
DD

```

```yaml
D

```

```yaml
YYYY-MM-DD

```

```yaml
DD/MM/YYYY

```

```yaml
YYYY-MM

```

## email

Checks if the input is a valid email address format.

`email`

*   est optionnel

*   peut être nul

### Type de email

`null`, la valeur doit être nulle

## endsWith

Checks if the input ends with one of the provided options.

`endsWith`

*   est optionnel

*   ne peut être nul

### Type de endsWith

`string`

## in

Checks if the input is included in an array of options.

`in`

*   est optionnel

*   ne peut être nul

### Type de in

`string`

## matches

Checks if the input matches a particular value or pattern. If you pass multiple arguments, it checks each until a match is found.

`matches`

*   est optionnel

*   ne peut être nul

### Type de matches

`string`

### Exemple de matches

```yaml
val1,val2

```

```yaml
/[0-9]/

```

## max

Checks that the value of a Number, or length of a String or Array is less than a maximum length or value. The maximum value/length defaults to 10.

`max`

*   est optionnel

*   ne peut être nul

### Type de max

l'un des éléments suivants :`string` ou `number` ([Détails](frw-form-definitions-composant-interaction-properties-validation-properties-max.md))

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

*   ne peut être nul

### Type de mime

`string`

### Exemple de mime

```yaml
image/png

```

```yaml
image/jpeg

```

## min

Checks the value of a Number, or length of a String or Array is more than a maximum length or value. The minimum value/length defaults to 1. You can force the validator to evaluate length or value by passing a second argument of either length or value.

`min`

*   est optionnel

*   peut être nul

### Type de min

l'un des éléments suivants :`string` ou `number` ([Détails](frw-form-definitions-composant-interaction-properties-validation-properties-min.md))

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

## not

Checks to ensure the input data does not match a set of predefined values.

`not`

*   est optionnel

*   ne peut être nul

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

*   peut être nul

### Type de number

`null`, la valeur doit être nulle

## optional

Use this rule to make a field optional. When used all validation rules pass until the field is no longer empty. Its location in the list of validation rules has no effect.

`optional`

*   est optionnel

*   peut être nul

### Type de optional

`null`, la valeur doit être nulle

## url

Checks if the input value appears to be a properly formatted URL including the protocol. This does not check if the URL actually resolves.

`url`

*   est optionnel

*   peut être nul

### Type de url

`null`, la valeur doit être nulle

## startsWith

Checks if the input starts with one of the provided options.

`startsWith`

*   est optionnel

*   ne peut être nul

### Type de startsWith

`string`

## avant

Pour une date qui doit être AVANT la date du jour.

`avant`

*   est optionnel

*   peut être nul

### Type de avant

`string`

## nam

Valide le NAM, si true valide selon un algorithme avec chiffre validateur, si false valide seulement le format du NAM sans l'algorithme de chiffre validateur.

`nam`

*   est optionnel

*   ne peut être nul

### Type de nam

`boolean`

## nas

Valide le NAS, si true valide selon un algorithme avec chiffre validateur, si false valide seulement le format du NAS sans l'algorithme de chiffre validateur.

`nas`

*   est optionnel

*   ne peut être nul

### Type de nas

`boolean`

## Modèle:`^[a-z][a-z0-9A-Z]{1,99}Custom$`



`^[a-z][a-z0-9A-Z]{1,99}Custom$`

*   est optionnel

*   peut être nul

### Type de ^\[a-z]\[a-z0-9A-Z]{1,99}Custom$

l'un des éléments suivants :`string` ou `boolean` ou `number` ou `integer` ([Détails](frw-form-definitions-composant-interaction-properties-validation-patternproperties-a-za-z0-9a-z199custom.md))
