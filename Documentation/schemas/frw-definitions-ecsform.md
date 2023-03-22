# EcsForm Schema

```txt
https://example.com/schemas/custom#/definitions/EcsForm
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## EcsForm Type

`object` ([EcsForm](frw-definitions-ecsform.md))

# EcsForm Properties

| Property                                                                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                                                      |
| :------------------------------------------------------------------------------------ | :-------- | :------- | :------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherMessageSauvegardeCourrielReprise](#affichermessagesauvegardecourrielreprise) | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-ecsform-properties-affichermessagesauvegardecourrielreprise.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/afficherMessageSauvegardeCourrielReprise") |
| [form](#form)                                                                         | `object`  | Required | cannot be null | [Untitled schema](frw-definitions-form.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/form")                                                                                            |
| [config](#config)                                                                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/config")                                                                   |
| [textes](#textes)                                                                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-ecsform-properties-textes.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/textes")                                                                     |

## afficherMessageSauvegardeCourrielReprise

DEPRECATED (Utiliser maintenant enregistrement.afficherMessageIncitatif)

`afficherMessageSauvegardeCourrielReprise`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-ecsform-properties-affichermessagesauvegardecourrielreprise.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/afficherMessageSauvegardeCourrielReprise")

### afficherMessageSauvegardeCourrielReprise Type

`boolean`

## form

Élément racine d'un formulaire.

`form`

*   is required

*   Type: `object` ([Form](frw-definitions-form.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-form.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/form")

### form Type

`object` ([Form](frw-definitions-form.md))

## config



`config`

*   is optional

*   Type: `object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/config")

### config Type

`object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

## textes



`textes`

*   is optional

*   Type: `object` ([Details](frw-definitions-ecsform-properties-textes.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-ecsform-properties-textes.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/textes")

### textes Type

`object` ([Details](frw-definitions-ecsform-properties-textes.md))
