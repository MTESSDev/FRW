# Schéma de EcsForm

```txt
https://example.com/schemas/custom#/definitions/EcsForm
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

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

*   Type: `boolean`

*   ne peut être nul

## form

Élément racine d'un formulaire.

`form`

*   est requis

*   Type: `object` ([Form](frw-definitions-form.md))

*   ne peut être nul

## config



`config`

*   est optionnel

*   Type: `object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

*   ne peut être nul

## textes



`textes`

*   est optionnel

*   Type: `object` ([Détails](frw-definitions-ecsform-properties-textes.md))

*   ne peut être nul
