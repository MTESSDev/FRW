# Configuration du formulaire Schema

```txt
https://example.com/schemas/custom#/definitions/Config
```



| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## Config Type

`object` ([Configuration du formulaire](frw-definitions-configuration-du-formulaire.md))

# Config Properties

| Property                                              | Type      | Required | Nullable       | Defined by                                                                                                                                                                               |
| :---------------------------------------------------- | :-------- | :------- | :------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [afficherBlocCode](#afficherbloccode)                 | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherBlocCode")       |
| [afficherPartagePage](#afficherpartagepage)           | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherPartagePage") |
| [confirmationTransmission](#confirmationtransmission) | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-confirmation-de-transmission.md "https://example.com/schemas/custom#/definitions/Config/properties/confirmationTransmission")                          |
| [courrielReprise](#courrielreprise)                   | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-courrielreprise.md "https://example.com/schemas/custom#/definitions/Config/properties/courrielReprise")                                                |
| [debuterFormulaire](#debuterformulaire)               | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-debuterformulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/debuterFormulaire")                                            |
| [enregistrement](#enregistrement)                     | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-enregistrement.md "https://example.com/schemas/custom#/definitions/Config/properties/enregistrement")                                                  |
| [formulaireUnilingue](#formulaireunilingue)           | `boolean` | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-formulaireunilingue.md "https://example.com/schemas/custom#/definitions/Config/properties/formulaireUnilingue") |
| [gererPlageDisponibilite](#gererplagedisponibilite)   | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité.md "https://example.com/schemas/custom#/definitions/Config/properties/gererPlageDisponibilite")                      |
| [injecterJs](#injecterjs)                             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/injecterJs")                              |
| [messages](#messages)                                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-messages.md "https://example.com/schemas/custom#/definitions/Config/properties/messages")                                                              |
| [pages](#pages)                                       | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-pages.md "https://example.com/schemas/custom#/definitions/Config/properties/pages")                                                                    |
| [piv](#piv)                                           | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-configuration-du-formulaire-properties-piv.md "https://example.com/schemas/custom#/definitions/Config/properties/piv")                                 |
| [revision](#revision)                                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-page-de-révision.md "https://example.com/schemas/custom#/definitions/Config/properties/revision")                                                      |
| [scripts](#scripts)                                   | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-scripts.md "https://example.com/schemas/custom#/definitions/Config/properties/scripts")                                                                |
| [securite](#securite)                                 | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-sécurité-du-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/securite")                                                |
| [soumission](#soumission)                             | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-page-de-soumission.md "https://example.com/schemas/custom#/definitions/Config/properties/soumission")                                                  |
| [title](#title)                                       | `object`  | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Config/properties/title")                                                              |

## afficherBlocCode

(Réservé) Afficher un bloc de code des éléments du formulaire.

`afficherBlocCode`

*   is optional

*   Type: `boolean` ([afficherBlocCode](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherBlocCode")

### afficherBlocCode Type

`boolean` ([afficherBlocCode](frw-definitions-configuration-du-formulaire-properties-afficherbloccode.md))

## afficherPartagePage

(Avancé) ajouter un bouton partage dans toutes les pages à la droite du titre de la page.

`afficherPartagePage`

*   is optional

*   Type: `boolean` ([afficherPartagePage](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md "https://example.com/schemas/custom#/definitions/Config/properties/afficherPartagePage")

### afficherPartagePage Type

`boolean` ([afficherPartagePage](frw-definitions-configuration-du-formulaire-properties-afficherpartagepage.md))

## confirmationTransmission



`confirmationTransmission`

*   is optional

*   Type: `object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-confirmation-de-transmission.md "https://example.com/schemas/custom#/definitions/Config/properties/confirmationTransmission")

### confirmationTransmission Type

`object` ([Confirmation de transmission](frw-definitions-confirmation-de-transmission.md))

## courrielReprise

Paramètres associés au courriel de reprise.

`courrielReprise`

*   is optional

*   Type: `object` ([courrielReprise](frw-definitions-courrielreprise.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-courrielreprise.md "https://example.com/schemas/custom#/definitions/Config/properties/courrielReprise")

### courrielReprise Type

`object` ([courrielReprise](frw-definitions-courrielreprise.md))

## debuterFormulaire

Paramètres de la page permettant de débuter un formulaire.

`debuterFormulaire`

*   is optional

*   Type: `object` ([debuterFormulaire](frw-definitions-debuterformulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-debuterformulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/debuterFormulaire")

### debuterFormulaire Type

`object` ([debuterFormulaire](frw-definitions-debuterformulaire.md))

## enregistrement

Paramètres associés à l'enregistrement d'un formulaire

`enregistrement`

*   is optional

*   Type: `object` ([enregistrement](frw-definitions-enregistrement.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-enregistrement.md "https://example.com/schemas/custom#/definitions/Config/properties/enregistrement")

### enregistrement Type

`object` ([enregistrement](frw-definitions-enregistrement.md))

## formulaireUnilingue

Permet de retirer le selecteur de langue. Le formulaire s'affichera en français seulement.

`formulaireUnilingue`

*   is optional

*   Type: `boolean`

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-formulaireunilingue.md "https://example.com/schemas/custom#/definitions/Config/properties/formulaireUnilingue")

### formulaireUnilingue Type

`boolean`

## gererPlageDisponibilite



`gererPlageDisponibilite`

*   is optional

*   Type: `object` ([Gerer les plages de disponibilité](frw-definitions-gerer-les-plages-de-disponibilité.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-gerer-les-plages-de-disponibilité.md "https://example.com/schemas/custom#/definitions/Config/properties/gererPlageDisponibilite")

### gererPlageDisponibilite Type

`object` ([Gerer les plages de disponibilité](frw-definitions-gerer-les-plages-de-disponibilité.md))

## injecterJs



`injecterJs`

*   is optional

*   Type: `object` ([Scripts Vue.js à injecter au formulaire.](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/injecterJs")

### injecterJs Type

`object` ([Scripts Vue.js à injecter au formulaire.](frw-definitions-scripts-vuejs-à-injecter-au-formulaire.md))

## messages

Paramètres associés aux différents messages.

`messages`

*   is optional

*   Type: `object` ([messages](frw-definitions-messages.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-messages.md "https://example.com/schemas/custom#/definitions/Config/properties/messages")

### messages Type

`object` ([messages](frw-definitions-messages.md))

## pages

Paramètres associés à différentes pages.

`pages`

*   is optional

*   Type: `object` ([pages](frw-definitions-pages.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-pages.md "https://example.com/schemas/custom#/definitions/Config/properties/pages")

### pages Type

`object` ([pages](frw-definitions-pages.md))

## piv

Paramètres associés au PIV.

`piv`

*   is optional

*   Type: `object` ([piv](frw-definitions-configuration-du-formulaire-properties-piv.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-configuration-du-formulaire-properties-piv.md "https://example.com/schemas/custom#/definitions/Config/properties/piv")

### piv Type

`object` ([piv](frw-definitions-configuration-du-formulaire-properties-piv.md))

## revision



`revision`

*   is optional

*   Type: `object` ([Page de révision](frw-definitions-page-de-révision.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-page-de-révision.md "https://example.com/schemas/custom#/definitions/Config/properties/revision")

### revision Type

`object` ([Page de révision](frw-definitions-page-de-révision.md))

## scripts

(Avancé) Paramètres d'injection de javascript.

`scripts`

*   is optional

*   Type: `object` ([scripts](frw-definitions-scripts.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-scripts.md "https://example.com/schemas/custom#/definitions/Config/properties/scripts")

### scripts Type

`object` ([scripts](frw-definitions-scripts.md))

## securite



`securite`

*   is optional

*   Type: `object` ([Sécurité du formulaire](frw-definitions-sécurité-du-formulaire.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-sécurité-du-formulaire.md "https://example.com/schemas/custom#/definitions/Config/properties/securite")

### securite Type

`object` ([Sécurité du formulaire](frw-definitions-sécurité-du-formulaire.md))

## soumission



`soumission`

*   is optional

*   Type: `object` ([Page de soumission](frw-definitions-page-de-soumission.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-page-de-soumission.md "https://example.com/schemas/custom#/definitions/Config/properties/soumission")

### soumission Type

`object` ([Page de soumission](frw-definitions-page-de-soumission.md))

## title

Multilingue

`title`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/Config/properties/title")

### title Type

`object` ([Translation](frw-definitions-translation.md))

### title Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
