# Schéma de anonyme

```txt
https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme
```

Paramètres de la page permettant de débuter un formulaire anonyme.

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de anonyme

| Propriété                                                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                          |
| :------------------------------------------------------------------ | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [texte](#texte)                                                     | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/texte")                           |
| [boutonDebuter](#boutondebuter)                                     | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/boutonDebuter")                   |
| [boutonDebuterTitreAccessibilite](#boutondebutertitreaccessibilite) | `object` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/DebuterFormulaire/properties/anonyme/properties/boutonDebuterTitreAccessibilite") |

## texte

Multilingue

`texte`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

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

### Valeur par défaut de boutonDebuterTitreAccessibilite

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
