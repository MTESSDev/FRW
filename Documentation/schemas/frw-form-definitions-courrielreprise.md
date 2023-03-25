## Type de CourrielReprise

`object` ([courrielReprise](frw-form-definitions-courrielreprise.md))

# Propriétés de CourrielReprise

| Propriété                                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                            |
| :---------------------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [courrielExpediteur](#courrielexpediteur) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-courrielreprise-properties-courrielexpediteur.md "schemas/form#/definitions/CourrielReprise/properties/courrielExpediteur") |
| [nomExpediteur](#nomexpediteur)           | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-courrielreprise-properties-courrielexpediteur-1.md "schemas/form#/definitions/CourrielReprise/properties/nomExpediteur")    |
| [objet](#objet)                           | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/CourrielReprise/properties/objet")                                                 |
| [corps](#corps)                           | `object` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-form-definitions-traduction.md "schemas/form#/definitions/CourrielReprise/properties/corps")                                                 |

## courrielExpediteur

Adresse courriel expéditeur.

`courrielExpediteur`

*   est optionnel

*   ne peut être nul

### Type de courrielExpediteur

`string` ([courrielExpediteur](frw-form-definitions-courrielreprise-properties-courrielexpediteur.md))

### Exemple de courrielExpediteur

```yaml
NEPASREPONDRE@mtess.gouv.qc.ca

```

## nomExpediteur

Nom de l'expéditeur expéditeur.

`nomExpediteur`

*   est optionnel

*   ne peut être nul

### Type de nomExpediteur

`string` ([courrielExpediteur](frw-form-definitions-courrielreprise-properties-courrielexpediteur-1.md))

### Exemple de nomExpediteur

```yaml
Formulaires en ligne - MESS

```

## objet

Textes multilingue (fr et en supportés seulement)

`objet`

*   est optionnel

*   ne peut être nul

### Type de objet

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de objet

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

### Exemple de objet

```yaml
Formulaire  « {0} » incomplet

```

## corps

Textes multilingue (fr et en supportés seulement)

`corps`

*   est optionnel

*   ne peut être nul

### Type de corps

`object` ([Traduction](frw-form-definitions-traduction.md))

### Valeur par défaut de corps

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
