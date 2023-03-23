# Schéma de enregistrement

```txt
https://example.com/schemas/custom#/definitions/Enregistrement
```

Paramètres associés à l'enregistrement d'un formulaire

| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

# Propriétés de Enregistrement

| Propriété                                                                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                    |
| :---------------------------------------------------------------------------- | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [actif](#actif)                                                               | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-enregistrement-properties-actif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/actif")                                       |
| [afficherMessageIncitatif](#affichermessageincitatif)                         | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-enregistrement-properties-affichermessageincitatif.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/afficherMessageIncitatif") |
| [texteModaleEnregistrementAuthentifie](#textemodaleenregistrementauthentifie) | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Enregistrement/properties/texteModaleEnregistrementAuthentifie")                            |

## actif

Indique si l'enregistrement du formulaire est actif (bouton enregistré présent et enregistrement au changement de page).

`actif`

*   est optionnel

*   Type: `boolean` ([actif](frw-definitions-enregistrement-properties-actif.md))

*   ne peut être nul

## afficherMessageIncitatif

Indique si le message (avis avertissement en haut de chaque page) incitant l'enregistrement est affiché ou non.

`afficherMessageIncitatif`

*   est optionnel

*   Type: `boolean` ([afficherMessageIncitatif](frw-definitions-enregistrement-properties-affichermessageincitatif.md))

*   ne peut être nul

## texteModaleEnregistrementAuthentifie

Multilingue

`texteModaleEnregistrementAuthentifie`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

### Valeur par défaut de texteModaleEnregistrementAuthentifie

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
