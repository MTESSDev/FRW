## Type de Fichier transmission

`object` ([Fichier transmission](frw-transmission.md))

# Propriétés de Fichier transmission

| Propriété                               | Type     | Obligatoire | Nullable         | Défini par                                                                                                                     |
| :-------------------------------------- | :------- | :---------- | :--------------- | :----------------------------------------------------------------------------------------------------------------------------- |
| [etapes](#etapes)                       | `array`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-etapes.md "schemas/transmission#/properties/etapes")                       |
| [http\_client](#http_client)            | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-http_client.md "schemas/transmission#/properties/http_client")             |
| [gabaritsCourriels](#gabaritscourriels) | `array`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-gabaritscourriels.md "schemas/transmission#/properties/gabaritsCourriels") |

## etapes

Liste des étapes désirées dans votre transmission. L'ordre est importante, le traitement la respectera

`etapes`

*   est optionnel

*   ne peut être nul

### Type de etapes

`object[]` ([tache](frw-transmission-definitions-tache.md))

## http\_client

La liste des clients http

`http_client`

*   est optionnel

*   ne peut être nul

### Type de http\_client

`object` ([http\_client](frw-transmission-definitions-http_client.md))

## gabaritsCourriels



`gabaritsCourriels`

*   est optionnel

*   ne peut être nul

### Type de gabaritsCourriels

`object[]` ([Détails](frw-transmission-definitions-itemsgabaritscourriels.md))

# Définitions de Fichier transmission

## Groupe de définitions Etapes

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Etapes"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions Taches

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Taches"}
```

| Propriété                           | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                     |
| :---------------------------------- | :-------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [tache](#tache)                     | `string`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-tache-properties-tache.md "schemas/transmission#/definitions/Taches/properties/tache")                     |
| [options](#options)                 | `object`  | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-options.md "schemas/transmission#/definitions/Taches/properties/options")                                  |
| [numeroExecution](#numeroexecution) | `integer` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-tache-properties-numeroexecution.md "schemas/transmission#/definitions/Taches/properties/numeroExecution") |

### tache



`tache`

*   est optionnel

*   ne peut être nul

#### Type de tache

`string` ([tache](frw-transmission-definitions-tache-properties-tache.md))

#### Contraintes de tache

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

### options



`options`

*   est optionnel

*   ne peut être nul

#### Type de options

`object` ([options](frw-transmission-definitions-options.md))

### numeroExecution



`numeroExecution`

*   est optionnel

*   ne peut être nul

#### Type de numeroExecution

`integer` ([numeroExecution](frw-transmission-definitions-tache-properties-numeroexecution.md))

## Groupe de définitions Options

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Options"}
```

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

### fichierBind



`fichierBind`

*   est optionnel

*   ne peut être nul

#### Type de fichierBind

`string` ([fichierBind](frw-transmission-definitions-options-properties-fichierbind.md))

### client



`client`

*   est optionnel

*   ne peut être nul

#### Type de client

`string` ([client](frw-transmission-definitions-options-properties-client.md))

### modeBoutonTesterTransmission



`modeBoutonTesterTransmission`

*   est optionnel

*   ne peut être nul

#### Type de modeBoutonTesterTransmission

`string` ([modeBoutonTesterTransmission](frw-transmission-definitions-options-properties-modeboutontestertransmission.md))

#### Contraintes de modeBoutonTesterTransmission

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur      | Explication |
| :---------- | :---------- |
| `"simuler"` |             |
| `"ignorer"` |             |
| `""`        |             |

### gabarit



`gabarit`

*   est optionnel

*   ne peut être nul

#### Type de gabarit

`string` ([gabarit](frw-transmission-definitions-options-properties-gabarit.md))

### filtresDocuments



`filtresDocuments`

*   est optionnel

*   ne peut être nul

#### Type de filtresDocuments

`object[]` ([Détails](frw-transmission-definitions-itemsfiltresdocuments.md))

### conditionsEt



`conditionsEt`

*   est optionnel

*   ne peut être nul

#### Type de conditionsEt

`object[]` ([Détails](frw-transmission-definitions-itemsconditions.md))

### conditionsOu



`conditionsOu`

*   est optionnel

*   ne peut être nul

#### Type de conditionsOu

`object[]` ([Détails](frw-transmission-definitions-itemsconditions.md))

### partiesVariables



`partiesVariables`

*   est optionnel

*   ne peut être nul

#### Type de partiesVariables

`object` ([partiesVariables](frw-transmission-definitions-options-properties-partiesvariables.md))

### desactiverEstampille



`desactiverEstampille`

*   est optionnel

*   ne peut être nul

#### Type de desactiverEstampille

`boolean` ([Désactiver estampille de pied de page](frw-transmission-definitions-options-properties-désactiver-estampille-de-pied-de-page.md))

## Groupe de définitions FiltresDocuments

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/FiltresDocuments"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions ItemsFiltresDocuments

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ItemsFiltresDocuments"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions ItemFiltreDocuments

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ItemFiltreDocuments"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                      |
| :------------------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [typeFiltre](#typefiltre) | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemfiltredocuments-properties-typefiltre.md "schemas/transmission#/definitions/ItemFiltreDocuments/properties/typeFiltre") |
| [valeurs](#valeurs)       | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemfiltredocuments-properties-valeurs.md "schemas/transmission#/definitions/ItemFiltreDocuments/properties/valeurs")       |

### typeFiltre



`typeFiltre`

*   est optionnel

*   ne peut être nul

#### Type de typeFiltre

`string` ([typeFiltre](frw-transmission-definitions-itemfiltredocuments-properties-typefiltre.md))

### valeurs



`valeurs`

*   est optionnel

*   ne peut être nul

#### Type de valeurs

`string` ([valeurs](frw-transmission-definitions-itemfiltredocuments-properties-valeurs.md))

## Groupe de définitions Conditions

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Conditions"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions ItemsConditions

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ItemsConditions"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions ItemConditions

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ItemConditions"}
```

| Propriété                           | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                      |
| :---------------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [condition](#condition)             | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemconditions-properties-condition.md "schemas/transmission#/definitions/ItemConditions/properties/condition")             |
| [champFormulaire](#champformulaire) | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemconditions-properties-champformulaire.md "schemas/transmission#/definitions/ItemConditions/properties/champFormulaire") |
| [valeur](#valeur)                   | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemconditions-properties-valeur.md "schemas/transmission#/definitions/ItemConditions/properties/valeur")                   |

### condition



`condition`

*   est optionnel

*   ne peut être nul

#### Type de condition

`string` ([condition](frw-transmission-definitions-itemconditions-properties-condition.md))

### champFormulaire



`champFormulaire`

*   est optionnel

*   ne peut être nul

#### Type de champFormulaire

`string` ([champFormulaire](frw-transmission-definitions-itemconditions-properties-champformulaire.md))

### valeur



`valeur`

*   est optionnel

*   ne peut être nul

#### Type de valeur

`string` ([valeur](frw-transmission-definitions-itemconditions-properties-valeur.md))

## Groupe de définitions Http\_client

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Http_client"}
```

| Propriété         | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                              |
| :---------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9_]+$` | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-valeur-de-lélément-du-client.md "schemas/transmission#/definitions/Http_client/patternProperties/^\[a-zA-Z0-9_]+$") |

### Modèle:`^[a-zA-Z0-9_]+$`

Nom de votre client, ici appel\_externe

`^[a-zA-Z0-9_]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9\_]+$

`object` ([Valeur de l'élément du client](frw-transmission-definitions-valeur-de-lélément-du-client.md))

#### Contraintes de ^\[a-zA-Z0-9\_]+$

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

## Groupe de définitions ValeurElementClient

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ValeurElementClient"}
```

| Propriété                  | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                               |
| :------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [method](#method)          | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-valeur-de-lélément-du-client-properties-method.md "schemas/transmission#/definitions/ValeurElementClient/properties/method")         |
| [url](#url)                | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-valeur-de-lélément-du-client-properties-url.md "schemas/transmission#/definitions/ValeurElementClient/properties/url")               |
| [headers](#headers)        | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-headers.md "schemas/transmission#/definitions/ValeurElementClient/properties/headers")                                               |
| [content](#content)        | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-content.md "schemas/transmission#/definitions/ValeurElementClient/properties/content")                                               |
| [auth\_basic](#auth_basic) | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-valeur-de-lélément-du-client-properties-auth_basic.md "schemas/transmission#/definitions/ValeurElementClient/properties/auth_basic") |
| Propriétés Additionnelles  | Any      | Optionnel   | can be null      |                                                                                                                                                                                          |

### method

Méthode d'appel de votre API, Peut-être POST, PUT, PATCH ou autre... normalement POST est le meilleur choix

`method`

*   est optionnel

*   ne peut être nul

#### Type de method

`string` ([method](frw-transmission-definitions-valeur-de-lélément-du-client-properties-method.md))

#### Contraintes de method

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur     | Explication |
| :--------- | :---------- |
| `"POST"`   |             |
| `"PUT"`    |             |
| `"PATCH"`  |             |
| `"GET"`    |             |
| `"DELETE"` |             |

### url

Url de votre API, des paramètres en GET ici peuvent être passés, il est possible de mettre des variables aussi

`url`

*   est optionnel

*   ne peut être nul

#### Type de url

`string` ([url](frw-transmission-definitions-valeur-de-lélément-du-client-properties-url.md))

### headers

Tous les headers que votre API doit reçevoir sont ici, possible aussi de mettre des variables

`headers`

*   est optionnel

*   ne peut être nul

#### Type de headers

`object` ([headers](frw-transmission-definitions-headers.md))

### content



`content`

*   est optionnel

*   ne peut être nul

#### Type de content

`object` ([content](frw-transmission-definitions-content.md))

### auth\_basic

HTTP Basic authentication

`auth_basic`

*   est optionnel

*   ne peut être nul

#### Type de auth\_basic

`string` ([auth\_basic](frw-transmission-definitions-valeur-de-lélément-du-client-properties-auth_basic.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Headers

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Headers"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                      |
| :------------------------ | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------- |
| [Accept](#accept)         | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-headers-properties-accept.md "schemas/transmission#/definitions/Headers/properties/Accept") |
| Propriétés Additionnelles | Any      | Optionnel   | can be null      |                                                                                                                                                 |

### Accept



`Accept`

*   est optionnel

*   ne peut être nul

#### Type de Accept

`string` ([Accept](frw-transmission-definitions-headers-properties-accept.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Content

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Content"}
```

| Propriété                          | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :--------------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [json\_content](#json_content)     | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-content-properties-json_content.md "schemas/transmission#/definitions/Content/properties/json_content") |
| [check\_response](#check_response) | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-check_response.md "schemas/transmission#/definitions/Content/properties/check_response")                |
| Propriétés Additionnelles          | Any      | Optionnel   | can be null      |                                                                                                                                                             |

### json\_content

Ici le json\_content que nous allons passés à votre API, vous êtes libres de mettre la structure que vous voulez, {{{Json .}}} permet de tout 'dumper' les variables de l'application vers votre API (voir Variables ci-dessous), utile aussi pour connaître les variables/objets disponibles

`json_content`

*   est optionnel

*   ne peut être nul

#### Type de json\_content

`string` ([json\_content](frw-transmission-definitions-content-properties-json_content.md))

### check\_response

Utile pour valider que l'appel s'est bien terminé en 200 avec une validation du retour de contenu de votre API en prime

`check_response`

*   est optionnel

*   ne peut être nul

#### Type de check\_response

`object` ([check\_response](frw-transmission-definitions-check_response.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Check\_response

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Check_response"}
```

| Propriété                                                                                   | Type    | Obligatoire | Nullable         | Défini par                                                                                                                                                                                              |
| :------------------------------------------------------------------------------------------ | :------ | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [throw\_exception\_if\_body\_not\_contains\_all](#throw_exception_if_body_not_contains_all) | `array` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-throw_exception_if_body_not_contains_all.md "schemas/transmission#/definitions/Check_response/properties/throw_exception_if_body_not_contains_all") |
| [throw\_exception\_if\_body\_contains\_any](#throw_exception_if_body_contains_any)          | `array` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-throw_exception_if_body_contains_any.md "schemas/transmission#/definitions/Check_response/properties/throw_exception_if_body_contains_any")         |

### throw\_exception\_if\_body\_not\_contains\_all



`throw_exception_if_body_not_contains_all`

*   est optionnel

*   ne peut être nul

#### Type de throw\_exception\_if\_body\_not\_contains\_all

`array` ([throw\_exception\_if\_body\_not\_contains\_all](frw-transmission-definitions-throw_exception_if_body_not_contains_all.md))

### throw\_exception\_if\_body\_contains\_any



`throw_exception_if_body_contains_any`

*   est optionnel

*   ne peut être nul

#### Type de throw\_exception\_if\_body\_contains\_any

`array` ([Throw\_exception\_if\_body\_contains\_any](frw-transmission-definitions-throw_exception_if_body_contains_any.md))

## Groupe de définitions Throw\_exception\_if\_body\_not\_contains\_all

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Throw_exception_if_body_not_contains_all"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Throw\_exception\_if\_body\_contains\_any

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/Throw_exception_if_body_contains_any"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions GabaritsCourriels

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/GabaritsCourriels"}
```

| Propriété | Type | Obligatoire | Nullable | Défini par |
| :-------- | :--- | :---------- | :------- | :--------- |

## Groupe de définitions ItemsGabaritsCourriels

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ItemsGabaritsCourriels"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions ItemGabaritsCourriels

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ItemGabaritsCourriels"}
```

| Propriété                       | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                |
| :------------------------------ | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                       | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemgabaritscourriels-properties-id.md "schemas/transmission#/definitions/ItemGabaritsCourriels/properties/id")                       |
| [a](#a)                         | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel.md "schemas/transmission#/definitions/ItemGabaritsCourriels/properties/a")                                         |
| [cc](#cc)                       | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel.md "schemas/transmission#/definitions/ItemGabaritsCourriels/properties/cc")                                        |
| [cci](#cci)                     | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel.md "schemas/transmission#/definitions/ItemGabaritsCourriels/properties/cci")                                       |
| [objet](#objet)                 | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemgabaritscourriels-properties-objet.md "schemas/transmission#/definitions/ItemGabaritsCourriels/properties/objet")                 |
| [corps](#corps)                 | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemgabaritscourriels-properties-corps.md "schemas/transmission#/definitions/ItemGabaritsCourriels/properties/corps")                 |
| [nomExpediteur](#nomexpediteur) | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-itemgabaritscourriels-properties-nomexpediteur.md "schemas/transmission#/definitions/ItemGabaritsCourriels/properties/nomExpediteur") |

### id



`id`

*   est optionnel

*   ne peut être nul

#### Type de id

`string` ([id](frw-transmission-definitions-itemgabaritscourriels-properties-id.md))

### a



`a`

*   est optionnel

*   ne peut être nul

#### Type de a

`object` ([Détails](frw-transmission-definitions-provenancecourriel.md))

### cc



`cc`

*   est optionnel

*   ne peut être nul

#### Type de cc

`object` ([Détails](frw-transmission-definitions-provenancecourriel.md))

### cci



`cci`

*   est optionnel

*   ne peut être nul

#### Type de cci

`object` ([Détails](frw-transmission-definitions-provenancecourriel.md))

### objet

l objet du courriel

`objet`

*   est optionnel

*   ne peut être nul

#### Type de objet

`string` ([objet](frw-transmission-definitions-itemgabaritscourriels-properties-objet.md))

### corps

le corps du message

`corps`

*   est optionnel

*   ne peut être nul

#### Type de corps

`string` ([corps](frw-transmission-definitions-itemgabaritscourriels-properties-corps.md))

### nomExpediteur



`nomExpediteur`

*   est optionnel

*   ne peut être nul

#### Type de nomExpediteur

`string`

## Groupe de définitions ProvenanceCourriel

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/transmission#/definitions/ProvenanceCourriel"}
```

| Propriété                   | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                      |
| :-------------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [unitaire](#unitaire)       | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel-properties-unitaire.md "schemas/transmission#/definitions/ProvenanceCourriel/properties/unitaire")       |
| [acceptation](#acceptation) | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel-properties-acceptation.md "schemas/transmission#/definitions/ProvenanceCourriel/properties/acceptation") |
| [techno](#techno)           | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel-properties-techno.md "schemas/transmission#/definitions/ProvenanceCourriel/properties/techno")           |
| [production](#production)   | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel-properties-production.md "schemas/transmission#/definitions/ProvenanceCourriel/properties/production")   |
| [tous](#tous)               | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-provenancecourriel-properties-tous.md "schemas/transmission#/definitions/ProvenanceCourriel/properties/tous")               |
| Propriétés Additionnelles   | Any      | Optionnel   | can be null      |                                                                                                                                                                                 |

### unitaire



`unitaire`

*   est optionnel

*   ne peut être nul

#### Type de unitaire

`string`

### acceptation



`acceptation`

*   est optionnel

*   ne peut être nul

#### Type de acceptation

`string`

### techno



`techno`

*   est optionnel

*   ne peut être nul

#### Type de techno

`string`

### production



`production`

*   est optionnel

*   ne peut être nul

#### Type de production

`string`

### tous



`tous`

*   est optionnel

*   ne peut être nul

#### Type de tous

`string`

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
