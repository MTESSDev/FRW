# Untitled schema Schema

```txt
https://example.com/schemas/custom
```



| Abstract               | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                 |
| :--------------------- | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :------------------------------------------------------------------------- |
| Cannot be instantiated | Yes        | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [FRW.form.schema.json](../out/FRW.form.schema.json "open original schema") |

## Untitled schema Type

unknown

# Untitled schema Definitions

## Definitions group EcsForm

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/EcsForm"}
```

| Property                                                                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                      |
| :------------------------------------------------------------------------------------ | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherMessageSauvegardeCourrielReprise](#affichermessagesauvegardecourrielreprise) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-ecsform-properties-affichermessagesauvegardecourrielreprise.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/afficherMessageSauvegardeCourrielReprise") |
| [form](#form)                                                                         | `object`  | Required | cannot be null | [Untitled schema](frw-definitions-form.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/form")                                                                                            |
| [config](#config)                                                                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/config")                                                                   |
| [textes](#textes)                                                                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-ecsform-properties-textes.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/textes")                                                                     |

### afficherMessageSauvegardeCourrielReprise

DEPRECATED (Utiliser maintenant enregistrement.afficherMessageIncitatif)

`afficherMessageSauvegardeCourrielReprise`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-ecsform-properties-affichermessagesauvegardecourrielreprise.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/afficherMessageSauvegardeCourrielReprise")

#### afficherMessageSauvegardeCourrielReprise Type

`boolean`

### form

Élément racine d'un formulaire.

`form`

*   is required

*   Type: `object` ([Form](frw-definitions-form.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/form")

#### form Type

`object` ([Form](frw-definitions-form.md))

### config



`config`

*   is optional

*   Type: `object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/config")

#### config Type

`object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

### textes



`textes`

*   is optional

*   Type: `object` ([Details](frw-definitions-ecsform-properties-textes.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-ecsform-properties-textes.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/textes")

#### textes Type

`object` ([Details](frw-definitions-ecsform-properties-textes.md))

## Definitions group Form

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Form"}
```

| Property                                    | Type     | Required | Nullable       | Defined by                                                                                                                                                      |
| :------------------------------------------ | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sectionsGroup](#sectionsgroup)             | `array`  | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-sectionsgroup.md "https://example.com/schemas/custom#/definitions/Form/properties/sectionsGroup")             |
| [templates](#templates)                     | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-templates.md "https://example.com/schemas/custom#/definitions/Form/properties/templates")                     |
| [title](#title)                             | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Form/properties/title")                                       |
| [inputDefaultClasses](#inputdefaultclasses) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-inputdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/inputDefaultClasses") |
| [defaults](#defaults)                       | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-defaults-values.md "https://example.com/schemas/custom#/definitions/Form/properties/defaults")                                |
| [outerDefaultClasses](#outerdefaultclasses) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-form-properties-outerdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/outerDefaultClasses") |

### sectionsGroup



`sectionsGroup`

*   is optional

*   Type: `object[]` ([Section Group](frw-definitions-section-group.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-sectionsgroup.md "https://example.com/schemas/custom#/definitions/Form/properties/sectionsGroup")

#### sectionsGroup Type

`object[]` ([Section Group](frw-definitions-section-group.md))

### templates



`templates`

*   is optional

*   Type: `object` ([Details](frw-definitions-form-properties-templates.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-templates.md "https://example.com/schemas/custom#/definitions/Form/properties/templates")

#### templates Type

`object` ([Details](frw-definitions-form-properties-templates.md))

### title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Form/properties/title")

#### title Type

`object` ([Translation](frw-definitions-translation.md))

#### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### inputDefaultClasses



`inputDefaultClasses`

*   is optional

*   Type: `object` ([Details](frw-definitions-form-properties-inputdefaultclasses.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-inputdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/inputDefaultClasses")

#### inputDefaultClasses Type

`object` ([Details](frw-definitions-form-properties-inputdefaultclasses.md))

### defaults



`defaults`

*   is optional

*   Type: `object` ([Defaults values](frw-definitions-defaults-values.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-defaults-values.md "https://example.com/schemas/custom#/definitions/Form/properties/defaults")

#### defaults Type

`object` ([Defaults values](frw-definitions-defaults-values.md))

### outerDefaultClasses



`outerDefaultClasses`

*   is optional

*   Type: `object` ([Details](frw-definitions-form-properties-outerdefaultclasses.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form-properties-outerdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/outerDefaultClasses")

#### outerDefaultClasses Type

`object` ([Details](frw-definitions-form-properties-outerdefaultclasses.md))

## Definitions group Section

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Section"}
```

| Property                                                                            | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                    |
| :---------------------------------------------------------------------------------- | :-------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [section](#section)                                                                 | `object`  | Required | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Section/properties/section")                                                                                |
| [id](#id)                                                                           | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-id.md "https://example.com/schemas/custom#/definitions/Section/properties/id")                                                                           |
| [cacherTexteExplicatifChampsObligatoires](#cachertexteexplicatifchampsobligatoires) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "https://example.com/schemas/custom#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires") |
| [classes](#classes)                                                                 | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-classes.md "https://example.com/schemas/custom#/definitions/Section/properties/classes")                                                                 |
| [v-if](#v-if)                                                                       | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-v-if.md "https://example.com/schemas/custom#/definitions/Section/properties/v-if")                                                                       |
| [components](#components)                                                           | `array`   | Optional | cannot be null | [Untitled schema](frw-definitions-section-properties-components.md "https://example.com/schemas/custom#/definitions/Section/properties/components")                                                           |

### section

Multilingue

`section`

*   is required

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Section/properties/section")

#### section Type

`object` ([Translation](frw-definitions-translation.md))

#### section Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### id



`id`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-id.md "https://example.com/schemas/custom#/definitions/Section/properties/id")

#### id Type

`string`

### cacherTexteExplicatifChampsObligatoires

Permet d'afficher l'indication de champs obligatoires.

`cacherTexteExplicatifChampsObligatoires`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "https://example.com/schemas/custom#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires")

#### cacherTexteExplicatifChampsObligatoires Type

`boolean`

### classes



`classes`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-classes.md "https://example.com/schemas/custom#/definitions/Section/properties/classes")

#### classes Type

`string`

### v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-v-if.md "https://example.com/schemas/custom#/definitions/Section/properties/v-if")

#### v-if Type

`string`

### components



`components`

*   is optional

*   Type: an array of merged types ([Details](frw-definitions-section-properties-components-items.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-properties-components.md "https://example.com/schemas/custom#/definitions/Section/properties/components")

#### components Type

an array of merged types ([Details](frw-definitions-section-properties-components-items.md))

## Definitions group SectionsGroup

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/SectionsGroup"}
```

| Property                      | Type     | Required | Nullable       | Defined by                                                                                                                                                  |
| :---------------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sections](#sections)         | `array`  | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-sections.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sections") |
| [prefixId](#prefixid)         | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-prefixid.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/prefixId") |
| [classes](#classes-1)         | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-classes.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/classes")   |
| [v-if](#v-if-1)               | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-section-group-properties-v-if.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/v-if")         |
| [sectionGroup](#sectiongroup) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sectionGroup")                   |

### sections



`sections`

*   is optional

*   Type: `object[]` ([Section](frw-definitions-section.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-sections.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sections")

#### sections Type

`object[]` ([Section](frw-definitions-section.md))

### prefixId



`prefixId`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-prefixid.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/prefixId")

#### prefixId Type

`string`

### classes



`classes`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-classes.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/classes")

#### classes Type

`string`

### v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-section-group-properties-v-if.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/v-if")

#### v-if Type

`string`

### sectionGroup

Multilingue

`sectionGroup`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sectionGroup")

#### sectionGroup Type

`object` ([Translation](frw-definitions-translation.md))

#### sectionGroup Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## Definitions group Display

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Display"}
```

| Property                              | Type      | Required | Nullable       | Defined by                                                                                                                                                      |
| :------------------------------------ | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [type](#type)                         | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-type.md "https://example.com/schemas/custom#/definitions/Display/properties/type")                         |
| [classes](#classes-2)                 | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-classes.md "https://example.com/schemas/custom#/definitions/Display/properties/classes")                   |
| [afficherBlocCode](#afficherbloccode) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Display/properties/afficherBlocCode") |
| [tag](#tag)                           | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-tag.md "https://example.com/schemas/custom#/definitions/Display/properties/tag")                           |
| [src](#src)                           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/src")                                      |
| [base64](#base64)                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/base64")                                   |
| [text](#text)                         | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/text")                                     |
| [title](#title-1)                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/title")                                    |
| [additionals](#additionals)           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-additionals.md "https://example.com/schemas/custom#/definitions/Display/properties/additionals")           |
| [alt](#alt)                           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/alt")                                      |
| [v-if](#v-if-2)                       | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-v-if.md "https://example.com/schemas/custom#/definitions/Display/properties/v-if")                         |
| [components](#components-1)           | `array`   | Optional | cannot be null | [Untitled schema](frw-definitions-display-properties-components.md "https://example.com/schemas/custom#/definitions/Display/properties/components")             |

### type

Types from custom templates list.

`type`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-type.md "https://example.com/schemas/custom#/definitions/Display/properties/type")

#### type Type

`string`

#### type Examples

```json
"inline"
```

```json
"dynamic"
```

```json
"bandeau"
```

```json
"bandeau-notification"
```

```json
"image"
```

```json
"avis"
```

```json
"accordeon"
```

### classes



`classes`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-classes.md "https://example.com/schemas/custom#/definitions/Display/properties/classes")

#### classes Type

`string`

### afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   is optional

*   Type: `boolean` ([afficherBlocCode](frw-definitions-display-properties-afficherbloccode.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Display/properties/afficherBlocCode")

#### afficherBlocCode Type

`boolean` ([afficherBlocCode](frw-definitions-display-properties-afficherbloccode.md))

### tag



`tag`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-tag.md "https://example.com/schemas/custom#/definitions/Display/properties/tag")

#### tag Type

`string`

### src

Multilingue

`src`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/src")

#### src Type

`object` ([Translation](frw-definitions-translation.md))

#### src Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### base64

Multilingue

`base64`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/base64")

#### base64 Type

`object` ([Translation](frw-definitions-translation.md))

#### base64 Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### text

Multilingue

`text`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/text")

#### text Type

`object` ([Translation](frw-definitions-translation.md))

#### text Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/title")

#### title Type

`object` ([Translation](frw-definitions-translation.md))

#### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### additionals



`additionals`

*   is optional

*   Type: `object` ([Details](frw-definitions-display-properties-additionals.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-additionals.md "https://example.com/schemas/custom#/definitions/Display/properties/additionals")

#### additionals Type

`object` ([Details](frw-definitions-display-properties-additionals.md))

### alt

Multilingue

`alt`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/alt")

#### alt Type

`object` ([Translation](frw-definitions-translation.md))

#### alt Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-v-if.md "https://example.com/schemas/custom#/definitions/Display/properties/v-if")

#### v-if Type

`string`

### components



`components`

*   is optional

*   Type: an array of merged types ([Details](frw-definitions-display-properties-components-items.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-display-properties-components.md "https://example.com/schemas/custom#/definitions/Display/properties/components")

#### components Type

an array of merged types ([Details](frw-definitions-display-properties-components-items.md))

## Definitions group Input

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Input"}
```

| Property                                    | Type      | Required | Nullable       | Defined by                                                                                                                                                                                             |
| :------------------------------------------ | :-------- | :------- | :------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                               | `string`  | Required | cannot be null | [Untitled schema](frw-definitions-input-properties-name.md "https://example.com/schemas/custom#/definitions/Input/properties/name")                                                                    |
| [type](#type-1)                             | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-type.md "https://example.com/schemas/custom#/definitions/Input/properties/type")                                                                    |
| [value](#value)                             | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-value.md "https://example.com/schemas/custom#/definitions/Input/properties/value")                                                                  |
| [limit](#limit)                             | `number`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-limit.md "https://example.com/schemas/custom#/definitions/Input/properties/limit")                                                                  |
| [validation-name](#validation-name)         | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-name")                                                                   |
| [validation-messages](#validation-messages) | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-messages") |
| [label](#label)                             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/label")                                                                             |
| [placeholder](#placeholder)                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/placeholder")                                                                       |
| [inputClasses](#inputclasses)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-inputclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/inputClasses")                                                    |
| [inputmode](#inputmode)                     | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-inputmode.md "https://example.com/schemas/custom#/definitions/Input/properties/inputmode")                                                          |
| [pattern](#pattern)                         | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-pattern.md "https://example.com/schemas/custom#/definitions/Input/properties/pattern")                                                              |
| [outerClasses](#outerclasses)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-outerclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/outerClasses")                                                    |
| [help](#help)                               | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/help")                                                                              |
| [pdfBind](#pdfbind)                         | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-pdfbind.md "https://example.com/schemas/custom#/definitions/Input/properties/pdfBind")                                                              |
| [additionals](#additionals-1)               | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-additionals.md "https://example.com/schemas/custom#/definitions/Input/properties/additionals")                                                      |
| [v-if](#v-if-3)                             | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-v-if.md "https://example.com/schemas/custom#/definitions/Input/properties/v-if")                                                                    |
| [v-else-value](#v-else-value)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-v-else-value.md "https://example.com/schemas/custom#/definitions/Input/properties/v-else-value")                                                    |
| [helpPosition](#helpposition)               | `string`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-helpposition.md "https://example.com/schemas/custom#/definitions/Input/properties/helpPosition")                                                    |
| [min](#min)                                 | Multiple  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/min")                                                                      |
| [max](#max)                                 | Multiple  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/max")                                                                      |
| [addLabel](#addlabel)                       | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/addLabel")                                                                          |
| [removeLabel](#removelabel)                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/removeLabel")                                                                       |
| [instanceLabel](#instancelabel)             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/instanceLabel")                                                                     |
| [tooltip](#tooltip)                         | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation-1.md "https://example.com/schemas/custom#/definitions/Input/properties/tooltip")                                                                         |
| [options](#options)                         | Multiple  | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-options.md "https://example.com/schemas/custom#/definitions/Input/properties/options")                                                              |
| [nomDocument](#nomdocument)                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/nomDocument")                                                                       |
| [afficherBlocCode](#afficherbloccode-1)     | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Input/properties/afficherBlocCode")                                            |
| [validations](#validations)                 | `object`  | Optional | can be null    | [Untitled schema](frw-definitions-input-properties-validation.md "https://example.com/schemas/custom#/definitions/Input/properties/validations")                                                       |
| [repeatable](#repeatable)                   | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-repeatable.md "https://example.com/schemas/custom#/definitions/Input/properties/repeatable")                                                        |
| [minimum](#minimum)                         | `number`  | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-minimum.md "https://example.com/schemas/custom#/definitions/Input/properties/minimum")                                                              |
| [components](#components-2)                 | `array`   | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-components.md "https://example.com/schemas/custom#/definitions/Input/properties/components")                                                        |
| [disabled](#disabled)                       | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-input-properties-disabled.md "https://example.com/schemas/custom#/definitions/Input/properties/disabled")                                                            |

### name

Adds a name attribute, and when used with <FormulateForm> this is the key of the field. If no name is defined a random hash will be assigned

`name`

*   is required

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-name.md "https://example.com/schemas/custom#/definitions/Input/properties/name")

#### name Type

`string`

### type

Required. The type of input element. See the input library for a full range of options.

`type`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-type.md "https://example.com/schemas/custom#/definitions/Input/properties/type")

#### type Type

`string`

#### type Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value                    | Explanation |
| :----------------------- | :---------- |
| `"listeDeroulante"`      |             |
| `"text"`                 |             |
| `"codePostal"`           |             |
| `"cp12"`                 |             |
| `"nam"`                  |             |
| `"nas"`                  |             |
| `"montant"`              |             |
| `"adresse"`              |             |
| `"button"`               |             |
| `"submit"`               |             |
| `"customfile"`           |             |
| `"customfileUlterieure"` |             |
| `"file"`                 |             |
| `"group"`                |             |
| `"repeatableGroup"`      |             |
| `"radio"`                |             |
| `"checkbox"`             |             |
| `"select"`               |             |
| `"number"`               |             |
| `"range"`                |             |
| `"textarea"`             |             |
| `"color"`                |             |
| `"date"`                 |             |
| `"datetime-local"`       |             |
| `"email"`                |             |
| `"hidden"`               |             |
| `"month"`                |             |
| `"password"`             |             |
| `"search"`               |             |
| `"tel"`                  |             |
| `"time"`                 |             |
| `"url"`                  |             |
| `"week"`                 |             |

#### type Default Value

The default value is:

```json
"text"
```

### value



`value`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-value.md "https://example.com/schemas/custom#/definitions/Input/properties/value")

#### value Type

`string`

### limit



`limit`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-limit.md "https://example.com/schemas/custom#/definitions/Input/properties/limit")

#### limit Type

`number`

### validation-name

Multilingue

`validation-name`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-name")

#### validation-name Type

`object` ([Translation](frw-definitions-translation.md))

#### validation-name Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### validation-messages



`validation-messages`

*   is optional

*   Type: `object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-messages")

#### validation-messages Type

`object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md))

### label

Multilingue

`label`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/label")

#### label Type

`object` ([Translation](frw-definitions-translation.md))

#### label Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### placeholder

Multilingue

`placeholder`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/placeholder")

#### placeholder Type

`object` ([Translation](frw-definitions-translation.md))

#### placeholder Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### inputClasses



`inputClasses`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-inputclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/inputClasses")

#### inputClasses Type

`string`

### inputmode

Text field inputmode (html)

`inputmode`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-inputmode.md "https://example.com/schemas/custom#/definitions/Input/properties/inputmode")

#### inputmode Type

`string`

#### inputmode Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value      | Explanation |
| :--------- | :---------- |
| `"number"` |             |

### pattern

Regex pattern (html)

`pattern`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-pattern.md "https://example.com/schemas/custom#/definitions/Input/properties/pattern")

#### pattern Type

`string`

### outerClasses



`outerClasses`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-outerclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/outerClasses")

#### outerClasses Type

`string`

### help

Multilingue

`help`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/help")

#### help Type

`object` ([Translation](frw-definitions-translation.md))

#### help Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### pdfBind



`pdfBind`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-pdfbind.md "https://example.com/schemas/custom#/definitions/Input/properties/pdfBind")

#### pdfBind Type

`string`

### additionals



`additionals`

*   is optional

*   Type: `object` ([Details](frw-definitions-input-properties-additionals.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-additionals.md "https://example.com/schemas/custom#/definitions/Input/properties/additionals")

#### additionals Type

`object` ([Details](frw-definitions-input-properties-additionals.md))

### v-if

Conditionnal display on another property/form field.

`v-if`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-v-if.md "https://example.com/schemas/custom#/definitions/Input/properties/v-if")

#### v-if Type

`string`

### v-else-value

Valeur de remplacement lorsque le v-if n'affiche pas le champ. Supporté CÔTÉ SERVEUR UNIQUEMENT.

`v-else-value`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-v-else-value.md "https://example.com/schemas/custom#/definitions/Input/properties/v-else-value")

#### v-else-value Type

`string`

### helpPosition



`helpPosition`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-helpposition.md "https://example.com/schemas/custom#/definitions/Input/properties/helpPosition")

#### helpPosition Type

`string`

#### helpPosition Constraints

**enum**: the value of this property must be equal to one of the following values:

| Value      | Explanation |
| :--------- | :---------- |
| `"before"` |             |
| `"after"`  |             |

### min



`min`

*   is optional

*   Type: any of the following: `string` or `number` ([Details](frw-definitions-input-properties-min.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/min")

#### min Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-min.md))

### max



`max`

*   is optional

*   Type: any of the following: `string` or `number` ([Details](frw-definitions-input-properties-max.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/max")

#### max Type

any of the following: `string` or `number` ([Details](frw-definitions-input-properties-max.md))

### addLabel

Multilingue

`addLabel`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/addLabel")

#### addLabel Type

`object` ([Translation](frw-definitions-translation.md))

#### addLabel Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### removeLabel

Multilingue

`removeLabel`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/removeLabel")

#### removeLabel Type

`object` ([Translation](frw-definitions-translation.md))

#### removeLabel Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### instanceLabel

Multilingue

`instanceLabel`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/instanceLabel")

#### instanceLabel Type

`object` ([Translation](frw-definitions-translation.md))

#### instanceLabel Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### tooltip



`tooltip`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation-1.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation-1.md "https://example.com/schemas/custom#/definitions/Input/properties/tooltip")

#### tooltip Type

`object` ([Translation](frw-definitions-translation-1.md))

#### tooltip Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### options

Array or object of options (select or box classifications)

`options`

*   is optional

*   Type: any of the following: `object` or `string` or `array` ([Details](frw-definitions-input-properties-options.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-options.md "https://example.com/schemas/custom#/definitions/Input/properties/options")

#### options Type

any of the following: `object` or `string` or `array` ([Details](frw-definitions-input-properties-options.md))

#### options Examples

```json
"yesno"
```

### nomDocument

Multilingue

`nomDocument`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/nomDocument")

#### nomDocument Type

`object` ([Translation](frw-definitions-translation.md))

#### nomDocument Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   is optional

*   Type: `boolean` ([afficherBlocCode](frw-definitions-input-properties-afficherbloccode.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Input/properties/afficherBlocCode")

#### afficherBlocCode Type

`boolean` ([afficherBlocCode](frw-definitions-input-properties-afficherbloccode.md))

### validations



`validations`

*   is optional

*   Type: `object` ([Validation](frw-definitions-input-properties-validation.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-input-properties-validation.md "https://example.com/schemas/custom#/definitions/Input/properties/validations")

#### validations Type

`object` ([Validation](frw-definitions-input-properties-validation.md))

#### validations Default Value

The default value is:

```json
{}
```

### repeatable



`repeatable`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-repeatable.md "https://example.com/schemas/custom#/definitions/Input/properties/repeatable")

#### repeatable Type

`boolean`

### minimum



`minimum`

*   is optional

*   Type: `number`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-minimum.md "https://example.com/schemas/custom#/definitions/Input/properties/minimum")

#### minimum Type

`number`

### components



`components`

*   is optional

*   Type: an array of merged types ([Details](frw-definitions-input-properties-components-items.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-components.md "https://example.com/schemas/custom#/definitions/Input/properties/components")

#### components Type

an array of merged types ([Details](frw-definitions-input-properties-components-items.md))

### disabled



`disabled`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-input-properties-disabled.md "https://example.com/schemas/custom#/definitions/Input/properties/disabled")

#### disabled Type

`boolean`

## Definitions group Translation

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Translation"}
```

| Property              | Type     | Required | Nullable    | Defined by                                                                                                                                  |
| :-------------------- | :------- | :------- | :---------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| [fr](#fr)             | `string` | Required | can be null | [Untitled schema](frw-definitions-translation-properties-fr.md "https://example.com/schemas/custom#/definitions/Translation/properties/fr") |
| [en](#en)             | `string` | Optional | can be null | [Untitled schema](frw-definitions-translation-properties-en.md "https://example.com/schemas/custom#/definitions/Translation/properties/en") |
| Additional Properties | Any      | Optional | can be null |                                                                                                                                             |

### fr

Texte de langue française.

`fr`

*   is required

*   Type: `string` ([fr](frw-definitions-translation-properties-fr.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-translation-properties-fr.md "https://example.com/schemas/custom#/definitions/Translation/properties/fr")

#### fr Type

`string` ([fr](frw-definitions-translation-properties-fr.md))

### en

Texte de langue anglaise.

`en`

*   is optional

*   Type: `string` ([en](frw-definitions-translation-properties-en.md))

*   can be null

*   defined in: [Untitled schema](frw-definitions-translation-properties-en.md "https://example.com/schemas/custom#/definitions/Translation/properties/en")

#### en Type

`string` ([en](frw-definitions-translation-properties-en.md))

### Additional Properties

Additional properties are allowed and do not have to follow a specific schema

## Definitions group Tooltip

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Tooltip"}
```

| Property              | Type     | Required | Nullable       | Defined by                                                                                                                   |
| :-------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| [title](#title-2)     | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/title") |
| [text](#text-1)       | `object` | Required | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/text")  |
| Additional Properties | Any      | Optional | can be null    |                                                                                                                              |

### title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/title")

#### title Type

`object` ([Translation](frw-definitions-translation.md))

#### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### text

Multilingue

`text`

*   is required

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/text")

#### text Type

`object` ([Translation](frw-definitions-translation.md))

#### text Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### Additional Properties

Additional properties are allowed and do not have to follow a specific schema

## Definitions group Defaults

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Defaults"}
```

| Property              | Type | Required | Nullable    | Defined by |
| :-------------------- | :--- | :------- | :---------- | :--------- |
| Additional Properties | Any  | Optional | can be null |            |

### Additional Properties

Additional properties are allowed and do not have to follow a specific schema

## Definitions group Config

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Config"}
```

| Property                                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                               |
| :---------------------------------------------------- | :-------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherBlocCode](#afficherbloccode-2)               | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherBlocCode")       |
| [afficherPartagePage](#afficherpartagepage)           | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherPartagePage") |
| [confirmationTransmission](#confirmationtransmission) | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-confirmation-de-transmission.md "https://example.com/schemas/custom#/definitions/Config/properties/confirmationTransmission")                          |
| [courrielReprise](#courrielreprise)                   | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-courrielreprise.md "https://example.com/schemas/custom#/definitions/Config/properties/courrielReprise")                                                |
| [debuterFormulaire](#debuterformulaire)               | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-debuterformulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/debuterFormulaire")                                            |
| [enregistrement](#enregistrement)                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-enregistrement.md "https://example.com/schemas/custom#/definitions/Config/properties/enregistrement")                                                  |
| [formulaireUnilingue](#formulaireunilingue)           | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-formulaireunilingue.md "https://example.com/schemas/custom#/definitions/Config/properties/formulaireUnilingue") |
| [gererPlageDisponibilite](#gererplagedisponibilite)   | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité.md "https://example.com/schemas/custom#/definitions/Config/properties/gererPlageDisponibilite")                      |
| [injecterJs](#injecterjs)                             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/injecterJs")                              |
| [messages](#messages)                                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-messages.md "https://example.com/schemas/custom#/definitions/Config/properties/messages")                                                              |
| [pages](#pages)                                       | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-pages.md "https://example.com/schemas/custom#/definitions/Config/properties/pages")                                                                    |
| [piv](#piv)                                           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-piv.md "https://example.com/schemas/custom#/definitions/Config/properties/piv")                                 |
| [revision](#revision)                                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-page-de-révision.md "https://example.com/schemas/custom#/definitions/Config/properties/revision")                                                      |
| [scripts](#scripts)                                   | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-scripts.md "https://example.com/schemas/custom#/definitions/Config/properties/scripts")                                                                |
| [securite](#securite)                                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-sécurité-du-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/securite")                                                |
| [soumission](#soumission)                             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-page-de-soumission.md "https://example.com/schemas/custom#/definitions/Config/properties/soumission")                                                  |
| [title](#title-3)                                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Config/properties/title")                                                              |

### afficherBlocCode

(Réservé) Afficher un bloc de code des éléments du formulaire.

`afficherBlocCode`

*   is optional

*   Type: `boolean` ([afficherBlocCode](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherBlocCode")

#### afficherBlocCode Type

`boolean` ([afficherBlocCode](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

### afficherPartagePage

(Avancé) ajouter un bouton partage dans toutes les pages à la droite du titre de la page.

`afficherPartagePage`

*   is optional

*   Type: `boolean` ([afficherPartagePage](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherPartagePage")

#### afficherPartagePage Type

`boolean` ([afficherPartagePage](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

### confirmationTransmission



`confirmationTransmission`

*   is optional

*   Type: `object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-confirmation-de-transmission.md "https://example.com/schemas/custom#/definitions/Config/properties/confirmationTransmission")

#### confirmationTransmission Type

`object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

### courrielReprise

Paramètres associés au courriel de reprise.

`courrielReprise`

*   is optional

*   Type: `object` ([courrielReprise](frw-definitions-courrielreprise.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-courrielreprise.md "https://example.com/schemas/custom#/definitions/Config/properties/courrielReprise")

#### courrielReprise Type

`object` ([courrielReprise](frw-definitions-courrielreprise.md))

### debuterFormulaire

Paramètres de la page permettant de débuter un formulaire.

`debuterFormulaire`

*   is optional

*   Type: `object` ([debuterFormulaire](frw-definitions-debuterformulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-debuterformulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/debuterFormulaire")

#### debuterFormulaire Type

`object` ([debuterFormulaire](frw-definitions-debuterformulaire.md))

### enregistrement

Paramètres associés à l'enregistrement d'un formulaire

`enregistrement`

*   is optional

*   Type: `object` ([enregistrement](frw-definitions-enregistrement.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-enregistrement.md "https://example.com/schemas/custom#/definitions/Config/properties/enregistrement")

#### enregistrement Type

`object` ([enregistrement](frw-definitions-enregistrement.md))

### formulaireUnilingue

Permet de retirer le selecteur de langue. Le formulaire s'affichera en français seulement.

`formulaireUnilingue`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-formulaireunilingue.md "https://example.com/schemas/custom#/definitions/Config/properties/formulaireUnilingue")

#### formulaireUnilingue Type

`boolean`

### gererPlageDisponibilite



`gererPlageDisponibilite`

*   is optional

*   Type: `object` ([Gerer les plages de disponibilité](frw-definitions-gerer-les-plages-de-disponibilité.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité.md "https://example.com/schemas/custom#/definitions/Config/properties/gererPlageDisponibilite")

#### gererPlageDisponibilite Type

`object` ([Gerer les plages de disponibilité](frw-definitions-gerer-les-plages-de-disponibilité.md))

### injecterJs



`injecterJs`

*   is optional

*   Type: `object` ([Scripts Vue.js à injecter au formulaire.](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/injecterJs")

#### injecterJs Type

`object` ([Scripts Vue.js à injecter au formulaire.](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

### messages

Paramètres associés aux différents messages.

`messages`

*   is optional

*   Type: `object` ([messages](frw-definitions-messages.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-messages.md "https://example.com/schemas/custom#/definitions/Config/properties/messages")

#### messages Type

`object` ([messages](frw-definitions-messages.md))

### pages

Paramètres associés à différentes pages.

`pages`

*   is optional

*   Type: `object` ([pages](frw-definitions-pages.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-pages.md "https://example.com/schemas/custom#/definitions/Config/properties/pages")

#### pages Type

`object` ([pages](frw-definitions-pages.md))

### piv

Paramètres associés au PIV.

`piv`

*   is optional

*   Type: `object` ([piv](frw-definitions-configuration-du-formulaire-properties-piv.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-piv.md "https://example.com/schemas/custom#/definitions/Config/properties/piv")

#### piv Type

`object` ([piv](frw-definitions-configuration-du-formulaire-properties-piv.md))

### revision



`revision`

*   is optional

*   Type: `object` ([Page de révision](frw-definitions-page-de-révision.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-page-de-révision.md "https://example.com/schemas/custom#/definitions/Config/properties/revision")

#### revision Type

`object` ([Page de révision](frw-definitions-page-de-révision.md))

### scripts

(Avancé) Paramètres d'injection de javascript.

`scripts`

*   is optional

*   Type: `object` ([scripts](frw-definitions-scripts.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-scripts.md "https://example.com/schemas/custom#/definitions/Config/properties/scripts")

#### scripts Type

`object` ([scripts](frw-definitions-scripts.md))

### securite



`securite`

*   is optional

*   Type: `object` ([Sécurité du formulaire](frw-definitions-sécurité-du-formulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-sécurité-du-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/securite")

#### securite Type

`object` ([Sécurité du formulaire](frw-definitions-sécurité-du-formulaire.md))

### soumission



`soumission`

*   is optional

*   Type: `object` ([Page de soumission](frw-definitions-page-de-soumission.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-page-de-soumission.md "https://example.com/schemas/custom#/definitions/Config/properties/soumission")

#### soumission Type

`object` ([Page de soumission](frw-definitions-page-de-soumission.md))

### title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Config/properties/title")

#### title Type

`object` ([Translation](frw-definitions-translation.md))

#### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## Definitions group Securite

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Securite"}
```

| Property                      | Type      | Required | Nullable       | Defined by                                                                                                                                                              |
| :---------------------------- | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [accesAnonyme](#accesanonyme) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-sécurité-du-formulaire-properties-accesanonyme.md "https://example.com/schemas/custom#/definitions/Securite/properties/accesAnonyme") |

### accesAnonyme

Permet d'activer l'accès anonyme au formulaire.

`accesAnonyme`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-sécurité-du-formulaire-properties-accesanonyme.md "https://example.com/schemas/custom#/definitions/Securite/properties/accesAnonyme")

#### accesAnonyme Type

`boolean`

## Definitions group Enregistrement

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Enregistrement"}
```

| Property                                                                      | Type      | Required | Nullable       | Defined by                                                                                                                                                                                    |
| :---------------------------------------------------------------------------- | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)                                                               | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-enregistrement-properties-actif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/actif")                                       |
| [afficherMessageIncitatif](#affichermessageincitatif)                         | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-enregistrement-properties-affichermessageincitatif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/afficherMessageIncitatif") |
| [texteModaleEnregistrementAuthentifie](#textemodaleenregistrementauthentifie) | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")                            |

### actif

Indique si l'enregistrement du formulaire est actif (bouton enregistré présent et enregistrement au changement de page).

`actif`

*   is optional

*   Type: `boolean` ([actif](frw-definitions-enregistrement-properties-actif.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-enregistrement-properties-actif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/actif")

#### actif Type

`boolean` ([actif](frw-definitions-enregistrement-properties-actif.md))

### afficherMessageIncitatif

Indique si le message (avis avertissement en haut de chaque page) incitant l'enregistrement est affiché ou non.

`afficherMessageIncitatif`

*   is optional

*   Type: `boolean` ([afficherMessageIncitatif](frw-definitions-enregistrement-properties-affichermessageincitatif.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-enregistrement-properties-affichermessageincitatif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/afficherMessageIncitatif")

#### afficherMessageIncitatif Type

`boolean` ([afficherMessageIncitatif](frw-definitions-enregistrement-properties-affichermessageincitatif.md))

### texteModaleEnregistrementAuthentifie

Multilingue

`texteModaleEnregistrementAuthentifie`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")

#### texteModaleEnregistrementAuthentifie Type

`object` ([Translation](frw-definitions-translation.md))

#### texteModaleEnregistrementAuthentifie Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## Definitions group GererPlageDisponibilite

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/GererPlageDisponibilite"}
```

| Property                                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                                |
| :---------------------------------------------------- | :-------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [actif](#actif-1)                                     | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-actif.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/actif")                                       |
| [joursOuvrablesUniquement](#joursouvrablesuniquement) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-joursouvrablesuniquement.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/joursOuvrablesUniquement") |
| [nombreConvois](#nombreconvois)                       | `integer` | Optional | cannot be null | [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-nombreconvois.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/nombreConvois")                       |
| [plages](#plages)                                     | `array`   | Optional | cannot be null | [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-plages.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/plages")                                     |

### actif



`actif`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-actif.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/actif")

#### actif Type

`boolean`

### joursOuvrablesUniquement



`joursOuvrablesUniquement`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-joursouvrablesuniquement.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/joursOuvrablesUniquement")

#### joursOuvrablesUniquement Type

`boolean`

### nombreConvois



`nombreConvois`

*   is optional

*   Type: `integer`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-nombreconvois.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/nombreConvois")

#### nombreConvois Type

`integer`

### plages



`plages`

*   is optional

*   Type: `array`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité-properties-plages.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/plages")

#### plages Type

`array`

## Definitions group ConfirmationTransmission

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/ConfirmationTransmission"}
```

| Property                                                    | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                  |
| :---------------------------------------------------------- | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteSupplementaire](#textesupplementaire)                 | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/texteSupplementaire")                                                                 |
| [nomChampCourrielUtilisateur](#nomchampcourrielutilisateur) | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur") |
| [modaleCourrielConfirmation](#modalecourrielconfirmation)   | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")                           |

### texteSupplementaire

Multilingue

`texteSupplementaire`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/texteSupplementaire")

#### texteSupplementaire Type

`object` ([Translation](frw-definitions-translation.md))

#### texteSupplementaire Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### nomChampCourrielUtilisateur

Nom du champ courriel qui contient l'adresse courriel à utiliser pour le courriel de confirmation de transmission.

`nomChampCourrielUtilisateur`

*   is optional

*   Type: `string`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur")

#### nomChampCourrielUtilisateur Type

`string`

### modaleCourrielConfirmation



`modaleCourrielConfirmation`

*   is optional

*   Type: `object` ([Fenêtre modale de courriel de confirmation](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")

#### modaleCourrielConfirmation Type

`object` ([Fenêtre modale de courriel de confirmation](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md))

## Definitions group CourrielReprise

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/CourrielReprise"}
```

| Property                                  | Type     | Required | Nullable       | Defined by                                                                                                                                                                          |
| :---------------------------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [courrielExpediteur](#courrielexpediteur) | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/courrielExpediteur") |
| [nomExpediteur](#nomexpediteur)           | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/nomExpediteur")    |
| [objet](#objet)                           | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/objet")                                                |
| [corps](#corps)                           | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/corps")                                                |

### courrielExpediteur

Adresse courriel expéditeur.

`courrielExpediteur`

*   is optional

*   Type: `string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/courrielExpediteur")

#### courrielExpediteur Type

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur.md))

#### courrielExpediteur Examples

```json
"NEPASREPONDRE@mtess.gouv.qc.ca"
```

### nomExpediteur

Nom de l'expéditeur expéditeur.

`nomExpediteur`

*   is optional

*   Type: `string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/nomExpediteur")

#### nomExpediteur Type

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md))

#### nomExpediteur Examples

```json
"Formulaires en ligne - MESS"
```

### objet

Multilingue

`objet`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/objet")

#### objet Type

`object` ([Translation](frw-definitions-translation.md))

#### objet Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

#### objet Examples

```json
"Formulaire  « {0} » incomplet"
```

### corps

Multilingue

`corps`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/corps")

#### corps Type

`object` ([Translation](frw-definitions-translation.md))

#### corps Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## Definitions group DebuterFormulaire

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/DebuterFormulaire"}
```

| Property                    | Type     | Required | Nullable       | Defined by                                                                                                                                                                |
| :-------------------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [authentifie](#authentifie) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-debuterformulaire-properties-authentifie.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie") |
| [anonyme](#anonyme)         | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-debuterformulaire-properties-anonyme.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme")         |

### authentifie

Paramètres de la page permettant de débuter un formulaire authentifié.

`authentifie`

*   is optional

*   Type: `object` ([authentifie](frw-definitions-debuterformulaire-properties-authentifie.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-debuterformulaire-properties-authentifie.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie")

#### authentifie Type

`object` ([authentifie](frw-definitions-debuterformulaire-properties-authentifie.md))

### anonyme

Paramètres de la page permettant de débuter un formulaire anonyme.

`anonyme`

*   is optional

*   Type: `object` ([anonyme](frw-definitions-debuterformulaire-properties-anonyme.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-debuterformulaire-properties-anonyme.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme")

#### anonyme Type

`object` ([anonyme](frw-definitions-debuterformulaire-properties-anonyme.md))

## Definitions group Messages

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Messages"}
```

| Property                            | Type     | Required | Nullable       | Defined by                                                                                                                                                      |
| :---------------------------------- | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [erreurTechnique](#erreurtechnique) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-messages-properties-erreurtechnique.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique") |

### erreurTechnique

Paramètres du message d'erreur technique.

`erreurTechnique`

*   is optional

*   Type: `object` ([erreurTechnique](frw-definitions-messages-properties-erreurtechnique.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-messages-properties-erreurtechnique.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique")

#### erreurTechnique Type

`object` ([erreurTechnique](frw-definitions-messages-properties-erreurtechnique.md))

## Definitions group Pages

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Pages"}
```

| Property                            | Type     | Required | Nullable       | Defined by                                                                                                                                                |
| :---------------------------------- | :------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sessionInvalide](#sessioninvalide) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-pages-properties-sessioninvalide.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide") |

### sessionInvalide

Paramètres associés à la page de session invalide.

`sessionInvalide`

*   is optional

*   Type: `object` ([sessionInvalide](frw-definitions-pages-properties-sessioninvalide.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-pages-properties-sessioninvalide.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide")

#### sessionInvalide Type

`object` ([sessionInvalide](frw-definitions-pages-properties-sessioninvalide.md))

## Definitions group Revision

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Revision"}
```

| Property                                        | Type      | Required | Nullable       | Defined by                                                                                                                                                                          |
| :---------------------------------------------- | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [validationAutomatique](#validationautomatique) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-page-de-révision-properties-validationautomatique.md "https://example.com/schemas/custom#/definitions/Revision/properties/validationAutomatique") |

### validationAutomatique

Indique si la fenêtre modale permettant la saisie d'une adresse courriel pour le courriel de confirmation est affichée ou non.

`validationAutomatique`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-page-de-révision-properties-validationautomatique.md "https://example.com/schemas/custom#/definitions/Revision/properties/validationAutomatique")

#### validationAutomatique Type

`boolean`

## Definitions group Soumission

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Soumission"}
```

| Property                                      | Type     | Required | Nullable       | Defined by                                                                                                                                     |
| :-------------------------------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteBoutonSoumettre](#texteboutonsoumettre) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Soumission/properties/texteBoutonSoumettre") |

### texteBoutonSoumettre

Multilingue

`texteBoutonSoumettre`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Soumission/properties/texteBoutonSoumettre")

#### texteBoutonSoumettre Type

`object` ([Translation](frw-definitions-translation.md))

#### texteBoutonSoumettre Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## Definitions group ModaleCourrielConfirmation

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/ModaleCourrielConfirmation"}
```

| Property          | Type      | Required | Nullable       | Defined by                                                                                                                                                                                      |
| :---------------- | :-------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif-2) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-fenêtre-modale-de-courriel-de-confirmation-properties-actif.md "https://example.com/schemas/custom#/definitions/ModaleCourrielConfirmation/properties/actif") |

### actif

Indique si la fenêtre modale permettant la saisie d'une adresse courriel pour le courriel de confirmation est affichée ou non.

`actif`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-fenêtre-modale-de-courriel-de-confirmation-properties-actif.md "https://example.com/schemas/custom#/definitions/ModaleCourrielConfirmation/properties/actif")

#### actif Type

`boolean`

## Definitions group ValidationMessages

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/ValidationMessages"}
```

| Property         | Type     | Required | Nullable       | Defined by                                                                                                                                               |
| :--------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$") |

### Pattern: `^[a-zA-Z0-9]+$`

Multilingue

`^[a-zA-Z0-9]+$`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$")

#### ^\[a-zA-Z0-9]+$ Type

`object` ([Translation](frw-definitions-translation.md))

#### ^\[a-zA-Z0-9]+$ Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

## Definitions group InjecterJs

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/InjecterJs"}
```

| Property              | Type     | Required | Nullable       | Defined by                                                                                                                         |
| :-------------------- | :------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| [method](#method)     | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/method")   |
| [computed](#computed) | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/computed") |
| [watch](#watch)       | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/watch")    |

### method

Méthodes de type 'method' à injecter au code au modèle vue.js du formulaire.

`method`

*   is optional

*   Type: `object` ([method](frw-definitions-nomfonction.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/method")

#### method Type

`object` ([method](frw-definitions-nomfonction.md))

### computed

Méthodes de type 'computed' à injecter au code au modèle vue.js du formulaire.

`computed`

*   is optional

*   Type: `object` ([computed](frw-definitions-nomfonction.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/computed")

#### computed Type

`object` ([computed](frw-definitions-nomfonction.md))

### watch

Méthodes de type 'watch' à injecter au code au modèle vue.js du formulaire.

`watch`

*   is optional

*   Type: `object` ([watch](frw-definitions-nomfonction.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/watch")

#### watch Type

`object` ([watch](frw-definitions-nomfonction.md))

## Definitions group NomFonction

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/NomFonction"}
```

| Property         | Type     | Required | Nullable       | Defined by                                                                                                                                                                                                                 |
| :--------------- | :------- | :------- | :------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md "https://example.com/schemas/custom#/definitions/NomFonction/patternProperties/^\[a-zA-Z0-9]+$") |

### Pattern: `^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   is optional

*   Type: `object` ([Nom de la fonction Vue.js à injecter dans le formulaire](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md "https://example.com/schemas/custom#/definitions/NomFonction/patternProperties/^\[a-zA-Z0-9]+$")

#### ^\[a-zA-Z0-9]+$ Type

`object` ([Nom de la fonction Vue.js à injecter dans le formulaire](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md))

## Definitions group Code

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Code"}
```

| Property | Type | Required | Nullable | Defined by |
| :------- | :--- | :------- | :------- | :--------- |

## Definitions group Scripts

Reference this group by using

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Scripts"}
```

| Property                                | Type     | Required | Nullable       | Defined by                                                                                                                                                        |
| :-------------------------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [outilStatistiques](#outilstatistiques) | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-scripts-properties-outilstatistiques.md "https://example.com/schemas/custom#/definitions/Scripts/properties/outilStatistiques") |

### outilStatistiques

Javascript servant à une solution d'outil statistiques (ex. Google Analytics ou Matomo). Injecté dans toutes les pages à la fin du body.

`outilStatistiques`

*   is optional

*   Type: `string` ([outilStatistiques](frw-definitions-scripts-properties-outilstatistiques.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-scripts-properties-outilstatistiques.md "https://example.com/schemas/custom#/definitions/Scripts/properties/outilStatistiques")

#### outilStatistiques Type

`string` ([outilStatistiques](frw-definitions-scripts-properties-outilstatistiques.md))

#### outilStatistiques Examples

```json
"<script> // Votre js ici... </script>"
```
