## Type de ValeurElementClient

`object` ([Valeur de l'élément du client](frw-transmission-definitions-valeur-de-lélément-du-client.md))

# Propriétés de ValeurElementClient

| Propriété                  | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                               |
| :------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [method](#method)          | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-valeur-de-lélément-du-client-properties-method.md "schemas/transmission#/definitions/ValeurElementClient/properties/method")         |
| [url](#url)                | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-valeur-de-lélément-du-client-properties-url.md "schemas/transmission#/definitions/ValeurElementClient/properties/url")               |
| [headers](#headers)        | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-headers.md "schemas/transmission#/definitions/ValeurElementClient/properties/headers")                                               |
| [content](#content)        | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-content.md "schemas/transmission#/definitions/ValeurElementClient/properties/content")                                               |
| [auth\_basic](#auth_basic) | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-valeur-de-lélément-du-client-properties-auth_basic.md "schemas/transmission#/definitions/ValeurElementClient/properties/auth_basic") |
| Propriétés Additionnelles  | Any      | Optionnel   | can be null      |                                                                                                                                                                                          |

## method

Méthode d'appel de votre API, Peut-être POST, PUT, PATCH ou autre... normalement POST est le meilleur choix

`method`

*   est optionnel

*   ne peut être nul

### Type de method

`string` ([method](frw-transmission-definitions-valeur-de-lélément-du-client-properties-method.md))

### Contraintes de method

**énumération**: la valeur de cette propriété doit être égale à l'une des valeurs suivantes:

| Valeur     | Explication |
| :--------- | :---------- |
| `"POST"`   |             |
| `"PUT"`    |             |
| `"PATCH"`  |             |
| `"GET"`    |             |
| `"DELETE"` |             |

## url

Url de votre API, des paramètres en GET ici peuvent être passés, il est possible de mettre des variables aussi

`url`

*   est optionnel

*   ne peut être nul

### Type de url

`string` ([url](frw-transmission-definitions-valeur-de-lélément-du-client-properties-url.md))

## headers

Tous les headers que votre API doit reçevoir sont ici, possible aussi de mettre des variables

`headers`

*   est optionnel

*   ne peut être nul

### Type de headers

`object` ([headers](frw-transmission-definitions-headers.md))

## content



`content`

*   est optionnel

*   ne peut être nul

### Type de content

`object` ([content](frw-transmission-definitions-content.md))

## auth\_basic

HTTP Basic authentication

`auth_basic`

*   est optionnel

*   ne peut être nul

### Type de auth\_basic

`string` ([auth\_basic](frw-transmission-definitions-valeur-de-lélément-du-client-properties-auth_basic.md))

## Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
