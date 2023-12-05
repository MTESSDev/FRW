## Type de Estampille

`object` ([estampille](frw-bind-definitions-estampille.md))

# Propriétés de Estampille

| Propriété               | Type      | Obligatoire | Nullable         | Défini par                                                                                                                          |
| :---------------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------- |
| [positionX](#positionx) | `integer` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille-properties-positionx.md "schemas/bind#/definitions/Estampille/properties/positionX") |
| [positionY](#positiony) | `integer` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille-properties-positiony.md "schemas/bind#/definitions/Estampille/properties/positionY") |
| [lignes](#lignes)       | `array`   | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille-properties-lignes.md "schemas/bind#/definitions/Estampille/properties/lignes")       |

## positionX



`positionX`

*   est optionnel

*   ne peut être nul

### Type de positionX

`integer` ([positionX](frw-bind-definitions-estampille-properties-positionx.md))

## positionY



`positionY`

*   est optionnel

*   ne peut être nul

### Type de positionY

`integer` ([positionY](frw-bind-definitions-estampille-properties-positiony.md))

## lignes



`lignes`

*   est optionnel

*   ne peut être nul

### Type de lignes

`string[]`

### Exemple de lignes

```yaml
'- ''Numéro de référence : {{NoConfirmation}}'''

```

```yaml
>-
  - 'Date de transmission : {{FormatterDate DateTransmission "yyyy-MM-dd
  HH:mm:ss"}}'

```
