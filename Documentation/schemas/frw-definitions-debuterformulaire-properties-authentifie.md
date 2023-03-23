# Schéma de authentifie

```txt
https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie
```

Paramètres de la page permettant de débuter un formulaire authentifié.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de authentifie

`object` ([authentifie](frw-definitions-debuterformulaire-properties-authentifie.md))

# Propriétés de authentifie

| Propriété                                                           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                  |
| :------------------------------------------------------------------ | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)                                                     | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/actif") |
| [urlAuthentification](#urlauthentification)                         | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/urlAuthentification")                                 |
| [texte](#texte)                                                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/texte")                                               |
| [boutonDebuter](#boutondebuter)                                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuter")                                       |
| [boutonDebuterTitreAccessibilite](#boutondebutertitreaccessibilite) | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuterTitreAccessibilite")                     |

## actif

Indique si la page d'initialisation d'un formulaire est active ou non.

`actif`

*   est optionnel

*   Type: `boolean` ([actif](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/actif")

### Type de actif

`boolean` ([actif](frw-definitions-debuterformulaire-properties-authentifie-properties-actif.md))

## urlAuthentification

Multilingue

`urlAuthentification`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/urlAuthentification")

### Type de urlAuthentification

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de urlAuthentification

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## texte

Multilingue

`texte`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/texte")

### Type de texte

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de texte

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## boutonDebuter

Multilingue

`boutonDebuter`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuter")

### Type de boutonDebuter

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de boutonDebuter

La valeur par défaut est:

```yaml
fr: ''
en: ''

```

## boutonDebuterTitreAccessibilite

Multilingue

`boutonDebuterTitreAccessibilite`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

*   défini dans: [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/authentifie/properties/boutonDebuterTitreAccessibilite")

### Type de boutonDebuterTitreAccessibilite

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de boutonDebuterTitreAccessibilite

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
