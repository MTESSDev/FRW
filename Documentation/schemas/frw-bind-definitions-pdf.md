## Type de Pdf

`object` ([pdf](frw-bind-definitions-pdf.md))

# Propriétés de Pdf

| Propriété                                                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :------------------------------------------------------------ | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [rapetisserTexteTropLong](#rapetissertextetroplong)           | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-rapetissertextetroplong.md "schemas/bind#/definitions/Pdf/properties/rapetisserTexteTropLong")           |
| [redirigerAnnexeTexteTroplong](#redirigerannexetextetroplong) | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-redirigerannexetextetroplong.md "schemas/bind#/definitions/Pdf/properties/redirigerAnnexeTexteTroplong") |
| [pourcentageDepassementAnnexe](#pourcentagedepassementannexe) | `number`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-pourcentagedepassementannexe.md "schemas/bind#/definitions/Pdf/properties/pourcentageDepassementAnnexe") |
| [verrouillerChampsPdf](#verrouillerchampspdf)                 | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-verrouillerchampspdf.md "schemas/bind#/definitions/Pdf/properties/verrouillerChampsPdf")                 |

## rapetisserTexteTropLong

rapetisserTexteTropLong permet de réduire automatiquement la taille de la police d'un texte qui dépasse légèrement la longueur du champ dans le gabarit PDF.

`rapetisserTexteTropLong`

*   est optionnel

*   ne peut être nul

### Type de rapetisserTexteTropLong

`boolean` ([rapetisserTexteTropLong](frw-bind-definitions-pdf-properties-rapetissertextetroplong.md))

## redirigerAnnexeTexteTroplong

redirigerAnnexeTexteTopLong permet de créer une page d'annexe après la dernière page du formulaire pour y afficher les champs qui dépassent la longueur permise dans le gabarit.

`redirigerAnnexeTexteTroplong`

*   est optionnel

*   ne peut être nul

### Type de redirigerAnnexeTexteTroplong

`boolean` ([redirigerAnnexeTexteTroplong](frw-bind-definitions-pdf-properties-redirigerannexetextetroplong.md))

## pourcentageDepassementAnnexe

pourcentageDepassementAnnexe permet de spécifier une limite avant de créer l'annexe des textes trop longs. En dessous de la limite, on rapetisse la police et au dessus, on créé l'annexe.

`pourcentageDepassementAnnexe`

*   est optionnel

*   ne peut être nul

### Type de pourcentageDepassementAnnexe

`number` ([pourcentageDepassementAnnexe](frw-bind-definitions-pdf-properties-pourcentagedepassementannexe.md))

## verrouillerChampsPdf

verouillerChampsPdf permet de verouiller le fichier lorsque le traitement a terminé d'insérer les valeurs.

`verrouillerChampsPdf`

*   est optionnel

*   ne peut être nul

### Type de verrouillerChampsPdf

`boolean` ([verrouillerChampsPdf](frw-bind-definitions-pdf-properties-verrouillerchampspdf.md))
