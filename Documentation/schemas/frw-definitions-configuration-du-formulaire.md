# Schéma de Configuration du formulaire

```txt
https://example.com/schemas/custom#/definitions/Config
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de Config

`object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

# Propriétés de Config

| Propriété                                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                               |
| :---------------------------------------------------- | :-------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherBlocCode](#afficherbloccode)                 | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherBlocCode")       |
| [afficherPartagePage](#afficherpartagepage)           | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherPartagePage") |
| [confirmationTransmission](#confirmationtransmission) | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-confirmation-de-transmission.md "https://example.com/schemas/custom#/definitions/Config/properties/confirmationTransmission")                          |
| [courrielReprise](#courrielreprise)                   | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-courrielreprise.md "https://example.com/schemas/custom#/definitions/Config/properties/courrielReprise")                                                |
| [debuterFormulaire](#debuterformulaire)               | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-debuterformulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/debuterFormulaire")                                            |
| [enregistrement](#enregistrement)                     | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-enregistrement.md "https://example.com/schemas/custom#/definitions/Config/properties/enregistrement")                                                  |
| [formulaireUnilingue](#formulaireunilingue)           | `boolean` | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-formulaireunilingue.md "https://example.com/schemas/custom#/definitions/Config/properties/formulaireUnilingue") |
| [gererPlageDisponibilite](#gererplagedisponibilite)   | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-gerer-les-plages-de-disponibilité.md "https://example.com/schemas/custom#/definitions/Config/properties/gererPlageDisponibilite")                      |
| [injecterJs](#injecterjs)                             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/injecterJs")                              |
| [messages](#messages)                                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-messages.md "https://example.com/schemas/custom#/definitions/Config/properties/messages")                                                              |
| [pages](#pages)                                       | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-pages.md "https://example.com/schemas/custom#/definitions/Config/properties/pages")                                                                    |
| [piv](#piv)                                           | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-piv.md "https://example.com/schemas/custom#/definitions/Config/properties/piv")                                 |
| [revision](#revision)                                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-page-de-révision.md "https://example.com/schemas/custom#/definitions/Config/properties/revision")                                                      |
| [scripts](#scripts)                                   | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-scripts.md "https://example.com/schemas/custom#/definitions/Config/properties/scripts")                                                                |
| [securite](#securite)                                 | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-sécurité-du-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/securite")                                                |
| [soumission](#soumission)                             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-page-de-soumission.md "https://example.com/schemas/custom#/definitions/Config/properties/soumission")                                                  |
| [title](#title)                                       | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Config/properties/title")                                                              |

## afficherBlocCode

(Réservé) Afficher un bloc de code des éléments du formulaire.

`afficherBlocCode`

*   est optionnel

*   ne peut être nul

### Type de afficherBlocCode

`boolean` ([afficherBlocCode](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

## afficherPartagePage

(Avancé) ajouter un bouton partage dans toutes les pages à la droite du titre de la page.

`afficherPartagePage`

*   est optionnel

*   ne peut être nul

### Type de afficherPartagePage

`boolean` ([afficherPartagePage](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

## confirmationTransmission



`confirmationTransmission`

*   est optionnel

*   ne peut être nul

### Type de confirmationTransmission

`object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

## courrielReprise

Paramètres associés au courriel de reprise.

`courrielReprise`

*   est optionnel

*   ne peut être nul

### Type de courrielReprise

`object` ([courrielReprise](frw-definitions-courrielreprise.md))

## debuterFormulaire

Paramètres de la page permettant de débuter un formulaire.

`debuterFormulaire`

*   est optionnel

*   ne peut être nul

### Type de debuterFormulaire

`object` ([debuterFormulaire](frw-definitions-debuterformulaire.md))

## enregistrement

Paramètres associés à l'enregistrement d'un formulaire

`enregistrement`

*   est optionnel

*   ne peut être nul

### Type de enregistrement

`object` ([enregistrement](frw-definitions-enregistrement.md))

## formulaireUnilingue

Permet de retirer le selecteur de langue. Le formulaire s'affichera en français seulement.

`formulaireUnilingue`

*   est optionnel

*   ne peut être nul

### Type de formulaireUnilingue

`boolean`

## gererPlageDisponibilite



`gererPlageDisponibilite`

*   est optionnel

*   ne peut être nul

### Type de gererPlageDisponibilite

`object` ([Gerer les plages de disponibilité](frw-definitions-gerer-les-plages-de-disponibilité.md))

## injecterJs



`injecterJs`

*   est optionnel

*   ne peut être nul

### Type de injecterJs

`object` ([Scripts Vue.js à injecter au formulaire.](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

## messages

Paramètres associés aux différents messages.

`messages`

*   est optionnel

*   ne peut être nul

### Type de messages

`object` ([messages](frw-definitions-messages.md))

## pages

Paramètres associés à différentes pages.

`pages`

*   est optionnel

*   ne peut être nul

### Type de pages

`object` ([pages](frw-definitions-pages.md))

## piv

Paramètres associés au PIV.

`piv`

*   est optionnel

*   ne peut être nul

### Type de piv

`object` ([piv](frw-definitions-configuration-du-formulaire-properties-piv.md))

## revision



`revision`

*   est optionnel

*   ne peut être nul

### Type de revision

`object` ([Page de révision](frw-definitions-page-de-révision.md))

## scripts

(Avancé) Paramètres d'injection de javascript.

`scripts`

*   est optionnel

*   ne peut être nul

### Type de scripts

`object` ([scripts](frw-definitions-scripts.md))

## securite



`securite`

*   est optionnel

*   ne peut être nul

### Type de securite

`object` ([Sécurité du formulaire](frw-definitions-sécurité-du-formulaire.md))

## soumission



`soumission`

*   est optionnel

*   ne peut être nul

### Type de soumission

`object` ([Page de soumission](frw-definitions-page-de-soumission.md))

## title

Multilingue

`title`

*   est optionnel

*   ne peut être nul

### Type de title

`object` ([Translation](frw-definitions-translation.md))

### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
