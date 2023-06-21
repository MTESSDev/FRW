## Type de Choix

`object` ([Défini le comportement final du formulaire selon des critères d'aiguillage.](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1.md))

# Propriétés de Choix

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                              |
| :------------------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [vif](#vif)               | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1-properties-vif.md "schemas/form#/definitions/Choix/properties/vif")               |
| [mode](#mode)             | `string` | Obligatoire | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1-properties-mode.md "schemas/form#/definitions/Choix/properties/mode")             |
| [formulaire](#formulaire) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-défini-le-comportement-final-du-formulaire-selon-des-critères-daiguillage-1-properties-formulaire.md "schemas/form#/definitions/Choix/properties/formulaire") |

## vif

Condition d'aiguillage

`vif`

*   est optionnel

*   ne peut être nul

### Type de vif

`string`

## mode

Mode d'aiguillage

`mode`

*   est requis

*   ne peut être nul

### Type de mode

`string`

### Contraintes de mode

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                    | Explication |
| :------------------------ | :---------- |
| `"redirectionFormulaire"` |             |
| `"redirectionUrl"`        |             |
| `"confirmation"`          |             |

## formulaire

Nom du formulaire de destination (mode redirectionFormulaire).

`formulaire`

*   est optionnel

*   ne peut être nul

### Type de formulaire

`string`
