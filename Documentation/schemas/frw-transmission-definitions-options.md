## Type de Options

`object` ([options](frw-transmission-definitions-options.md))

# Propriétés de Options

| Propriété                                                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                                                   |
| :------------------------------------------------------------ | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [fichierBind](#fichierbind)                                   | `string`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options-properties-fichierbind.md "schemas/transmission#/definitions/Options/properties/fichierBind")                                    |
| [client](#client)                                             | `string`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options-properties-client.md "schemas/transmission#/definitions/Options/properties/client")                                              |
| [modeBoutonTesterTransmission](#modeboutontestertransmission) | `string`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options-properties-modeboutontestertransmission.md "schemas/transmission#/definitions/Options/properties/modeBoutonTesterTransmission")  |
| [gabarit](#gabarit)                                           | `string`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options-properties-gabarit.md "schemas/transmission#/definitions/Options/properties/gabarit")                                            |
| [filtresDocuments](#filtresdocuments)                         | `array`   | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-filtresdocuments.md "schemas/transmission#/definitions/Options/properties/filtresDocuments")                                             |
| [conditionsEt](#conditionset)                                 | `array`   | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-conditions.md "schemas/transmission#/definitions/Options/properties/conditionsEt")                                                       |
| [conditionsOu](#conditionsou)                                 | `array`   | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-conditions.md "schemas/transmission#/definitions/Options/properties/conditionsOu")                                                       |
| [partiesVariables](#partiesvariables)                         | `object`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options-properties-partiesvariables.md "schemas/transmission#/definitions/Options/properties/partiesVariables")                          |
| [desactiverEstampille](#desactiverestampille)                 | `boolean` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options-properties-désactiver-estampille-de-pied-de-page.md "schemas/transmission#/definitions/Options/properties/desactiverEstampille") |

## fichierBind



`fichierBind`

*   est optionnel

*   ne peut être nul

### Type de fichierBind

`string` ([fichierBind](frw-transmission-definitions-options-properties-fichierbind.md))

## client



`client`

*   est optionnel

*   ne peut être nul

### Type de client

`string` ([client](frw-transmission-definitions-options-properties-client.md))

## modeBoutonTesterTransmission



`modeBoutonTesterTransmission`

*   est optionnel

*   ne peut être nul

### Type de modeBoutonTesterTransmission

`string` ([modeBoutonTesterTransmission](frw-transmission-definitions-options-properties-modeboutontestertransmission.md))

### Contraintes de modeBoutonTesterTransmission

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur      | Explication |
| :---------- | :---------- |
| `"simuler"` |             |
| `"ignorer"` |             |
| `""`        |             |

## gabarit



`gabarit`

*   est optionnel

*   ne peut être nul

### Type de gabarit

`string` ([gabarit](frw-transmission-definitions-options-properties-gabarit.md))

## filtresDocuments



`filtresDocuments`

*   est optionnel

*   ne peut être nul

### Type de filtresDocuments

`object[]` ([Détails](frw-transmission-definitions-itemsfiltresdocuments.md))

## conditionsEt



`conditionsEt`

*   est optionnel

*   ne peut être nul

### Type de conditionsEt

`object[]` ([Détails](frw-transmission-definitions-itemsconditions.md))

## conditionsOu



`conditionsOu`

*   est optionnel

*   ne peut être nul

### Type de conditionsOu

`object[]` ([Détails](frw-transmission-definitions-itemsconditions.md))

## partiesVariables



`partiesVariables`

*   est optionnel

*   ne peut être nul

### Type de partiesVariables

`object` ([partiesVariables](frw-transmission-definitions-options-properties-partiesvariables.md))

## desactiverEstampille



`desactiverEstampille`

*   est optionnel

*   ne peut être nul

### Type de desactiverEstampille

`boolean` ([Désactiver estampille de pied de page](frw-transmission-definitions-options-properties-désactiver-estampille-de-pied-de-page.md))
