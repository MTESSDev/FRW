## Type de Scripts

`object` ([scripts](frw-definitions-scripts.md))

# Propriétés de Scripts

| Propriété                               | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                     |
| :-------------------------------------- | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- |
| [outilStatistiques](#outilstatistiques) | `string` | Optionnel   | ne peut être nul | [Fichier formulaire](frw-definitions-scripts-properties-outilstatistiques.md "schemas/form#/definitions/Scripts/properties/outilStatistiques") |

## outilStatistiques

Javascript servant à une solution d'outil statistiques (ex. Google Analytics ou Matomo). Injecté dans toutes les pages à la fin du body.

`outilStatistiques`

*   est optionnel

*   ne peut être nul

### Type de outilStatistiques

`string` ([outilStatistiques](frw-definitions-scripts-properties-outilstatistiques.md))

### Exemple de outilStatistiques

```yaml
<script> // Votre js ici... </script>

```
