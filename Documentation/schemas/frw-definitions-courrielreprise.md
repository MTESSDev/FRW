# Schéma de courrielReprise

```txt
https://example.com/schemas/custom#/definitions/CourrielReprise
```

Paramètres associés au courriel de reprise.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de CourrielReprise

`object` ([courrielReprise](frw-definitions-courrielreprise.md))

# Propriétés de CourrielReprise

| Propriété                                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                          |
| :---------------------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [courrielExpediteur](#courrielexpediteur) | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-courrielreprise-properties-courrielexpediteur.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/courrielExpediteur") |
| [nomExpediteur](#nomexpediteur)           | `string` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/nomExpediteur")    |
| [objet](#objet)                           | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/objet")                                                |
| [corps](#corps)                           | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/corps")                                                |

## courrielExpediteur

Adresse courriel expéditeur.

`courrielExpediteur`

*   est optionnel

*   Type: `string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-courrielreprise-properties-courrielexpediteur.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/courrielExpediteur")

### Type de courrielExpediteur

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur.md))

### Exemple de courrielExpediteur

```yaml
NEPASREPONDRE@mtess.gouv.qc.ca

```

## nomExpediteur

Nom de l'expéditeur expéditeur.

`nomExpediteur`

*   est optionnel

*   Type: `string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/nomExpediteur")

### Type de nomExpediteur

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md))

### Exemple de nomExpediteur

```yaml
Formulaires en ligne - MESS

```

## objet

Multilingue

`objet`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/objet")

### Type de objet

`object` ([Translation](frw-definitions-translation.md))

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

Multilingue

`corps`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/corps")

### Type de corps

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de corps

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
