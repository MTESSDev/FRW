## Type de Enregistrement

`object` ([enregistrement](frw-definitions-enregistrement.md))

# Propriétés de Enregistrement

| Propriété                                                                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                 |
| :---------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)                                                               | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-enregistrement-properties-actif.md "schemas/form#/definitions/Enregistrement/properties/actif")                                       |
| [afficherMessageIncitatif](#affichermessageincitatif)                         | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-enregistrement-properties-affichermessageincitatif.md "schemas/form#/definitions/Enregistrement/properties/afficherMessageIncitatif") |
| [texteModaleEnregistrementAuthentifie](#textemodaleenregistrementauthentifie) | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-traduction.md "schemas/form#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")                             |

## actif

Indique si l'enregistrement du formulaire est actif (bouton enregistré présent et enregistrement au changement de page).

`actif`

*   est optionnel

*   ne peut être nul

### Type de actif

`boolean` ([actif](frw-definitions-enregistrement-properties-actif.md))

## afficherMessageIncitatif

Indique si le message (avis avertissement en haut de chaque page) incitant l'enregistrement est affiché ou non.

`afficherMessageIncitatif`

*   est optionnel

*   ne peut être nul

### Type de afficherMessageIncitatif

`boolean` ([afficherMessageIncitatif](frw-definitions-enregistrement-properties-affichermessageincitatif.md))

## texteModaleEnregistrementAuthentifie

Textes multilingue (fr et en supportés seulement)

`texteModaleEnregistrementAuthentifie`

*   est optionnel

*   ne peut être nul

### Type de texteModaleEnregistrementAuthentifie

`object` ([Traduction](frw-definitions-traduction.md))

### Valeur par défaut de texteModaleEnregistrementAuthentifie

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
