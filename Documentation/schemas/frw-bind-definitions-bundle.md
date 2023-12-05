## Type de Bundle

`object` ([bundle](frw-bind-definitions-bundle.md))

# Propriétés de Bundle

| Propriété                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                        |
| :---------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| [nomSortie](#nomsortie)       | `string` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bundle-properties-nomsortie.md "schemas/bind#/definitions/Bundle/properties/nomSortie")       |
| [conditionsEt](#conditionset) | `string` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bundle-properties-conditionset.md "schemas/bind#/definitions/Bundle/properties/conditionsEt") |
| [templates](#templates)       | `array`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bundle-properties-templates.md "schemas/bind#/definitions/Bundle/properties/templates")       |
| [estampille](#estampille)     | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille.md "schemas/bind#/definitions/Bundle/properties/estampille")                       |
| Propriétés Additionnelles     | Any      | Optionnel   | can be null      |                                                                                                                                   |

## nomSortie

Le nomSortie sert à définir le nom du fichier qui sera produit.

`nomSortie`

*   est optionnel

*   ne peut être nul

### Type de nomSortie

`string` ([nomSortie](frw-bind-definitions-bundle-properties-nomsortie.md))

## conditionsEt

si la condition est true, retourne la valeur après le ':' sinon (la condition est false), ne retourne rien; lorsqu'il n'y a rien, il n'y a pas de condition à respecter, donc le bloc s'exécute

`conditionsEt`

*   est optionnel

*   ne peut être nul

### Type de conditionsEt

`string` ([conditionsEt](frw-bind-definitions-bundle-properties-conditionset.md))

### Exemple de conditionsEt

```yaml
'''{TypeDemande:neContientPas(Afdr):false}'''

```

## templates



`templates`

*   est optionnel

*   ne peut être nul

### Type de templates

`string[]`

## estampille



`estampille`

*   est optionnel

*   ne peut être nul

### Type de estampille

`object` ([estampille](frw-bind-definitions-estampille.md))

## Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
