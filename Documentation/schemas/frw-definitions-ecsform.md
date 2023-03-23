## Type de EcsForm

`object` ([EcsForm](frw-definitions-ecsform.md))

# Propriétés de EcsForm

| Propriété                                                                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                      |
| :------------------------------------------------------------------------------------ | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherMessageSauvegardeCourrielReprise](#affichermessagesauvegardecourrielreprise) | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-ecsform-properties-affichermessagesauvegardecourrielreprise.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/afficherMessageSauvegardeCourrielReprise") |
| [form](#form)                                                                         | `object`  | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-form.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/form")                                                                                            |
| [config](#config)                                                                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/config")                                                                   |
| [textes](#textes)                                                                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-ecsform-properties-textes.md "https://example.com/schemas/custom#/definitions/EcsForm/properties/textes")                                                                     |

## afficherMessageSauvegardeCourrielReprise

DEPRECATED (Utiliser maintenant enregistrement.afficherMessageIncitatif)

`afficherMessageSauvegardeCourrielReprise`

*   est optionnel

*   ne peut être nul

### Type de afficherMessageSauvegardeCourrielReprise

`boolean`

## form

Élément racine d'un formulaire.

`form`

*   est requis

*   ne peut être nul

### Type de form

`object` ([Form](frw-definitions-form.md))

## config



`config`

*   est optionnel

*   ne peut être nul

### Type de config

`object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

## textes



`textes`

*   est optionnel

*   ne peut être nul

### Type de textes

`object` ([Détails](frw-definitions-ecsform-properties-textes.md))
