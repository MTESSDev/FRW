# Schéma de Configuration du formulaire

```txt
https://example.com/schemas/custom#/definitions/Config
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

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
| [soumission](#soumission)                             | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-configuration-du-formulaire-properties-page-de-soumission.md "https://example.com/schemas/custom#/definitions/Config/properties/soumission")           |
| [title](#title)                                       | `object`  | Optionnel   | ne peut être nul | [Schéma sans nom](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Config/properties/title")                                                              |

## afficherBlocCode

(Réservé) Afficher un bloc de code des éléments du formulaire.

`afficherBlocCode`

*   est optionnel

*   Type: `boolean` ([afficherBlocCode](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

*   ne peut être nul

## afficherPartagePage

(Avancé) ajouter un bouton partage dans toutes les pages à la droite du titre de la page.

`afficherPartagePage`

*   est optionnel

*   Type: `boolean` ([afficherPartagePage](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

*   ne peut être nul

## confirmationTransmission



`confirmationTransmission`

*   est optionnel

*   Type: `object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

*   ne peut être nul

## courrielReprise

Paramètres associés au courriel de reprise.

`courrielReprise`

*   est optionnel

*   Type: `object` ([courrielReprise](frw-definitions-courrielreprise.md))

*   ne peut être nul

## debuterFormulaire

Paramètres de la page permettant de débuter un formulaire.

`debuterFormulaire`

*   est optionnel

*   Type: `object` ([debuterFormulaire](frw-definitions-debuterformulaire.md))

*   ne peut être nul

## enregistrement

Paramètres associés à l'enregistrement d'un formulaire

`enregistrement`

*   est optionnel

*   Type: `object` ([enregistrement](frw-definitions-enregistrement.md))

*   ne peut être nul

## formulaireUnilingue

Permet de retirer le selecteur de langue. Le formulaire s'affichera en français seulement.

`formulaireUnilingue`

*   est optionnel

*   Type: `boolean`

*   ne peut être nul

## gererPlageDisponibilite



`gererPlageDisponibilite`

*   est optionnel

*   Type: `object` ([Gerer les plages de disponibilité](frw-definitions-gerer-les-plages-de-disponibilité.md))

*   ne peut être nul

## injecterJs



`injecterJs`

*   est optionnel

*   Type: `object` ([Scripts Vue.js à injecter au formulaire.](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

*   ne peut être nul

## messages

Paramètres associés aux différents messages.

`messages`

*   est optionnel

*   Type: `object` ([messages](frw-definitions-messages.md))

*   ne peut être nul

## pages

Paramètres associés à différentes pages.

`pages`

*   est optionnel

*   Type: `object` ([pages](frw-definitions-pages.md))

*   ne peut être nul

## piv

Paramètres associés au PIV.

`piv`

*   est optionnel

*   Type: `object` ([piv](frw-definitions-configuration-du-formulaire-properties-piv.md))

*   ne peut être nul

## revision



`revision`

*   est optionnel

*   Type: `object` ([Page de révision](frw-definitions-page-de-révision.md))

*   ne peut être nul

## scripts

(Avancé) Paramètres d'injection de javascript.

`scripts`

*   est optionnel

*   Type: `object` ([scripts](frw-definitions-scripts.md))

*   ne peut être nul

## securite



`securite`

*   est optionnel

*   Type: `object` ([Sécurité du formulaire](frw-definitions-sécurité-du-formulaire.md))

*   ne peut être nul

## soumission



`soumission`

*   est optionnel

*   Type: `object` ([Page de soumission](frw-definitions-configuration-du-formulaire-properties-page-de-soumission.md))

*   ne peut être nul

## title

Multilingue

`title`

*   est optionnel

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   ne peut être nul

### Valeur par défaut de title

La valeur par défaut est:

```yaml
fr: ''
en: ''

```
