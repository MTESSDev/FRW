## Type de Content

`object` ([content](frw-transmission-definitions-content.md))

# Propriétés de Content

| Propriété                          | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :--------------------------------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [json\_content](#json_content)     | `string` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-content-properties-json_content.md "schemas/transmission#/definitions/Content/properties/json_content") |
| [check\_response](#check_response) | `object` | Optionnel   | ne peut être nul | [Fichier transmission](frw-transmission-definitions-check_response.md "schemas/transmission#/definitions/Content/properties/check_response")                |
| Propriétés Additionnelles          | Any      | Optionnel   | can be null      |                                                                                                                                                             |

## json\_content

Ici le json\_content que nous allons passés à votre API, vous êtes libres de mettre la structure que vous voulez, {{{Json .}}} permet de tout 'dumper' les variables de l'application vers votre API (voir Variables ci-dessous), utile aussi pour connaître les variables/objets disponibles

`json_content`

*   est optionnel

*   ne peut être nul

### Type de json\_content

`string` ([json\_content](frw-transmission-definitions-content-properties-json_content.md))

## check\_response

Utile pour valider que l'appel s'est bien terminé en 200 avec une validation du retour de contenu de votre API en prime

`check_response`

*   est optionnel

*   ne peut être nul

### Type de check\_response

`object` ([check\_response](frw-transmission-definitions-check_response.md))

## Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
