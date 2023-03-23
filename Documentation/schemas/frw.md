## Type de Schéma sans nom

inconnu

# Définitions de Schéma sans nom

## Groupe de définitions EcsForm

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/EcsForm"}
```

| Propriété                                                                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                      |
| :------------------------------------------------------------------------------------ | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherMessageSauvegardeCourrielReprise](#affichermessagesauvegardecourrielreprise) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-ecsform-properties-affichermessagesauvegardecourrielreprise.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/afficherMessageSauvegardeCourrielReprise") |
| [form](#form)                                                                         | `object`  | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-form.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/form")                                                                                            |
| [config](#config)                                                                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/config")                                                                   |
| [textes](#textes)                                                                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-ecsform-properties-textes.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/textes")                                                                     |

### afficherMessageSauvegardeCourrielReprise

DEPRECATED (Utiliser maintenant enregistrement.afficherMessageIncitatif)

`afficherMessageSauvegardeCourrielReprise`

*   est optionnel

*   ne peut être nul

#### Type de afficherMessageSauvegardeCourrielReprise

`boolean`

### form

Élément racine d'un formulaire.

`form`

*   est requis

*   ne peut être nul

#### Type de form

`object` ([Form](frw-definitions-form.md))

### config



`config`

*   est optionnel

*   ne peut être nul

#### Type de config

`object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

### textes



`textes`

*   est optionnel

*   ne peut être nul

#### Type de textes

`object` ([Détails](frw-definitions-ecsform-properties-textes.md))

## Groupe de définitions Form

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Form"}
```

| Propriété                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                      |
| :------------------------------------------ | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sectionsGroup](#sectionsgroup)             | `array`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-sectionsgroup.md "https://example.com/schemas/custom#/definitions/Form/properties/sectionsGroup")             |
| [templates](#templates)                     | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-templates.md "https://example.com/schemas/custom#/definitions/Form/properties/templates")                     |
| [title](#title)                             | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Form/properties/title")                                       |
| [inputDefaultClasses](#inputdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-inputdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/inputDefaultClasses") |
| [defaults](#defaults)                       | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-defaults-values.md "https://example.com/schemas/custom#/definitions/Form/properties/defaults")                                |
| [outerDefaultClasses](#outerdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-form-properties-outerdefaultclasses.md "https://example.com/schemas/custom#/definitions/Form/properties/outerDefaultClasses") |

### sectionsGroup



`sectionsGroup`

*   est optionnel

*   ne peut être nul

#### Type de sectionsGroup

`object[]` ([Section Group](frw-definitions-section-group.md))

### templates



`templates`

*   est optionnel

*   ne peut être nul

#### Type de templates

`object` ([Détails](frw-definitions-form-properties-templates.md))

### title

Multilingue

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### inputDefaultClasses



`inputDefaultClasses`

*   est optionnel

*   ne peut être nul

#### Type de inputDefaultClasses

`object` ([Détails](frw-definitions-form-properties-inputdefaultclasses.md))

### defaults



`defaults`

*   est optionnel

*   ne peut être nul

#### Type de defaults

`object` ([Defaults values](frw-definitions-defaults-values.md))

### outerDefaultClasses



`outerDefaultClasses`

*   est optionnel

*   ne peut être nul

#### Type de outerDefaultClasses

`object` ([Détails](frw-definitions-form-properties-outerdefaultclasses.md))

## Groupe de définitions Section

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Section"}
```

| Propriété                                                                           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                    |
| :---------------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [section](#section)                                                                 | `object`  | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Section/properties/section")                                                                                |
| [id](#id)                                                                           | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-id.md "https://example.com/schemas/custom#/definitions/Section/properties/id")                                                                           |
| [cacherTexteExplicatifChampsObligatoires](#cachertexteexplicatifchampsobligatoires) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "https://example.com/schemas/custom#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires") |
| [classes](#classes)                                                                 | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-classes.md "https://example.com/schemas/custom#/definitions/Section/properties/classes")                                                                 |
| [v-if](#v-if)                                                                       | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-v-if.md "https://example.com/schemas/custom#/definitions/Section/properties/v-if")                                                                       |
| [components](#components)                                                           | `array`   | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-properties-components.md "https://example.com/schemas/custom#/definitions/Section/properties/components")                                                           |

### section

Multilingue

`section`

*   est requis

*   ne peut être nul

#### Type de section

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de section

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### id



`id`

*   est optionnel

*   ne peut être nul

#### Type de id

`string`

### cacherTexteExplicatifChampsObligatoires

Permet d'afficher l'indication de champs obligatoires.

`cacherTexteExplicatifChampsObligatoires`

*   est optionnel

*   ne peut être nul

#### Type de cacherTexteExplicatifChampsObligatoires

`boolean`

### classes



`classes`

*   est optionnel

*   ne peut être nul

#### Type de classes

`string`

### v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

#### Type de v-if

`string`

### components



`components`

*   est optionnel

*   ne peut être nul

#### Type de components

an array of merged types ([Détails](frw-definitions-section-properties-components-items.md))

## Groupe de définitions SectionsGroup

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/SectionsGroup"}
```

| Propriété                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :---------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sections](#sections)         | `array`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-sections.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sections") |
| [prefixId](#prefixid)         | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-prefixid.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/prefixId") |
| [classes](#classes-1)         | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-classes.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/classes")   |
| [v-if](#v-if-1)               | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-section-group-properties-v-if.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/v-if")         |
| [sectionGroup](#sectiongroup) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/SectionsGroup/properties/sectionGroup")                   |

### sections



`sections`

*   est optionnel

*   ne peut être nul

#### Type de sections

`object[]` ([Section](frw-definitions-section.md))

### prefixId



`prefixId`

*   est optionnel

*   ne peut être nul

#### Type de prefixId

`string`

### classes



`classes`

*   est optionnel

*   ne peut être nul

#### Type de classes

`string`

### v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

#### Type de v-if

`string`

### sectionGroup

Multilingue

`sectionGroup`

*   est optionnel

*   ne peut être nul

#### Type de sectionGroup

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de sectionGroup

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions Display

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Display"}
```

| Propriété                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                      |
| :------------------------------------ | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [type](#type)                         | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-type.md "https://example.com/schemas/custom#/definitions/Display/properties/type")                         |
| [classes](#classes-2)                 | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-classes.md "https://example.com/schemas/custom#/definitions/Display/properties/classes")                   |
| [afficherBlocCode](#afficherbloccode) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Display/properties/afficherBlocCode") |
| [tag](#tag)                           | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-tag.md "https://example.com/schemas/custom#/definitions/Display/properties/tag")                           |
| [src](#src)                           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/src")                                      |
| [base64](#base64)                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/base64")                                   |
| [text](#text)                         | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/text")                                     |
| [title](#title-1)                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/title")                                    |
| [additionals](#additionals)           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-additionals.md "https://example.com/schemas/custom#/definitions/Display/properties/additionals")           |
| [alt](#alt)                           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Display/properties/alt")                                      |
| [v-if](#v-if-2)                       | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-v-if.md "https://example.com/schemas/custom#/definitions/Display/properties/v-if")                         |
| [components](#components-1)           | `array`   | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-display-properties-components.md "https://example.com/schemas/custom#/definitions/Display/properties/components")             |

### type

Types from custom templates list.

`type`

*   est optionnel

*   ne peut être nul

#### Type de type

`string`

#### Exemple de type

```yaml
inline

```

```yaml
dynamic

```

```yaml
bandeau

```

```yaml
bandeau-notification

```

```yaml
image

```

```yaml
avis

```

```yaml
accordeon

```

### classes



`classes`

*   est optionnel

*   ne peut être nul

#### Type de classes

`string`

### afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   est optionnel

*   ne peut être nul

#### Type de afficherBlocCode

`boolean` ([afficherBlocCode](frw-definitions-display-properties-afficherbloccode.md))

### tag



`tag`

*   est optionnel

*   ne peut être nul

#### Type de tag

`string`

### src

Multilingue

`src`

*   est optionnel

*   ne peut être nul

#### Type de src

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de src

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### base64

Multilingue

`base64`

*   est optionnel

*   ne peut être nul

#### Type de base64

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de base64

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### text

Multilingue

`text`

*   est optionnel

*   ne peut être nul

#### Type de text

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de text

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### title

Multilingue

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### additionals



`additionals`

*   est optionnel

*   ne peut être nul

#### Type de additionals

`object` ([Détails](frw-definitions-display-properties-additionals.md))

### alt

Multilingue

`alt`

*   est optionnel

*   ne peut être nul

#### Type de alt

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de alt

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

#### Type de v-if

`string`

### components



`components`

*   est optionnel

*   ne peut être nul

#### Type de components

an array of merged types ([Détails](frw-definitions-display-properties-components-items.md))

## Groupe de définitions Input

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Input"}
```

| Propriété                                   | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                             |
| :------------------------------------------ | :-------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [name](#name)                               | `string`  | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-name.md "https://example.com/schemas/custom#/definitions/Input/properties/name")                                                                    |
| [type](#type-1)                             | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-type.md "https://example.com/schemas/custom#/definitions/Input/properties/type")                                                                    |
| [value](#value)                             | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-value.md "https://example.com/schemas/custom#/definitions/Input/properties/value")                                                                  |
| [limit](#limit)                             | `number`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-limit.md "https://example.com/schemas/custom#/definitions/Input/properties/limit")                                                                  |
| [validation-name](#validation-name)         | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-name")                                                                   |
| [validation-messages](#validation-messages) | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md "https://example.com/schemas/custom#/definitions/Input/properties/validation-messages") |
| [label](#label)                             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/label")                                                                             |
| [placeholder](#placeholder)                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/placeholder")                                                                       |
| [inputClasses](#inputclasses)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-inputclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/inputClasses")                                                    |
| [inputmode](#inputmode)                     | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-inputmode.md "https://example.com/schemas/custom#/definitions/Input/properties/inputmode")                                                          |
| [pattern](#pattern)                         | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-pattern.md "https://example.com/schemas/custom#/definitions/Input/properties/pattern")                                                              |
| [outerClasses](#outerclasses)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-outerclasses.md "https://example.com/schemas/custom#/definitions/Input/properties/outerClasses")                                                    |
| [help](#help)                               | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/help")                                                                              |
| [pdfBind](#pdfbind)                         | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-pdfbind.md "https://example.com/schemas/custom#/definitions/Input/properties/pdfBind")                                                              |
| [additionals](#additionals-1)               | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-additionals.md "https://example.com/schemas/custom#/definitions/Input/properties/additionals")                                                      |
| [v-if](#v-if-3)                             | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-v-if.md "https://example.com/schemas/custom#/definitions/Input/properties/v-if")                                                                    |
| [v-else-value](#v-else-value)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-v-else-value.md "https://example.com/schemas/custom#/definitions/Input/properties/v-else-value")                                                    |
| [helpPosition](#helpposition)               | `string`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-helpposition.md "https://example.com/schemas/custom#/definitions/Input/properties/helpPosition")                                                    |
| [min](#min)                                 | Plusieurs | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-min.md "https://example.com/schemas/custom#/definitions/Input/properties/min")                                                                      |
| [max](#max)                                 | Plusieurs | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-max.md "https://example.com/schemas/custom#/definitions/Input/properties/max")                                                                      |
| [addLabel](#addlabel)                       | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/addLabel")                                                                          |
| [removeLabel](#removelabel)                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/removeLabel")                                                                       |
| [instanceLabel](#instancelabel)             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/instanceLabel")                                                                     |
| [tooltip](#tooltip)                         | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation-1.md "https://example.com/schemas/custom#/definitions/Input/properties/tooltip")                                                                         |
| [options](#options)                         | Plusieurs | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-options.md "https://example.com/schemas/custom#/definitions/Input/properties/options")                                                              |
| [nomDocument](#nomdocument)                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Input/properties/nomDocument")                                                                       |
| [afficherBlocCode](#afficherbloccode-1)     | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Input/properties/afficherBlocCode")                                            |
| [validations](#validations)                 | `object`  | Optionnel   | peut être nul    | [Schéma sans nom](frw-definitions-input-properties-validation.md "https://example.com/schemas/custom#/definitions/Input/properties/validations")                                                       |
| [repeatable](#repeatable)                   | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-repeatable.md "https://example.com/schemas/custom#/definitions/Input/properties/repeatable")                                                        |
| [minimum](#minimum)                         | `number`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-minimum.md "https://example.com/schemas/custom#/definitions/Input/properties/minimum")                                                              |
| [components](#components-2)                 | `array`   | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-components.md "https://example.com/schemas/custom#/definitions/Input/properties/components")                                                        |
| [disabled](#disabled)                       | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-input-properties-disabled.md "https://example.com/schemas/custom#/definitions/Input/properties/disabled")                                                            |

### name

Adds a name attribute, and when used with <FormulateForm> this is the key of the field. If no name is defined a random hash will be assigned

`name`

*   est requis

*   ne peut être nul

#### Type de name

`string`

### type

Required. The type of input element. See the input library for a full range of options.

`type`

*   est optionnel

*   ne peut être nul

#### Type de type

`string`

#### Contraintes de type

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                   | Explication |
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

#### Valeur par défaut de type

La valeur par défaut est:

```yaml
text

```

### value



`value`

*   est optionnel

*   ne peut être nul

#### Type de value

`string`

### limit



`limit`

*   est optionnel

*   ne peut être nul

#### Type de limit

`number`

### validation-name

Multilingue

`validation-name`

*   est optionnel

*   ne peut être nul

#### Type de validation-name

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de validation-name

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### validation-messages



`validation-messages`

*   est optionnel

*   ne peut être nul

#### Type de validation-messages

`object` ([validation-messages (Messages de validation personnalisés)](frw-definitions-input-properties-validation-messages-messages-de-validation-personnalisés.md))

### label

Multilingue

`label`

*   est optionnel

*   ne peut être nul

#### Type de label

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de label

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### placeholder

Multilingue

`placeholder`

*   est optionnel

*   ne peut être nul

#### Type de placeholder

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de placeholder

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### inputClasses



`inputClasses`

*   est optionnel

*   ne peut être nul

#### Type de inputClasses

`string`

### inputmode

Text field inputmode (html)

`inputmode`

*   est optionnel

*   ne peut être nul

#### Type de inputmode

`string`

#### Contraintes de inputmode

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur     | Explication |
| :--------- | :---------- |
| `"number"` |             |

### pattern

Regex pattern (html)

`pattern`

*   est optionnel

*   ne peut être nul

#### Type de pattern

`string`

### outerClasses



`outerClasses`

*   est optionnel

*   ne peut être nul

#### Type de outerClasses

`string`

### help

Multilingue

`help`

*   est optionnel

*   ne peut être nul

#### Type de help

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de help

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### pdfBind



`pdfBind`

*   est optionnel

*   ne peut être nul

#### Type de pdfBind

`string`

### additionals



`additionals`

*   est optionnel

*   ne peut être nul

#### Type de additionals

`object` ([Détails](frw-definitions-input-properties-additionals.md))

### v-if

Conditionnal display on another property/form field.

`v-if`

*   est optionnel

*   ne peut être nul

#### Type de v-if

`string`

### v-else-value

Valeur de remplacement lorsque le v-if n'affiche pas le champ. Supporté CÔTÉ SERVEUR UNIQUEMENT.

`v-else-value`

*   est optionnel

*   ne peut être nul

#### Type de v-else-value

`string`

### helpPosition



`helpPosition`

*   est optionnel

*   ne peut être nul

#### Type de helpPosition

`string`

#### Contraintes de helpPosition

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur     | Explication |
| :--------- | :---------- |
| `"before"` |             |
| `"after"`  |             |

### min



`min`

*   est optionnel

*   ne peut être nul

#### Type de min

l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-min.md))

### max



`max`

*   est optionnel

*   ne peut être nul

#### Type de max

l'un des éléments suivants :`string` ou `number` ([Détails](frw-definitions-input-properties-max.md))

### addLabel

Multilingue

`addLabel`

*   est optionnel

*   ne peut être nul

#### Type de addLabel

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de addLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### removeLabel

Multilingue

`removeLabel`

*   est optionnel

*   ne peut être nul

#### Type de removeLabel

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de removeLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### instanceLabel

Multilingue

`instanceLabel`

*   est optionnel

*   ne peut être nul

#### Type de instanceLabel

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de instanceLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### tooltip



`tooltip`

*   est optionnel

*   ne peut être nul

#### Type de tooltip

`object` ([Translation](frw-definitions-translation-1.md))

#### Valeur par défaut de tooltip

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### options

Array or object of options (select or box classifications)

`options`

*   est optionnel

*   peut être nul

#### Type de options

l'un des éléments suivants :`object` ou `string` ou `array` ([Détails](frw-definitions-input-properties-options.md))

#### Exemple de options

```yaml
yesno

```

### nomDocument

Multilingue

`nomDocument`

*   est optionnel

*   ne peut être nul

#### Type de nomDocument

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de nomDocument

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### afficherBlocCode

Indique si le bloc de code utilisé pour générer le contrôle est affiché sous ce dernier. Utile pour P700 notamment.

`afficherBlocCode`

*   est optionnel

*   ne peut être nul

#### Type de afficherBlocCode

`boolean` ([afficherBlocCode](frw-definitions-input-properties-afficherbloccode.md))

### validations



`validations`

*   est optionnel

*   peut être nul

#### Type de validations

`object` ([Validation](frw-definitions-input-properties-validation.md))

#### Valeur par défaut de validations

La valeur par défaut est:

```yaml
{}

```

### repeatable



`repeatable`

*   est optionnel

*   ne peut être nul

#### Type de repeatable

`boolean`

### minimum



`minimum`

*   est optionnel

*   ne peut être nul

#### Type de minimum

`number`

### components



`components`

*   est optionnel

*   ne peut être nul

#### Type de components

an array of merged types ([Détails](frw-definitions-input-properties-components-items.md))

### disabled



`disabled`

*   est optionnel

*   ne peut être nul

#### Type de disabled

`boolean`

## Groupe de définitions Translation

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Translation"}
```

| Propriété                 | Type     | Obligatoire | Nullable      | Défini par                                                                                                                                  |
| :------------------------ | :------- | :---------- | :------------ | :------------------------------------------------------------------------------------------------------------------------------------------ |
| [fr](#fr)                 | `string` | Obligatoire | peut être nul | [Schéma sans nom](frw-definitions-translation-properties-fr.md "https://example.com/schemas/custom#/definitions/Translation/properties/fr") |
| [en](#en)                 | `string` | Optionnel   | peut être nul | [Schéma sans nom](frw-definitions-translation-properties-en.md "https://example.com/schemas/custom#/definitions/Translation/properties/en") |
| Propriétés Additionnelles | Any      | Optionnel   | can be null   |                                                                                                                                             |

### fr

Texte de langue française.

`fr`

*   est requis

*   peut être nul

#### Type de fr

`string` ([fr](frw-definitions-translation-properties-fr.md))

### en

Texte de langue anglaise.

`en`

*   est optionnel

*   peut être nul

#### Type de en

`string` ([en](frw-definitions-translation-properties-en.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Tooltip

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Tooltip"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                   |
| :------------------------ | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| [title](#title-2)         | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/title") |
| [text](#text-1)           | `object` | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Tooltip/properties/text")  |
| Propriétés Additionnelles | Any      | Optionnel   | can be null      |                                                                                                                              |

### title

Multilingue

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### text

Multilingue

`text`

*   est requis

*   ne peut être nul

#### Type de text

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de text

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Defaults

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Defaults"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Config

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Config"}
```

| Propriété                                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                               |
| :---------------------------------------------------- | :-------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherBlocCode](#afficherbloccode-2)               | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherBlocCode")       |
| [afficherPartagePage](#afficherpartagepage)           | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherPartagePage") |
| [confirmationTransmission](#confirmationtransmission) | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-confirmation-de-transmission.md "https://example.com/schemas/custom#/definitions/Config/properties/confirmationTransmission")                          |
| [courrielReprise](#courrielreprise)                   | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-courrielreprise.md "https://example.com/schemas/custom#/definitions/Config/properties/courrielReprise")                                                |
| [debuterFormulaire](#debuterformulaire)               | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-debuterformulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/debuterFormulaire")                                            |
| [enregistrement](#enregistrement)                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-enregistrement.md "https://example.com/schemas/custom#/definitions/Config/properties/enregistrement")                                                  |
| [formulaireUnilingue](#formulaireunilingue)           | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-formulaireunilingue.md "https://example.com/schemas/custom#/definitions/Config/properties/formulaireUnilingue") |
| [gererPlageDisponibilite](#gererplagedisponibilite)   | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-gerer-les-plages-de-disponibilité.md "https://example.com/schemas/custom#/definitions/Config/properties/gererPlageDisponibilite")                      |
| [injecterJs](#injecterjs)                             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/injecterJs")                              |
| [messages](#messages)                                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-messages.md "https://example.com/schemas/custom#/definitions/Config/properties/messages")                                                              |
| [pages](#pages)                                       | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-pages.md "https://example.com/schemas/custom#/definitions/Config/properties/pages")                                                                    |
| [piv](#piv)                                           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-piv.md "https://example.com/schemas/custom#/definitions/Config/properties/piv")                                 |
| [revision](#revision)                                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-page-de-révision.md "https://example.com/schemas/custom#/definitions/Config/properties/revision")                                                      |
| [scripts](#scripts)                                   | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-scripts.md "https://example.com/schemas/custom#/definitions/Config/properties/scripts")                                                                |
| [securite](#securite)                                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-sécurité-du-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/securite")                                                |
| [soumission](#soumission)                             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-page-de-soumission.md "https://example.com/schemas/custom#/definitions/Config/properties/soumission")                                                  |
| [title](#title-3)                                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Config/properties/title")                                                              |

### afficherBlocCode

(Réservé) Afficher un bloc de code des éléments du formulaire.

`afficherBlocCode`

*   est optionnel

*   ne peut être nul

#### Type de afficherBlocCode

`boolean` ([afficherBlocCode](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

### afficherPartagePage

(Avancé) ajouter un bouton partage dans toutes les pages à la droite du titre de la page.

`afficherPartagePage`

*   est optionnel

*   ne peut être nul

#### Type de afficherPartagePage

`boolean` ([afficherPartagePage](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

### confirmationTransmission



`confirmationTransmission`

*   est optionnel

*   ne peut être nul

#### Type de confirmationTransmission

`object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

### courrielReprise

Paramètres associés au courriel de reprise.

`courrielReprise`

*   est optionnel

*   ne peut être nul

#### Type de courrielReprise

`object` ([courrielReprise](frw-definitions-courrielreprise.md))

### debuterFormulaire

Paramètres de la page permettant de débuter un formulaire.

`debuterFormulaire`

*   est optionnel

*   ne peut être nul

#### Type de debuterFormulaire

`object` ([debuterFormulaire](frw-definitions-debuterformulaire.md))

### enregistrement

Paramètres associés à l'enregistrement d'un formulaire

`enregistrement`

*   est optionnel

*   ne peut être nul

#### Type de enregistrement

`object` ([enregistrement](frw-definitions-enregistrement.md))

### formulaireUnilingue

Permet de retirer le selecteur de langue. Le formulaire s'affichera en français seulement.

`formulaireUnilingue`

*   est optionnel

*   ne peut être nul

#### Type de formulaireUnilingue

`boolean`

### gererPlageDisponibilite



`gererPlageDisponibilite`

*   est optionnel

*   ne peut être nul

#### Type de gererPlageDisponibilite

`object` ([Gerer les plages de disponibilité](frw-definitions-gerer-les-plages-de-disponibilité.md))

### injecterJs



`injecterJs`

*   est optionnel

*   ne peut être nul

#### Type de injecterJs

`object` ([Scripts Vue.js à injecter au formulaire.](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

### messages

Paramètres associés aux différents messages.

`messages`

*   est optionnel

*   ne peut être nul

#### Type de messages

`object` ([messages](frw-definitions-messages.md))

### pages

Paramètres associés à différentes pages.

`pages`

*   est optionnel

*   ne peut être nul

#### Type de pages

`object` ([pages](frw-definitions-pages.md))

### piv

Paramètres associés au PIV.

`piv`

*   est optionnel

*   ne peut être nul

#### Type de piv

`object` ([piv](frw-definitions-configuration-du-formulaire-properties-piv.md))

### revision



`revision`

*   est optionnel

*   ne peut être nul

#### Type de revision

`object` ([Page de révision](frw-definitions-page-de-révision.md))

### scripts

(Avancé) Paramètres d'injection de javascript.

`scripts`

*   est optionnel

*   ne peut être nul

#### Type de scripts

`object` ([scripts](frw-definitions-scripts.md))

### securite



`securite`

*   est optionnel

*   ne peut être nul

#### Type de securite

`object` ([Sécurité du formulaire](frw-definitions-sécurité-du-formulaire.md))

### soumission



`soumission`

*   est optionnel

*   ne peut être nul

#### Type de soumission

`object` ([Page de soumission](frw-definitions-page-de-soumission.md))

### title

Multilingue

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions Securite

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Securite"}
```

| Propriété                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                              |
| :---------------------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [accesAnonyme](#accesanonyme) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-sécurité-du-formulaire-properties-accesanonyme.md "https://example.com/schemas/custom#/definitions/Securite/properties/accesAnonyme") |

### accesAnonyme

Permet d'activer l'accès anonyme au formulaire.

`accesAnonyme`

*   est optionnel

*   ne peut être nul

#### Type de accesAnonyme

`boolean`

## Groupe de définitions Enregistrement

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Enregistrement"}
```

| Propriété                                                                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                    |
| :---------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)                                                               | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-enregistrement-properties-actif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/actif")                                       |
| [afficherMessageIncitatif](#affichermessageincitatif)                         | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-enregistrement-properties-affichermessageincitatif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/afficherMessageIncitatif") |
| [texteModaleEnregistrementAuthentifie](#textemodaleenregistrementauthentifie) | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")                            |

### actif

Indique si l'enregistrement du formulaire est actif (bouton enregistré présent et enregistrement au changement de page).

`actif`

*   est optionnel

*   ne peut être nul

#### Type de actif

`boolean` ([actif](frw-definitions-enregistrement-properties-actif.md))

### afficherMessageIncitatif

Indique si le message (avis avertissement en haut de chaque page) incitant l'enregistrement est affiché ou non.

`afficherMessageIncitatif`

*   est optionnel

*   ne peut être nul

#### Type de afficherMessageIncitatif

`boolean` ([afficherMessageIncitatif](frw-definitions-enregistrement-properties-affichermessageincitatif.md))

### texteModaleEnregistrementAuthentifie

Multilingue

`texteModaleEnregistrementAuthentifie`

*   est optionnel

*   ne peut être nul

#### Type de texteModaleEnregistrementAuthentifie

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de texteModaleEnregistrementAuthentifie

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions GererPlageDisponibilite

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/GererPlageDisponibilite"}
```

| Propriété                                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                                |
| :---------------------------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [actif](#actif-1)                                     | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-gerer-les-plages-de-disponibilité-properties-actif.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/actif")                                       |
| [joursOuvrablesUniquement](#joursouvrablesuniquement) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-gerer-les-plages-de-disponibilité-properties-joursouvrablesuniquement.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/joursOuvrablesUniquement") |
| [nombreConvois](#nombreconvois)                       | `integer` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-gerer-les-plages-de-disponibilité-properties-nombreconvois.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/nombreConvois")                       |
| [plages](#plages)                                     | `array`   | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-gerer-les-plages-de-disponibilité-properties-plages.md "https://example.com/schemas/custom#/definitions/GererPlageDisponibilite/properties/plages")                                     |

### actif



`actif`

*   est optionnel

*   ne peut être nul

#### Type de actif

`boolean`

### joursOuvrablesUniquement



`joursOuvrablesUniquement`

*   est optionnel

*   ne peut être nul

#### Type de joursOuvrablesUniquement

`boolean`

### nombreConvois



`nombreConvois`

*   est optionnel

*   ne peut être nul

#### Type de nombreConvois

`integer`

### plages



`plages`

*   est optionnel

*   ne peut être nul

#### Type de plages

`array`

## Groupe de définitions ConfirmationTransmission

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/ConfirmationTransmission"}
```

| Propriété                                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                                  |
| :---------------------------------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteSupplementaire](#textesupplementaire)                 | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/texteSupplementaire")                                                                 |
| [nomChampCourrielUtilisateur](#nomchampcourrielutilisateur) | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur") |
| [modaleCourrielConfirmation](#modalecourrielconfirmation)   | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md "https://example.com/schemas/custom#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")                           |

### texteSupplementaire

Multilingue

`texteSupplementaire`

*   est optionnel

*   ne peut être nul

#### Type de texteSupplementaire

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de texteSupplementaire

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### nomChampCourrielUtilisateur

Nom du champ courriel qui contient l'adresse courriel à utiliser pour le courriel de confirmation de transmission.

`nomChampCourrielUtilisateur`

*   est optionnel

*   ne peut être nul

#### Type de nomChampCourrielUtilisateur

`string`

### modaleCourrielConfirmation



`modaleCourrielConfirmation`

*   est optionnel

*   ne peut être nul

#### Type de modaleCourrielConfirmation

`object` ([Fenêtre modale de courriel de confirmation](frw-definitions-fenêtre-modale-de-courriel-de-confirmation.md))

## Groupe de définitions CourrielReprise

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/CourrielReprise"}
```

| Propriété                                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                          |
| :---------------------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [courrielExpediteur](#courrielexpediteur) | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-courrielreprise-properties-courrielexpediteur.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/courrielExpediteur") |
| [nomExpediteur](#nomexpediteur)           | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/nomExpediteur")    |
| [objet](#objet)                           | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/objet")                                                |
| [corps](#corps)                           | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/corps")                                                |

### courrielExpediteur

Adresse courriel expéditeur.

`courrielExpediteur`

*   est optionnel

*   ne peut être nul

#### Type de courrielExpediteur

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur.md))

#### Exemple de courrielExpediteur

```yaml
NEPASREPONDRE@mtess.gouv.qc.ca

```

### nomExpediteur

Nom de l'expéditeur expéditeur.

`nomExpediteur`

*   est optionnel

*   ne peut être nul

#### Type de nomExpediteur

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md))

#### Exemple de nomExpediteur

```yaml
Formulaires en ligne - MESS

```

### objet

Multilingue

`objet`

*   est optionnel

*   ne peut être nul

#### Type de objet

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de objet

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

#### Exemple de objet

```yaml
Formulaire  « {0} » incomplet

```

### corps

Multilingue

`corps`

*   est optionnel

*   ne peut être nul

#### Type de corps

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de corps

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions DebuterFormulaire

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/DebuterFormulaire"}
```

| Propriété                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                |
| :-------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [authentifie](#authentifie) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-debuterformulaire-properties-authentifie.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie") |
| [anonyme](#anonyme)         | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-debuterformulaire-properties-anonyme.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme")         |

### authentifie

Paramètres de la page permettant de débuter un formulaire authentifié.

`authentifie`

*   est optionnel

*   ne peut être nul

#### Type de authentifie

`object` ([authentifie](frw-definitions-debuterformulaire-properties-authentifie.md))

### anonyme

Paramètres de la page permettant de débuter un formulaire anonyme.

`anonyme`

*   est optionnel

*   ne peut être nul

#### Type de anonyme

`object` ([anonyme](frw-definitions-debuterformulaire-properties-anonyme.md))

## Groupe de définitions Messages

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Messages"}
```

| Propriété                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                      |
| :---------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [erreurTechnique](#erreurtechnique) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-messages-properties-erreurtechnique.md "https://example.com/schemas/custom#/definitions/Messages/properties/erreurTechnique") |

### erreurTechnique

Paramètres du message d'erreur technique.

`erreurTechnique`

*   est optionnel

*   ne peut être nul

#### Type de erreurTechnique

`object` ([erreurTechnique](frw-definitions-messages-properties-erreurtechnique.md))

## Groupe de définitions Pages

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Pages"}
```

| Propriété                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                |
| :---------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sessionInvalide](#sessioninvalide) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-pages-properties-sessioninvalide.md "https://example.com/schemas/custom#/definitions/Pages/properties/sessionInvalide") |

### sessionInvalide

Paramètres associés à la page de session invalide.

`sessionInvalide`

*   est optionnel

*   ne peut être nul

#### Type de sessionInvalide

`object` ([sessionInvalide](frw-definitions-pages-properties-sessioninvalide.md))

## Groupe de définitions Revision

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Revision"}
```

| Propriété                                       | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                          |
| :---------------------------------------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [validationAutomatique](#validationautomatique) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-page-de-révision-properties-validationautomatique.md "https://example.com/schemas/custom#/definitions/Revision/properties/validationAutomatique") |

### validationAutomatique

Indique si la fenêtre modale permettant la saisie d'une adresse courriel pour le courriel de confirmation est affichée ou non.

`validationAutomatique`

*   est optionnel

*   ne peut être nul

#### Type de validationAutomatique

`boolean`

## Groupe de définitions Soumission

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Soumission"}
```

| Propriété                                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                     |
| :-------------------------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| [texteBoutonSoumettre](#texteboutonsoumettre) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Soumission/properties/texteBoutonSoumettre") |

### texteBoutonSoumettre

Multilingue

`texteBoutonSoumettre`

*   est optionnel

*   ne peut être nul

#### Type de texteBoutonSoumettre

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de texteBoutonSoumettre

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions ModaleCourrielConfirmation

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/ModaleCourrielConfirmation"}
```

| Propriété         | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                      |
| :---------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif-2) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-fenêtre-modale-de-courriel-de-confirmation-properties-actif.md "https://example.com/schemas/custom#/definitions/ModaleCourrielConfirmation/properties/actif") |

### actif

Indique si la fenêtre modale permettant la saisie d'une adresse courriel pour le courriel de confirmation est affichée ou non.

`actif`

*   est optionnel

*   ne peut être nul

#### Type de actif

`boolean`

## Groupe de définitions ValidationMessages

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/ValidationMessages"}
```

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                               |
| :--------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$") |

### Modèle:`^[a-zA-Z0-9]+$`

Multilingue

`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([Translation](frw-definitions-translation.md))

#### Valeur par défaut de ^\[a-zA-Z0-9]+$

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions InjecterJs

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/InjecterJs"}
```

| Propriété             | Type     | Obligatoire | Nullable         | Défini par                                                                                                                         |
| :-------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------- |
| [method](#method)     | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/method")   |
| [computed](#computed) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/computed") |
| [watch](#watch)       | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction.md "https://example.com/schemas/custom#/definitions/InjecterJs/properties/watch")    |

### method

Méthodes de type 'method' à injecter au code au modèle vue.js du formulaire.

`method`

*   est optionnel

*   ne peut être nul

#### Type de method

`object` ([method](frw-definitions-nomfonction.md))

### computed

Méthodes de type 'computed' à injecter au code au modèle vue.js du formulaire.

`computed`

*   est optionnel

*   ne peut être nul

#### Type de computed

`object` ([computed](frw-definitions-nomfonction.md))

### watch

Méthodes de type 'watch' à injecter au code au modèle vue.js du formulaire.

`watch`

*   est optionnel

*   ne peut être nul

#### Type de watch

`object` ([watch](frw-definitions-nomfonction.md))

## Groupe de définitions NomFonction

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/NomFonction"}
```

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                                 |
| :--------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md "https://example.com/schemas/custom#/definitions/NomFonction/patternProperties/^\[a-zA-Z0-9]+$") |

### Modèle:`^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([Nom de la fonction Vue.js à injecter dans le formulaire](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md))

## Groupe de définitions Code

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Code"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions Scripts

Référencer ce groupe en utilisant

```json
{"$ref":"https://example.com/schemas/custom#/definitions/Scripts"}
```

| Propriété                               | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                        |
| :-------------------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [outilStatistiques](#outilstatistiques) | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-scripts-properties-outilstatistiques.md "https://example.com/schemas/custom#/definitions/Scripts/properties/outilStatistiques") |

### outilStatistiques

Javascript servant à une solution d'outil statistiques (ex. Google Analytics ou Matomo). Injecté dans toutes les pages à la fin du body.

`outilStatistiques`

*   est optionnel

*   ne peut être nul

#### Type de outilStatistiques

`string` ([outilStatistiques](frw-definitions-scripts-properties-outilstatistiques.md))

#### Exemple de outilStatistiques

```yaml
<script> // Votre js ici... </script>

```
