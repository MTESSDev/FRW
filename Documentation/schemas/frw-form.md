## Type de Fichier formulaire

`object` ([Fichier formulaire](frw-form.md))

# Propriétés de Fichier formulaire

| Propriété         | Type     | Obligatoire | Nullable         | Défini par                                                                                                  |
| :---------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------- |
| [form](#form)     | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form.md "schemas/form#/properties/form")                          |
| [config](#config) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-configuration-du-formulaire.md "schemas/form#/properties/config") |
| [textes](#textes) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-properties-textes.md "schemas/form#/properties/textes")                       |

## form

Élément racine d'un formulaire.

`form`

*   est optionnel

*   ne peut être nul

### Type de form

`object` ([Form](frw-form-definitions-form.md))

### Exemple de form

```yaml
form:
  title: Mon formulaire

```

## config



`config`

*   est optionnel

*   ne peut être nul

### Type de config

`object` ([Configuration du formulaire](frw-form-definitions-configuration-du-formulaire.md))

## textes



`textes`

*   est optionnel

*   ne peut être nul

### Type de textes

`object` ([Détails](frw-form-properties-textes.md))

# Définitions de Fichier formulaire

## Groupe de définitions Form

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Form"}
```

| Propriété                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                |
| :------------------------------------------ | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sectionsGroup](#sectionsgroup)             | `array`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-groupes-de-sections.md "schemas/form#/definitions/Form/properties/sectionsGroup")               |
| [templates](#templates)                     | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-réservé-frw---templates-de-composants.md "schemas/form#/definitions/Form/properties/templates") |
| [title](#title)                             | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Form/properties/title")                                                |
| [inputDefaultClasses](#inputdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-inputdefaultclasses.md "schemas/form#/definitions/Form/properties/inputDefaultClasses")         |
| [defaults](#defaults)                       | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-valeurs-par-défaut.md "schemas/form#/definitions/Form/properties/defaults")                                     |
| [outerDefaultClasses](#outerdefaultclasses) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-form-properties-outerdefaultclasses.md "schemas/form#/definitions/Form/properties/outerDefaultClasses")         |

### sectionsGroup



`sectionsGroup`

*   est optionnel

*   ne peut être nul

#### Type de sectionsGroup

`object[]` ([Section Group](frw-form-definitions-section-group.md))

### templates



`templates`

*   est optionnel

*   ne peut être nul

#### Type de templates

`object` ([RÉSERVÉ FRW - Templates de composants](frw-form-definitions-form-properties-réservé-frw---templates-de-composants.md))

#### Limites d'accès de templates

La valeur de cette propriété est gérée exclusivement par l'autorité propriétaire, et les tentatives d'une demande de modification de la valeur de cette propriété devraient être ignorées ou rejetées par cette autorité propriétaire.

### title

Textes multilingue (fr et en supportés seulement)

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Détails](frw-form-definitions-form-properties-inputdefaultclasses.md))

### defaults



`defaults`

*   est optionnel

*   ne peut être nul

#### Type de defaults

`object` ([Valeurs par défaut](frw-form-definitions-valeurs-par-défaut.md))

### outerDefaultClasses



`outerDefaultClasses`

*   est optionnel

*   ne peut être nul

#### Type de outerDefaultClasses

`object` ([Détails](frw-form-definitions-form-properties-outerdefaultclasses.md))

## Groupe de définitions Section

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Section"}
```

| Propriété                                                                           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                      |
| :---------------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [section](#section)                                                                 | `object`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Section/properties/section")                                                                                 |
| [id](#id)                                                                           | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-properties-id.md "schemas/form#/definitions/Section/properties/id")                                                                           |
| [cacherTexteExplicatifChampsObligatoires](#cachertexteexplicatifchampsobligatoires) | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-properties-cachertexteexplicatifchampsobligatoires.md "schemas/form#/definitions/Section/properties/cacherTexteExplicatifChampsObligatoires") |
| [classes](#classes)                                                                 | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-properties-classes.md "schemas/form#/definitions/Section/properties/classes")                                                                 |
| [v-if](#v-if)                                                                       | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-properties-v-if.md "schemas/form#/definitions/Section/properties/v-if")                                                                       |
| [components](#components)                                                           | `array`   | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composants.md "schemas/form#/definitions/Section/properties/components")                                                                              |

### section

Textes multilingue (fr et en supportés seulement)

`section`

*   est requis

*   ne peut être nul

#### Type de section

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object[]` ([Détails](frw-form-definitions-component.md))

## Groupe de définitions SectionsGroup

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/SectionsGroup"}
```

| Propriété                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                    |
| :---------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| [sections](#sections)         | `array`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-group-properties-sections.md "schemas/form#/definitions/SectionsGroup/properties/sections") |
| [prefixId](#prefixid)         | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-group-properties-prefixid.md "schemas/form#/definitions/SectionsGroup/properties/prefixId") |
| [classes](#classes-1)         | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-group-properties-classes.md "schemas/form#/definitions/SectionsGroup/properties/classes")   |
| [v-if](#v-if-1)               | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-section-group-properties-v-if.md "schemas/form#/definitions/SectionsGroup/properties/v-if")         |
| [sectionGroup](#sectiongroup) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/SectionsGroup/properties/sectionGroup")                    |

### sections



`sections`

*   est optionnel

*   ne peut être nul

#### Type de sections

`object[]` ([Section](frw-form-definitions-section.md))

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

Textes multilingue (fr et en supportés seulement)

`sectionGroup`

*   est optionnel

*   ne peut être nul

#### Type de sectionGroup

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de sectionGroup

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions Components

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Components"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions Component

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Component"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions ComposantAffichage

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/ComposantAffichage"}
```

| Propriété                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                               |
| :------------------------------------ | :-------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [type](#type)                         | `string`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-affichage-properties-type.md "schemas/form#/definitions/ComposantAffichage/properties/type")                         |
| [classes](#classes-2)                 | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-affichage-properties-classes.md "schemas/form#/definitions/ComposantAffichage/properties/classes")                   |
| [afficherBlocCode](#afficherbloccode) | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-affichage-properties-afficherbloccode.md "schemas/form#/definitions/ComposantAffichage/properties/afficherBlocCode") |
| [tag](#tag)                           | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-affichage-properties-tag.md "schemas/form#/definitions/ComposantAffichage/properties/tag")                           |
| [src](#src)                           | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/src")                                                   |
| [base64](#base64)                     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/base64")                                                |
| [text](#text)                         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/text")                                                  |
| [title](#title-1)                     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/title")                                                 |
| [additionals](#additionals)           | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-attributs-supplémentaires.md "schemas/form#/definitions/ComposantAffichage/properties/additionals")                            |
| [alt](#alt)                           | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantAffichage/properties/alt")                                                   |
| [v-if](#v-if-2)                       | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-affichage-properties-v-if.md "schemas/form#/definitions/ComposantAffichage/properties/v-if")                         |
| [components](#components-1)           | `array`   | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composants.md "schemas/form#/definitions/ComposantAffichage/properties/components")                                            |

### type

Types from custom templates list.

`type`

*   est requis

*   ne peut être nul

#### Type de type

`string`

#### Contraintes de type

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                   | Explication |
| :----------------------- | :---------- |
| `"inline"`               |             |
| `"dynamic"`              |             |
| `"bandeau"`              |             |
| `"bandeau-notification"` |             |
| `"image"`                |             |
| `"avis"`                 |             |
| `"accordeon"`            |             |

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

`boolean` ([afficherBlocCode](frw-form-definitions-composant-affichage-properties-afficherbloccode.md))

### tag



`tag`

*   est optionnel

*   ne peut être nul

#### Type de tag

`string`

### src

Textes multilingue (fr et en supportés seulement)

`src`

*   est optionnel

*   ne peut être nul

#### Type de src

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de src

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### base64

Textes multilingue (fr et en supportés seulement)

`base64`

*   est optionnel

*   ne peut être nul

#### Type de base64

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de base64

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### text

Textes multilingue (fr et en supportés seulement)

`text`

*   est optionnel

*   ne peut être nul

#### Type de text

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de text

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### title

Textes multilingue (fr et en supportés seulement)

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Attributs supplémentaires](frw-form-definitions-attributs-supplémentaires.md))

### alt

Textes multilingue (fr et en supportés seulement)

`alt`

*   est optionnel

*   ne peut être nul

#### Type de alt

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object[]` ([Détails](frw-form-definitions-component.md))

## Groupe de définitions ComposantInteraction

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/ComposantInteraction"}
```

| Propriété                                   | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                            |
| :------------------------------------------ | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [name](#name)                               | `string`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-name.md "schemas/form#/definitions/ComposantInteraction/properties/name")                                  |
| [type](#type-1)                             | `string`  | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-type.md "schemas/form#/definitions/ComposantInteraction/properties/type")                                  |
| [value](#value)                             | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-value.md "schemas/form#/definitions/ComposantInteraction/properties/value")                                |
| [limit](#limit)                             | `number`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-limit.md "schemas/form#/definitions/ComposantInteraction/properties/limit")                                |
| [validation-name](#validation-name)         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/validation-name")                                                  |
| [validation-messages](#validation-messages) | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-messages-de-validation.md "schemas/form#/definitions/ComposantInteraction/properties/validation-messages") |
| [label](#label)                             | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/label")                                                            |
| [placeholder](#placeholder)                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/placeholder")                                                      |
| [inputClasses](#inputclasses)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-inputclasses.md "schemas/form#/definitions/ComposantInteraction/properties/inputClasses")                  |
| [inputmode](#inputmode)                     | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-inputmode.md "schemas/form#/definitions/ComposantInteraction/properties/inputmode")                        |
| [pattern](#pattern)                         | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-pattern.md "schemas/form#/definitions/ComposantInteraction/properties/pattern")                            |
| [outerClasses](#outerclasses)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-outerclasses.md "schemas/form#/definitions/ComposantInteraction/properties/outerClasses")                  |
| [help](#help)                               | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/help")                                                             |
| [pdfBind](#pdfbind)                         | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-pdfbind.md "schemas/form#/definitions/ComposantInteraction/properties/pdfBind")                            |
| [additionals](#additionals-1)               | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-attributs-supplémentaires.md "schemas/form#/definitions/ComposantInteraction/properties/additionals")                                       |
| [v-if](#v-if-3)                             | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-v-if.md "schemas/form#/definitions/ComposantInteraction/properties/v-if")                                  |
| [v-else-value](#v-else-value)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-v-else-value.md "schemas/form#/definitions/ComposantInteraction/properties/v-else-value")                  |
| [helpPosition](#helpposition)               | `string`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-helpposition.md "schemas/form#/definitions/ComposantInteraction/properties/helpPosition")                  |
| [min](#min)                                 | Plusieurs | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-min.md "schemas/form#/definitions/ComposantInteraction/properties/min")                                    |
| [max](#max)                                 | Plusieurs | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-max.md "schemas/form#/definitions/ComposantInteraction/properties/max")                                    |
| [addLabel](#addlabel)                       | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/addLabel")                                                         |
| [removeLabel](#removelabel)                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/removeLabel")                                                      |
| [instanceLabel](#instancelabel)             | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/instanceLabel")                                                    |
| [tooltip](#tooltip)                         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-infobulle.md "schemas/form#/definitions/ComposantInteraction/properties/tooltip")                                                           |
| [options](#options)                         | Plusieurs | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-options.md "schemas/form#/definitions/ComposantInteraction/properties/options")                            |
| [nomDocument](#nomdocument)                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ComposantInteraction/properties/nomDocument")                                                      |
| [afficherBlocCode](#afficherbloccode-1)     | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-afficherbloccode.md "schemas/form#/definitions/ComposantInteraction/properties/afficherBlocCode")          |
| [validations](#validations)                 | `object`  | Optionnel   | peut être nul    | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-validation.md "schemas/form#/definitions/ComposantInteraction/properties/validations")                     |
| [repeatable](#repeatable)                   | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-repeatable.md "schemas/form#/definitions/ComposantInteraction/properties/repeatable")                      |
| [minimum](#minimum)                         | `number`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-minimum.md "schemas/form#/definitions/ComposantInteraction/properties/minimum")                            |
| [components](#components-2)                 | `array`   | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composants.md "schemas/form#/definitions/ComposantInteraction/properties/components")                                                       |
| [disabled](#disabled)                       | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-composant-interaction-properties-disabled.md "schemas/form#/definitions/ComposantInteraction/properties/disabled")                          |

### name

Adds a name attribute, and when used with <FormulateForm> this is the key of the field. If no name is defined a random hash will be assigned

`name`

*   est requis

*   ne peut être nul

#### Type de name

`string`

### type

Required. The type of input element. See the input library for a full range of options.

> **test**

`type`

*   est requis

*   ne peut être nul

#### Type de type

`string`

#### Contraintes de type

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                   | Explication                |
| :----------------------- | :------------------------- |
| `"listeDeroulante"`      |                            |
| `"text"`                 | Champ texte                |
| `"codePostal"`           |                            |
| `"cp12"`                 |                            |
| `"nam"`                  | Numéro d'assurance maladie |
| `"nas"`                  |                            |
| `"montant"`              |                            |
| `"adresse"`              |                            |
| `"button"`               |                            |
| `"submit"`               |                            |
| `"customfile"`           |                            |
| `"customfileUlterieure"` |                            |
| `"file"`                 |                            |
| `"group"`                |                            |
| `"repeatableGroup"`      |                            |
| `"radio"`                |                            |
| `"checkbox"`             |                            |
| `"select"`               |                            |
| `"number"`               |                            |
| `"range"`                |                            |
| `"textarea"`             |                            |
| `"color"`                |                            |
| `"date"`                 |                            |
| `"datetime-local"`       |                            |
| `"email"`                |                            |
| `"hidden"`               |                            |
| `"month"`                |                            |
| `"password"`             |                            |
| `"search"`               |                            |
| `"tel"`                  |                            |
| `"time"`                 |                            |
| `"url"`                  |                            |
| `"week"`                 |                            |

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

Textes multilingue (fr et en supportés seulement)

`validation-name`

*   est optionnel

*   ne peut être nul

#### Type de validation-name

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Messages de validation](frw-form-definitions-composant-interaction-properties-messages-de-validation.md))

### label

Textes multilingue (fr et en supportés seulement)

`label`

*   est optionnel

*   ne peut être nul

#### Type de label

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de label

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### placeholder

Textes multilingue (fr et en supportés seulement)

`placeholder`

*   est optionnel

*   ne peut être nul

#### Type de placeholder

`object` ([Traduction](frw-form-definitions-traduction.md))

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

Textes multilingue (fr et en supportés seulement)

`help`

*   est optionnel

*   ne peut être nul

#### Type de help

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Attributs supplémentaires](frw-form-definitions-attributs-supplémentaires.md))

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

l'un des éléments suivants :`string` ou `number` ([Détails](frw-form-definitions-composant-interaction-properties-min.md))

### max



`max`

*   est optionnel

*   ne peut être nul

#### Type de max

l'un des éléments suivants :`string` ou `number` ([Détails](frw-form-definitions-composant-interaction-properties-max.md))

### addLabel

Textes multilingue (fr et en supportés seulement)

`addLabel`

*   est optionnel

*   ne peut être nul

#### Type de addLabel

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de addLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### removeLabel

Textes multilingue (fr et en supportés seulement)

`removeLabel`

*   est optionnel

*   ne peut être nul

#### Type de removeLabel

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de removeLabel

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### instanceLabel

Textes multilingue (fr et en supportés seulement)

`instanceLabel`

*   est optionnel

*   ne peut être nul

#### Type de instanceLabel

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Infobulle](frw-form-definitions-infobulle.md))

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

l'un des éléments suivants :`object` ou `string` ou `array` ([Détails](frw-form-definitions-composant-interaction-properties-options.md))

#### Exemple de options

```yaml
yesno

```

### nomDocument

Textes multilingue (fr et en supportés seulement)

`nomDocument`

*   est optionnel

*   ne peut être nul

#### Type de nomDocument

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`boolean` ([afficherBlocCode](frw-form-definitions-composant-interaction-properties-afficherbloccode.md))

### validations



`validations`

*   est optionnel

*   peut être nul

#### Type de validations

`object` ([Validation](frw-form-definitions-composant-interaction-properties-validation.md))

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

`object[]` ([Détails](frw-form-definitions-component.md))

### disabled



`disabled`

*   est optionnel

*   ne peut être nul

#### Type de disabled

`boolean`

## Groupe de définitions Additionals

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Additionals"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions Translation

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Translation"}
```

| Propriété                 | Type     | Obligatoire | Nullable      | Défini par                                                                                                                   |
| :------------------------ | :------- | :---------- | :------------ | :--------------------------------------------------------------------------------------------------------------------------- |
| [fr](#fr)                 | `string` | Obligatoire | peut être nul | [Fichier formulaire](frw-form-definitions-traduction-properties-fr.md "schemas/form#/definitions/Translation/properties/fr") |
| [en](#en)                 | `string` | Optionnel   | peut être nul | [Fichier formulaire](frw-form-definitions-traduction-properties-en.md "schemas/form#/definitions/Translation/properties/en") |
| Propriétés Additionnelles | Any      | Optionnel   | can be null   |                                                                                                                              |

### fr

Texte de langue française.

`fr`

*   est requis

*   peut être nul

#### Type de fr

`string` ([fr](frw-form-definitions-traduction-properties-fr.md))

### en

Texte de langue anglaise.

`en`

*   est optionnel

*   peut être nul

#### Type de en

`string` ([en](frw-form-definitions-traduction-properties-en.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Tooltip

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Tooltip"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                    |
| :------------------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------ |
| [title](#title-2)         | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Tooltip/properties/title") |
| [text](#text-1)           | `object` | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Tooltip/properties/text")  |
| Propriétés Additionnelles | Any      | Optionnel   | can be null      |                                                                                                               |

### title

Textes multilingue (fr et en supportés seulement)

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### text

Textes multilingue (fr et en supportés seulement)

`text`

*   est requis

*   ne peut être nul

#### Type de text

`object` ([Traduction](frw-form-definitions-traduction.md))

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
{"$ref":"schemas/form#/definitions/Defaults"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Config

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Config"}
```

| Propriété                                                 | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                       |
| :-------------------------------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherBlocCode](#afficherbloccode-2)                   | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-configuration-du-formulaire-properties-afficherbloccode.md "schemas/form#/definitions/Config/properties/afficherBlocCode")             |
| [afficherPartagePage](#afficherpartagepage)               | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-configuration-du-formulaire-properties-afficherpartagepage.md "schemas/form#/definitions/Config/properties/afficherPartagePage")       |
| [confirmationTransmission](#confirmationtransmission)     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-confirmation-de-transmission.md "schemas/form#/definitions/Config/properties/confirmationTransmission")                                |
| [aiguillage](#aiguillage)                                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage.md "schemas/form#/definitions/Config/properties/aiguillage") |
| [courrielReprise](#courrielreprise)                       | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-courrielreprise.md "schemas/form#/definitions/Config/properties/courrielReprise")                                                      |
| [debuterFormulaire](#debuterformulaire)                   | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-debuterformulaire.md "schemas/form#/definitions/Config/properties/debuterFormulaire")                                                  |
| [domaines](#domaines)                                     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-configuration-du-formulaire-properties-domaines.md "schemas/form#/definitions/Config/properties/domaines")                             |
| [enregistrement](#enregistrement)                         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-enregistrement.md "schemas/form#/definitions/Config/properties/enregistrement")                                                        |
| [formulaireUnilingue](#formulaireunilingue)               | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-configuration-du-formulaire-properties-formulaireunilingue.md "schemas/form#/definitions/Config/properties/formulaireUnilingue")       |
| [injecterJs](#injecterjs)                                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-scripts-vuejs-à-injecter-au-formulaire.md "schemas/form#/definitions/Config/properties/injecterJs")                                    |
| [messages](#messages)                                     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-messages.md "schemas/form#/definitions/Config/properties/messages")                                                                    |
| [pages](#pages)                                           | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-pages.md "schemas/form#/definitions/Config/properties/pages")                                                                          |
| [piv](#piv)                                               | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-piv.md "schemas/form#/definitions/Config/properties/piv")                                                                              |
| [revision](#revision)                                     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-page-de-révision.md "schemas/form#/definitions/Config/properties/revision")                                                            |
| [scripts](#scripts)                                       | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-scripts.md "schemas/form#/definitions/Config/properties/scripts")                                                                      |
| [securite](#securite)                                     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-sécurité-du-formulaire.md "schemas/form#/definitions/Config/properties/securite")                                                      |
| [soumission](#soumission)                                 | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-page-de-soumission.md "schemas/form#/definitions/Config/properties/soumission")                                                        |
| [title](#title-3)                                         | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Config/properties/title")                                                                     |
| [plageEffectiviteFormulaire](#plageeffectiviteformulaire) | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-plageeffectiviteformulaire.md "schemas/form#/definitions/Config/properties/plageEffectiviteFormulaire")                                |

### afficherBlocCode

(Réservé) Afficher un bloc de code des éléments du formulaire.

`afficherBlocCode`

*   est optionnel

*   ne peut être nul

#### Type de afficherBlocCode

`boolean` ([afficherBlocCode](frw-form-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

### afficherPartagePage

(Avancé) ajoute un bouton partage dans toutes les pages à la droite du titre de la page.

`afficherPartagePage`

*   est optionnel

*   ne peut être nul

#### Type de afficherPartagePage

`boolean` ([afficherPartagePage](frw-form-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

### confirmationTransmission



`confirmationTransmission`

*   est optionnel

*   ne peut être nul

#### Type de confirmationTransmission

`object` ([Confirmation de transmission](frw-form-definitions-confirmation-de-transmission.md))

### aiguillage



`aiguillage`

*   est optionnel

*   ne peut être nul

#### Type de aiguillage

`object` ([Défini le comportement final du formulaire selon des critères d'aiguillage.](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage.md))

### courrielReprise

Paramètres associés au courriel de reprise.

`courrielReprise`

*   est optionnel

*   ne peut être nul

#### Type de courrielReprise

`object` ([courrielReprise](frw-form-definitions-courrielreprise.md))

### debuterFormulaire

Paramètres de la page permettant de débuter un formulaire.

`debuterFormulaire`

*   est optionnel

*   ne peut être nul

#### Type de debuterFormulaire

`object` ([debuterFormulaire](frw-form-definitions-debuterformulaire.md))

### domaines

Définition des domaines de valeurs.

`domaines`

*   est optionnel

*   ne peut être nul

#### Type de domaines

`object` ([domaines](frw-form-definitions-configuration-du-formulaire-properties-domaines.md))

#### Contraintes de domaines

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

### enregistrement

Paramètres associés à l'enregistrement d'un formulaire

`enregistrement`

*   est optionnel

*   ne peut être nul

#### Type de enregistrement

`object` ([enregistrement](frw-form-definitions-enregistrement.md))

### formulaireUnilingue

Retire le selecteur de langue. Le formulaire s'affichera en français seulement.

`formulaireUnilingue`

*   est optionnel

*   ne peut être nul

#### Type de formulaireUnilingue

`boolean`

### injecterJs



`injecterJs`

*   est optionnel

*   ne peut être nul

#### Type de injecterJs

`object` ([Scripts Vue.js à injecter au formulaire.](frw-form-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

### messages

Paramètres associés aux différents messages.

`messages`

*   est optionnel

*   ne peut être nul

#### Type de messages

`object` ([messages](frw-form-definitions-messages.md))

### pages

Paramètres associés à différentes pages.

`pages`

*   est optionnel

*   ne peut être nul

#### Type de pages

`object` ([pages](frw-form-definitions-pages.md))

### piv

Paramètres associés au PIV.

`piv`

*   est optionnel

*   ne peut être nul

#### Type de piv

`object` ([piv](frw-form-definitions-piv.md))

### revision



`revision`

*   est optionnel

*   ne peut être nul

#### Type de revision

`object` ([Page de révision](frw-form-definitions-page-de-révision.md))

### scripts

(Avancé) Paramètres d'injection de javascript.

`scripts`

*   est optionnel

*   ne peut être nul

#### Type de scripts

`object` ([scripts](frw-form-definitions-scripts.md))

### securite



`securite`

*   est optionnel

*   ne peut être nul

#### Type de securite

`object` ([Sécurité du formulaire](frw-form-definitions-sécurité-du-formulaire.md))

### soumission



`soumission`

*   est optionnel

*   ne peut être nul

#### Type de soumission

`object` ([Page de soumission](frw-form-definitions-page-de-soumission.md))

### title

Textes multilingue (fr et en supportés seulement)

`title`

*   est optionnel

*   ne peut être nul

#### Type de title

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### plageEffectiviteFormulaire



`plageEffectiviteFormulaire`

*   est optionnel

*   ne peut être nul

#### Type de plageEffectiviteFormulaire

`object` ([plageEffectiviteFormulaire](frw-form-definitions-plageeffectiviteformulaire.md))

## Groupe de définitions Securite

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Securite"}
```

| Propriété                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                |
| :---------------------------- | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [accesAnonyme](#accesanonyme) | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-sécurité-du-formulaire-properties-accesanonyme.md "schemas/form#/definitions/Securite/properties/accesAnonyme") |

### accesAnonyme

Active l'accès anonyme au formulaire.

`accesAnonyme`

*   est optionnel

*   ne peut être nul

#### Type de accesAnonyme

`boolean`

## Groupe de définitions Enregistrement

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Enregistrement"}
```

| Propriété                                                                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                      |
| :---------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [actif](#actif)                                                               | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-enregistrement-properties-actif.md "schemas/form#/definitions/Enregistrement/properties/actif")                                       |
| [afficherMessageIncitatif](#affichermessageincitatif)                         | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-enregistrement-properties-affichermessageincitatif.md "schemas/form#/definitions/Enregistrement/properties/afficherMessageIncitatif") |
| [texteModaleEnregistrementAuthentifie](#textemodaleenregistrementauthentifie) | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")                             |

### actif

Indique si l'enregistrement du formulaire est actif (bouton enregistré présent et enregistrement au changement de page).

`actif`

*   est optionnel

*   ne peut être nul

#### Type de actif

`boolean` ([actif](frw-form-definitions-enregistrement-properties-actif.md))

### afficherMessageIncitatif

Indique si le message (avis avertissement en haut de chaque page) incitant l'enregistrement est affiché ou non.

`afficherMessageIncitatif`

*   est optionnel

*   ne peut être nul

#### Type de afficherMessageIncitatif

`boolean` ([afficherMessageIncitatif](frw-form-definitions-enregistrement-properties-affichermessageincitatif.md))

### texteModaleEnregistrementAuthentifie

Textes multilingue (fr et en supportés seulement)

`texteModaleEnregistrementAuthentifie`

*   est optionnel

*   ne peut être nul

#### Type de texteModaleEnregistrementAuthentifie

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de texteModaleEnregistrementAuthentifie

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions ConfirmationTransmission

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/ConfirmationTransmission"}
```

| Propriété                                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                    |
| :---------------------------------------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [texteSupplementaire](#textesupplementaire)                 | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ConfirmationTransmission/properties/texteSupplementaire")                                                                  |
| [nomChampCourrielUtilisateur](#nomchampcourrielutilisateur) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-confirmation-de-transmission-properties-nomchampcourrielutilisateur.md "schemas/form#/definitions/ConfirmationTransmission/properties/nomChampCourrielUtilisateur") |
| [modaleCourrielConfirmation](#modalecourrielconfirmation)   | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-fenêtre-modale-de-courriel-de-confirmation.md "schemas/form#/definitions/ConfirmationTransmission/properties/modaleCourrielConfirmation")                           |

### texteSupplementaire

Textes multilingue (fr et en supportés seulement)

`texteSupplementaire`

*   est optionnel

*   ne peut être nul

#### Type de texteSupplementaire

`object` ([Traduction](frw-form-definitions-traduction.md))

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

`object` ([Fenêtre modale de courriel de confirmation](frw-form-definitions-fenêtre-modale-de-courriel-de-confirmation.md))

## Groupe de définitions Aiguillage

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Aiguillage"}
```

| Propriété       | Type    | Obligatoire | Nullable         | Défini par                                                                                                                                                                                       |
| :-------------- | :------ | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [choix](#choix) | `array` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-properties-choix.md "schemas/form#/definitions/Aiguillage/properties/choix") |

### choix

Liste de choix pour l'aiguillage

`choix`

*   est optionnel

*   ne peut être nul

#### Type de choix

`object[]` ([Défini le comportement final du formulaire selon des critères d'aiguillage.](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1.md))

## Groupe de définitions Choix

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Choix"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                              |
| :------------------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [vif](#vif)               | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1-properties-vif.md "schemas/form#/definitions/Choix/properties/vif")               |
| [mode](#mode)             | `string` | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1-properties-mode.md "schemas/form#/definitions/Choix/properties/mode")             |
| [formulaire](#formulaire) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1-properties-formulaire.md "schemas/form#/definitions/Choix/properties/formulaire") |

### vif

Condition d'aiguillage

`vif`

*   est optionnel

*   ne peut être nul

#### Type de vif

`string`

### mode

Mode d'aiguillage

`mode`

*   est requis

*   ne peut être nul

#### Type de mode

`string`

#### Contraintes de mode

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                    | Explication |
| :------------------------ | :---------- |
| `"redirectionFormulaire"` |             |
| `"redirectionUrl"`        |             |
| `"confirmation"`          |             |

### formulaire

Nom du formulaire de destination (mode redirectionFormulaire).

`formulaire`

*   est optionnel

*   ne peut être nul

#### Type de formulaire

`string`

## Groupe de définitions CourrielReprise

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/CourrielReprise"}
```

| Propriété                                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                            |
| :---------------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [courrielExpediteur](#courrielexpediteur) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-courrielreprise-properties-courrielexpediteur.md "schemas/form#/definitions/CourrielReprise/properties/courrielExpediteur") |
| [nomExpediteur](#nomexpediteur)           | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-courrielreprise-properties-courrielexpediteur-1.md "schemas/form#/definitions/CourrielReprise/properties/nomExpediteur")    |
| [objet](#objet)                           | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/CourrielReprise/properties/objet")                                                 |
| [corps](#corps)                           | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/CourrielReprise/properties/corps")                                                 |

### courrielExpediteur

Adresse courriel expéditeur.

`courrielExpediteur`

*   est optionnel

*   ne peut être nul

#### Type de courrielExpediteur

`string` ([courrielExpediteur](frw-form-definitions-courrielreprise-properties-courrielexpediteur.md))

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

`string` ([courrielExpediteur](frw-form-definitions-courrielreprise-properties-courrielexpediteur-1.md))

#### Exemple de nomExpediteur

```yaml
Formulaires en ligne - MESS

```

### objet

Textes multilingue (fr et en supportés seulement)

`objet`

*   est optionnel

*   ne peut être nul

#### Type de objet

`object` ([Traduction](frw-form-definitions-traduction.md))

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

Textes multilingue (fr et en supportés seulement)

`corps`

*   est optionnel

*   ne peut être nul

#### Type de corps

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de corps

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions DebuterFormulaire

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/DebuterFormulaire"}
```

| Propriété                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :-------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [authentifie](#authentifie) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-debuterformulaire-properties-authentifie.md "schemas/form#/definitions/DebuterFormulaire/properties/authentifie") |
| [anonyme](#anonyme)         | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-debuterformulaire-properties-anonyme.md "schemas/form#/definitions/DebuterFormulaire/properties/anonyme")         |

### authentifie

Paramètres de la page permettant de débuter un formulaire authentifié.

`authentifie`

*   est optionnel

*   ne peut être nul

#### Type de authentifie

`object` ([authentifie](frw-form-definitions-debuterformulaire-properties-authentifie.md))

### anonyme

Paramètres de la page permettant de débuter un formulaire anonyme.

`anonyme`

*   est optionnel

*   ne peut être nul

#### Type de anonyme

`object` ([anonyme](frw-form-definitions-debuterformulaire-properties-anonyme.md))

## Groupe de définitions Messages

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Messages"}
```

| Propriété                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                        |
| :---------------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------ |
| [erreurTechnique](#erreurtechnique) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-messages-properties-erreurtechnique.md "schemas/form#/definitions/Messages/properties/erreurTechnique") |

### erreurTechnique

Paramètres du message d'erreur technique.

`erreurTechnique`

*   est optionnel

*   ne peut être nul

#### Type de erreurTechnique

`object` ([erreurTechnique](frw-form-definitions-messages-properties-erreurtechnique.md))

## Groupe de définitions Pages

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Pages"}
```

| Propriété                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                          |
| :------------------------------------------ | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| [sessionInvalide](#sessioninvalide)         | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-pages-properties-sessioninvalide.md "schemas/form#/definitions/Pages/properties/sessionInvalide")         |
| [formulaireDesactive](#formulairedesactive) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-pages-properties-formulairedesactive.md "schemas/form#/definitions/Pages/properties/formulaireDesactive") |

### sessionInvalide

Paramètres associés à la page de session invalide.

`sessionInvalide`

*   est optionnel

*   ne peut être nul

#### Type de sessionInvalide

`object` ([sessionInvalide](frw-form-definitions-pages-properties-sessioninvalide.md))

### formulaireDesactive

Paramètres associés à la page de formulaire désactivé.

`formulaireDesactive`

*   est optionnel

*   ne peut être nul

#### Type de formulaireDesactive

`object` ([formulaireDesactive](frw-form-definitions-pages-properties-formulairedesactive.md))

## Groupe de définitions Revision

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Revision"}
```

| Propriété                                       | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                            |
| :---------------------------------------------- | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [validationAutomatique](#validationautomatique) | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-page-de-révision-properties-validationautomatique.md "schemas/form#/definitions/Revision/properties/validationAutomatique") |

### validationAutomatique

Indique si la validation du formulaire est exécutée dès que la page révision est accédée, évitant ainsi à l'utilisateur de cliquer sur le bouton 'Valider'. Utile lorsqu'aucune consigne particulière ne doit être affichée avant la validation.

`validationAutomatique`

*   est optionnel

*   ne peut être nul

#### Type de validationAutomatique

`boolean`

## Groupe de définitions Soumission

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Soumission"}
```

| Propriété                                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                      |
| :-------------------------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------ |
| [texteBoutonSoumettre](#texteboutonsoumettre) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Soumission/properties/texteBoutonSoumettre") |

### texteBoutonSoumettre

Textes multilingue (fr et en supportés seulement)

`texteBoutonSoumettre`

*   est optionnel

*   ne peut être nul

#### Type de texteBoutonSoumettre

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de texteBoutonSoumettre

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions PlageEffectiviteFormulaire

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/PlageEffectiviteFormulaire"}
```

| Propriété                                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                    |
| :------------------------------------------ | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [dateDebut](#datedebut)                     | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-plageeffectiviteformulaire-properties-datedebut.md "schemas/form#/definitions/PlageEffectiviteFormulaire/properties/dateDebut")                     |
| [dateFin](#datefin)                         | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-plageeffectiviteformulaire-properties-datefin.md "schemas/form#/definitions/PlageEffectiviteFormulaire/properties/dateFin")                         |
| [nbJoursDelaiReprise](#nbjoursdelaireprise) | `number` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-plageeffectiviteformulaire-properties-nbjoursdelaireprise.md "schemas/form#/definitions/PlageEffectiviteFormulaire/properties/nbJoursDelaiReprise") |

### dateDebut



`dateDebut`

*   est optionnel

*   ne peut être nul

#### Type de dateDebut

`string`

### dateFin



`dateFin`

*   est optionnel

*   ne peut être nul

#### Type de dateFin

`string`

### nbJoursDelaiReprise



`nbJoursDelaiReprise`

*   est optionnel

*   ne peut être nul

#### Type de nbJoursDelaiReprise

`number`

## Groupe de définitions ModaleCourrielConfirmation

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/ModaleCourrielConfirmation"}
```

| Propriété         | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                        |
| :---------------- | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif-1) | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-fenêtre-modale-de-courriel-de-confirmation-properties-actif.md "schemas/form#/definitions/ModaleCourrielConfirmation/properties/actif") |

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
{"$ref":"schemas/form#/definitions/ValidationMessages"}
```

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                |
| :--------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/ValidationMessages/patternProperties/^\[a-zA-Z0-9]+$") |

### Modèle:`^[a-zA-Z0-9]+$`

Textes multilingue (fr et en supportés seulement)

`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de ^\[a-zA-Z0-9]+$

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions Domaines

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Domaines"}
```

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                  |
| :--------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-valeurelementdomaine.md "schemas/form#/definitions/NomDomaine/patternProperties/^\[a-zA-Z0-9]+$") |

### Modèle:`^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([Nom du domaine de valeurs](frw-form-definitions-valeurelementdomaine.md))

#### Contraintes de ^\[a-zA-Z0-9]+$

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

## Groupe de définitions NomDomaine

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/NomDomaine"}
```

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                  |
| :--------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------ |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-valeurelementdomaine.md "schemas/form#/definitions/NomDomaine/patternProperties/^\[a-zA-Z0-9]+$") |

### Modèle:`^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([Nom du domaine de valeurs](frw-form-definitions-valeurelementdomaine.md))

#### Contraintes de ^\[a-zA-Z0-9]+$

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

## Groupe de définitions ValeurElementDomaine

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/ValeurElementDomaine"}
```

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                            |
| :--------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-valeurelementdomaine-patternproperties-valeur-de-lélément-du-domaine.md "schemas/form#/definitions/ValeurElementDomaine/patternProperties/^\[a-zA-Z0-9]+$") |

### Modèle:`^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([Valeur de l'élément du domaine](frw-form-definitions-valeurelementdomaine-patternproperties-valeur-de-lélément-du-domaine.md))

#### Contraintes de ^\[a-zA-Z0-9]+$

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

## Groupe de définitions InjecterJs

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/InjecterJs"}
```

| Propriété             | Type     | Obligatoire | Nullable         | Défini par                                                                                                           |
| :-------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------- |
| [method](#method)     | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-nomfonction.md "schemas/form#/definitions/InjecterJs/properties/method")   |
| [computed](#computed) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-nomfonction.md "schemas/form#/definitions/InjecterJs/properties/computed") |
| [watch](#watch)       | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-nomfonction.md "schemas/form#/definitions/InjecterJs/properties/watch")    |

### method

Méthodes de type 'method' à injecter au code au modèle vue.js du formulaire.

`method`

*   est optionnel

*   ne peut être nul

#### Type de method

`object` ([method](frw-form-definitions-nomfonction.md))

### computed

Méthodes de type 'computed' à injecter au code au modèle vue.js du formulaire.

`computed`

*   est optionnel

*   ne peut être nul

#### Type de computed

`object` ([computed](frw-form-definitions-nomfonction.md))

### watch

Méthodes de type 'watch' à injecter au code au modèle vue.js du formulaire.

`watch`

*   est optionnel

*   ne peut être nul

#### Type de watch

`object` ([watch](frw-form-definitions-nomfonction.md))

## Groupe de définitions NomFonction

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/NomFonction"}
```

| Propriété        | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                   |
| :--------------- | :------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$` | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md "schemas/form#/definitions/NomFonction/patternProperties/^\[a-zA-Z0-9]+$") |

### Modèle:`^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([Nom de la fonction Vue.js à injecter dans le formulaire](frw-form-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md))

## Groupe de définitions Code

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Code"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions Scripts

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Scripts"}
```

| Propriété                               | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                          |
| :-------------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------- |
| [outilStatistiques](#outilstatistiques) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-scripts-properties-outilstatistiques.md "schemas/form#/definitions/Scripts/properties/outilStatistiques") |

### outilStatistiques

Javascript servant à une solution d'outil statistiques (ex. Google Analytics ou Matomo). Injecté dans toutes les pages à la fin du body.

`outilStatistiques`

*   est optionnel

*   ne peut être nul

#### Type de outilStatistiques

`string` ([outilStatistiques](frw-form-definitions-scripts-properties-outilstatistiques.md))

#### Exemple de outilStatistiques

```yaml
<script> // Votre js ici... </script>

```

## Groupe de définitions Piv

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Piv"}
```

| Propriété                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                       |
| :-------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------- |
| [entete](#entete)           | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-entete.md "schemas/form#/definitions/Piv/properties/entete")           |
| [piedPage](#piedpage)       | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-piedpage.md "schemas/form#/definitions/Piv/properties/piedPage")       |
| [nousJoindre](#nousjoindre) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-nousjoindre.md "schemas/form#/definitions/Piv/properties/nousJoindre") |

### entete



`entete`

*   est optionnel

*   ne peut être nul

#### Type de entete

`object` ([entete](frw-form-definitions-entete.md))

### piedPage



`piedPage`

*   est optionnel

*   ne peut être nul

#### Type de piedPage

`object` ([piedPage](frw-form-definitions-piedpage.md))

### nousJoindre

Permet d'afficher un lien 'Nous joindre' en dessous du changement de langue

`nousJoindre`

*   est optionnel

*   ne peut être nul

#### Type de nousJoindre

`object` ([nousJoindre](frw-form-definitions-nousjoindre.md))

## Groupe de définitions Entete

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Entete"}
```

| Propriété                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                             |
| :---------------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------- |
| [nomSiteMOLigne1](#nomsitemoligne1) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Entete/properties/nomSiteMOLigne1") |
| [nomSiteMOLigne2](#nomsitemoligne2) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Entete/properties/nomSiteMOLigne2") |

### nomSiteMOLigne1

Textes multilingue (fr et en supportés seulement)

`nomSiteMOLigne1`

*   est optionnel

*   ne peut être nul

#### Type de nomSiteMOLigne1

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de nomSiteMOLigne1

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### nomSiteMOLigne2

Textes multilingue (fr et en supportés seulement)

`nomSiteMOLigne2`

*   est optionnel

*   ne peut être nul

#### Type de nomSiteMOLigne2

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de nomSiteMOLigne2

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions NousJoindre

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/NousJoindre"}
```

| Propriété           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                          |
| :------------------ | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif-2)   | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-nousjoindre-properties-actif.md "schemas/form#/definitions/NousJoindre/properties/actif") |
| [texte](#texte)     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/NousJoindre/properties/texte")                   |
| [urlLien](#urllien) | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/NousJoindre/properties/urlLien")                 |

### actif



`actif`

*   est optionnel

*   ne peut être nul

#### Type de actif

`boolean`

### texte

Textes multilingue (fr et en supportés seulement)

`texte`

*   est optionnel

*   ne peut être nul

#### Type de texte

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de texte

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### urlLien

Textes multilingue (fr et en supportés seulement)

`urlLien`

*   est optionnel

*   ne peut être nul

#### Type de urlLien

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de urlLien

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## Groupe de définitions PiedPage

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/PiedPage"}
```

| Propriété     | Type     | Obligatoire | Nullable         | Défini par                                                                                              |
| :------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------ |
| [logo](#logo) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-logo.md "schemas/form#/definitions/PiedPage/properties/logo") |

### logo

Logo affiché dans le centre du pied de page

`logo`

*   est optionnel

*   ne peut être nul

#### Type de logo

`object` ([logo](frw-form-definitions-logo.md))

## Groupe de définitions Logo

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/form#/definitions/Logo"}
```

| Propriété             | Type     | Obligatoire | Nullable         | Défini par                                                                                                              |
| :-------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------- |
| [base64](#base64-1)   | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Logo/properties/base64")             |
| [width](#width)       | `number` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-logo-properties-width.md "schemas/form#/definitions/Logo/properties/width")   |
| [height](#height)     | `number` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-logo-properties-height.md "schemas/form#/definitions/Logo/properties/height") |
| [alt](#alt-1)         | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-logo-properties-alt.md "schemas/form#/definitions/Logo/properties/alt")       |
| [urlLien](#urllien-1) | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/Logo/properties/urlLien")            |

### base64

Textes multilingue (fr et en supportés seulement)

`base64`

*   est optionnel

*   ne peut être nul

#### Type de base64

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de base64

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### width



`width`

*   est optionnel

*   ne peut être nul

#### Type de width

`number` ([width](frw-form-definitions-logo-properties-width.md))

### height



`height`

*   est optionnel

*   ne peut être nul

#### Type de height

`number` ([height](frw-form-definitions-logo-properties-height.md))

### alt



`alt`

*   est optionnel

*   ne peut être nul

#### Type de alt

`string` ([alt](frw-form-definitions-logo-properties-alt.md))

### urlLien

Textes multilingue (fr et en supportés seulement)

`urlLien`

*   est optionnel

*   ne peut être nul

#### Type de urlLien

`object` ([Traduction](frw-form-definitions-traduction.md))

#### Valeur par défaut de urlLien

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
