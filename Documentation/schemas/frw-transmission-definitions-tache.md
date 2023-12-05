## Type de Taches

`object` ([tache](frw-transmission-definitions-tache.md))

## Valeur par défaut de Taches

La valeur par défaut est:

```yaml
tache: genererPdf

```

# Propriétés de Taches

| Propriété                           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                     |
| :---------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [tache](#tache)                     | `string`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-tache-properties-tache.md "schemas/transmission#/definitions/Taches/properties/tache")                     |
| [options](#options)                 | `object`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options.md "schemas/transmission#/definitions/Taches/properties/options")                                  |
| [numeroExecution](#numeroexecution) | `integer` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-tache-properties-numeroexecution.md "schemas/transmission#/definitions/Taches/properties/numeroExecution") |

## tache



`tache`

*   est optionnel

*   ne peut être nul

### Type de tache

`string` ([tache](frw-transmission-definitions-tache-properties-tache.md))

### Contraintes de tache

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur                     | Explication |
| :------------------------- | :---------- |
| `"genererWord"`            |             |
| `"genererPdf"`             |             |
| `"traiterDocumentsSoumis"` |             |
| `"extraireQuestions"`      |             |
| `"ajouterEstampille"`      |             |
| `"appelerServiceExterne"`  |             |
| `"envoyerCourriel"`        |             |

## options



`options`

*   est optionnel

*   ne peut être nul

### Type de options

`object` ([options](frw-transmission-definitions-options.md))

## numeroExecution



`numeroExecution`

*   est optionnel

*   ne peut être nul

### Type de numeroExecution

`integer` ([numeroExecution](frw-transmission-definitions-tache-properties-numeroexecution.md))
