## Type de NousJoindre

`object` ([nousJoindre](frw-form-definitions-nousjoindre.md))

# Propriétés de NousJoindre

| Propriété           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                          |
| :------------------ | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)     | `boolean` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-nousjoindre-properties-actif.md "schemas/form#/definitions/NousJoindre/properties/actif") |
| [texte](#texte)     | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/NousJoindre/properties/texte")                   |
| [urlLien](#urllien) | `object`  | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/NousJoindre/properties/urlLien")                 |

## actif



`actif`

*   est optionnel

*   ne peut être nul

### Type de actif

`boolean`

## texte

Textes multilingue (fr et en supportés seulement)

`texte`

*   est optionnel

*   ne peut être nul

### Type de texte

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de texte

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## urlLien

Textes multilingue (fr et en supportés seulement)

`urlLien`

*   est optionnel

*   ne peut être nul

### Type de urlLien

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de urlLien

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
