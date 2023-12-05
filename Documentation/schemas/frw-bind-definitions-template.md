## Type de Template

`object` ([template](frw-bind-definitions-template.md))

# Propriétés de Template

| Propriété                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                    |
| :------------------------------------ | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                             | `string`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-template-properties-id.md "schemas/bind#/definitions/Template/properties/id")                             |
| [name](#name)                         | `string`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-template-properties-name.md "schemas/bind#/definitions/Template/properties/name")                         |
| [gabarit](#gabarit)                   | `object`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-translation.md "schemas/bind#/definitions/Template/properties/gabarit")                                   |
| [pdf](#pdf)                           | `object`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-translation.md "schemas/bind#/definitions/Template/properties/pdf")                                       |
| [toujoursProduire](#toujoursproduire) | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-template-properties-toujoursproduire.md "schemas/bind#/definitions/Template/properties/toujoursProduire") |
| Propriétés Additionnelles             | Any       | Optionnel   | can be null      |                                                                                                                                               |

## id



`id`

*   est optionnel

*   ne peut être nul

### Type de id

`string` ([id](frw-bind-definitions-template-properties-id.md))

## name



`name`

*   est optionnel

*   ne peut être nul

### Type de name

`string` ([name](frw-bind-definitions-template-properties-name.md))

## gabarit



`gabarit`

*   est optionnel

*   ne peut être nul

### Type de gabarit

`object` ([translation](frw-bind-definitions-translation.md))

## pdf



`pdf`

*   est optionnel

*   ne peut être nul

### Type de pdf

`object` ([translation](frw-bind-definitions-translation.md))

## toujoursProduire

La propriété 'toujoursProduire' s'applique aux gabarits informationnels seulement et sert à forcer le traitement à produire le document même s'il n'y a aucun champs du formulaire qui y sont associés.

`toujoursProduire`

*   est optionnel

*   ne peut être nul

### Type de toujoursProduire

`boolean` ([toujoursProduire](frw-bind-definitions-template-properties-toujoursproduire.md))

## Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
