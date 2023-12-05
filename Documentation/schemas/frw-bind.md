## Type de Fichier bind

`object` ([Fichier bind](frw-bind.md))

# Propriétés de Fichier bind

| Propriété               | Type     | Obligatoire | Nullable         | Défini par                                                                             |
| :---------------------- | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------- |
| [bundles](#bundles)     | `array`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bundles.md "schemas/bind#/properties/bundles")     |
| [config](#config)       | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-config.md "schemas/bind#/properties/config")       |
| [templates](#templates) | `array`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-templates.md "schemas/bind#/properties/templates") |
| [bind](#bind)           | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bind.md "schemas/bind#/properties/bind")           |

## bundles



`bundles`

*   est optionnel

*   ne peut être nul

### Type de bundles

`object[]` ([ListeBundle](frw-bind-definitions-listebundle.md))

## config



`config`

*   est optionnel

*   ne peut être nul

### Type de config

`object` ([config](frw-bind-definitions-config.md))

## templates



`templates`

*   est optionnel

*   ne peut être nul

### Type de templates

`object[]` ([ListeTemplate](frw-bind-definitions-listetemplate.md))

## bind

la section bind permet, en fonction des instructions de la configuration du formulaire, d’associer les bonnes valeurs du formulaire Web aux champs des gabarits PDF et d’appliquer un formatage si nécessaire.

`bind`

*   est optionnel

*   ne peut être nul

### Type de bind

`object` ([bind](frw-bind-definitions-bind.md))

# Définitions de Fichier bind

## Groupe de définitions Config

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Config"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                  |
| :------------------------ | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------- |
| [formulaire](#formulaire) | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-formulaire.md "schemas/bind#/definitions/Config/properties/formulaire") |
| [pdf](#pdf)               | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf.md "schemas/bind#/definitions/Config/properties/pdf")               |

### formulaire



`formulaire`

*   est optionnel

*   ne peut être nul

#### Type de formulaire

`object` ([formulaire](frw-bind-definitions-formulaire.md))

### pdf

La section 'pdf' permet de définir des options pour la production du fichier.

`pdf`

*   est optionnel

*   ne peut être nul

#### Type de pdf

`object` ([pdf](frw-bind-definitions-pdf.md))

## Groupe de définitions Formulaire

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Formulaire"}
```

| Propriété           | Type         | Obligatoire | Nullable         | Défini par                                                                                                                      |
| :------------------ | :----------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------ |
| [systeme](#systeme) | Non spécifié | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-formulaire-properties-systeme.md "schemas/bind#/definitions/Formulaire/properties/systeme") |
| [type](#type)       | Non spécifié | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-formulaire-properties-type.md "schemas/bind#/definitions/Formulaire/properties/type")       |

### systeme

Le système doit être l'identifiant de système autorisé que vous aurez obtenu de l'équipe FRW.

`systeme`

*   est optionnel

*   ne peut être nul

#### Type de systeme

inconnu ([systeme](frw-bind-definitions-formulaire-properties-systeme.md))

### type

Le type doit être le même nom que le répertoire de votre formulaire

`type`

*   est optionnel

*   ne peut être nul

#### Type de type

inconnu ([type](frw-bind-definitions-formulaire-properties-type.md))

## Groupe de définitions Pdf

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Pdf"}
```

| Propriété                                                     | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                                  |
| :------------------------------------------------------------ | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [rapetisserTexteTropLong](#rapetissertextetroplong)           | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-rapetissertextetroplong.md "schemas/bind#/definitions/Pdf/properties/rapetisserTexteTropLong")           |
| [redirigerAnnexeTexteTroplong](#redirigerannexetextetroplong) | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-redirigerannexetextetroplong.md "schemas/bind#/definitions/Pdf/properties/redirigerAnnexeTexteTroplong") |
| [pourcentageDepassementAnnexe](#pourcentagedepassementannexe) | `number`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-pourcentagedepassementannexe.md "schemas/bind#/definitions/Pdf/properties/pourcentageDepassementAnnexe") |
| [verrouillerChampsPdf](#verrouillerchampspdf)                 | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-pdf-properties-verrouillerchampspdf.md "schemas/bind#/definitions/Pdf/properties/verrouillerChampsPdf")                 |

### rapetisserTexteTropLong

rapetisserTexteTropLong permet de réduire automatiquement la taille de la police d'un texte qui dépasse légèrement la longueur du champ dans le gabarit PDF.

`rapetisserTexteTropLong`

*   est optionnel

*   ne peut être nul

#### Type de rapetisserTexteTropLong

`boolean` ([rapetisserTexteTropLong](frw-bind-definitions-pdf-properties-rapetissertextetroplong.md))

### redirigerAnnexeTexteTroplong

redirigerAnnexeTexteTopLong permet de créer une page d'annexe après la dernière page du formulaire pour y afficher les champs qui dépassent la longueur permise dans le gabarit.

`redirigerAnnexeTexteTroplong`

*   est optionnel

*   ne peut être nul

#### Type de redirigerAnnexeTexteTroplong

`boolean` ([redirigerAnnexeTexteTroplong](frw-bind-definitions-pdf-properties-redirigerannexetextetroplong.md))

### pourcentageDepassementAnnexe

pourcentageDepassementAnnexe permet de spécifier une limite avant de créer l'annexe des textes trop longs. En dessous de la limite, on rapetisse la police et au dessus, on créé l'annexe.

`pourcentageDepassementAnnexe`

*   est optionnel

*   ne peut être nul

#### Type de pourcentageDepassementAnnexe

`number` ([pourcentageDepassementAnnexe](frw-bind-definitions-pdf-properties-pourcentagedepassementannexe.md))

### verrouillerChampsPdf

verouillerChampsPdf permet de verouiller le fichier lorsque le traitement a terminé d'insérer les valeurs.

`verrouillerChampsPdf`

*   est optionnel

*   ne peut être nul

#### Type de verrouillerChampsPdf

`boolean` ([verrouillerChampsPdf](frw-bind-definitions-pdf-properties-verrouillerchampspdf.md))

## Groupe de définitions Bundles

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Bundles"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions ListeBundle

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/ListeBundle"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Bundle

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Bundle"}
```

| Propriété                     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                        |
| :---------------------------- | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------- |
| [nomSortie](#nomsortie)       | `string` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bundle-properties-nomsortie.md "schemas/bind#/definitions/Bundle/properties/nomSortie")       |
| [conditionsEt](#conditionset) | `string` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bundle-properties-conditionset.md "schemas/bind#/definitions/Bundle/properties/conditionsEt") |
| [templates](#templates-1)     | `array`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-bundle-properties-templates.md "schemas/bind#/definitions/Bundle/properties/templates")       |
| [estampille](#estampille)     | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille.md "schemas/bind#/definitions/Bundle/properties/estampille")                       |
| Propriétés Additionnelles     | Any      | Optionnel   | can be null      |                                                                                                                                   |

### nomSortie

Le nomSortie sert à définir le nom du fichier qui sera produit.

`nomSortie`

*   est optionnel

*   ne peut être nul

#### Type de nomSortie

`string` ([nomSortie](frw-bind-definitions-bundle-properties-nomsortie.md))

### conditionsEt

si la condition est true, retourne la valeur après le ':' sinon (la condition est false), ne retourne rien; lorsqu'il n'y a rien, il n'y a pas de condition à respecter, donc le bloc s'exécute

`conditionsEt`

*   est optionnel

*   ne peut être nul

#### Type de conditionsEt

`string` ([conditionsEt](frw-bind-definitions-bundle-properties-conditionset.md))

#### Exemple de conditionsEt

```yaml
'''{TypeDemande:neContientPas(Afdr):false}'''

```

### templates



`templates`

*   est optionnel

*   ne peut être nul

#### Type de templates

`string[]`

### estampille



`estampille`

*   est optionnel

*   ne peut être nul

#### Type de estampille

`object` ([estampille](frw-bind-definitions-estampille.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Estampille

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Estampille"}
```

| Propriété               | Type      | Obligatoire | Nullable         | Défini par                                                                                                                          |
| :---------------------- | :-------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------- |
| [positionX](#positionx) | `integer` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille-properties-positionx.md "schemas/bind#/definitions/Estampille/properties/positionX") |
| [positionY](#positiony) | `integer` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille-properties-positiony.md "schemas/bind#/definitions/Estampille/properties/positionY") |
| [lignes](#lignes)       | `array`   | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-estampille-properties-lignes.md "schemas/bind#/definitions/Estampille/properties/lignes")       |

### positionX



`positionX`

*   est optionnel

*   ne peut être nul

#### Type de positionX

`integer` ([positionX](frw-bind-definitions-estampille-properties-positionx.md))

### positionY



`positionY`

*   est optionnel

*   ne peut être nul

#### Type de positionY

`integer` ([positionY](frw-bind-definitions-estampille-properties-positiony.md))

### lignes



`lignes`

*   est optionnel

*   ne peut être nul

#### Type de lignes

`string[]`

#### Exemple de lignes

```yaml
'- ''Numéro de référence : {{NoConfirmation}}'''

```

```yaml
>-
  - 'Date de transmission : {{FormatterDate DateTransmission "yyyy-MM-dd
  HH:mm:ss"}}'

```

## Groupe de définitions Templates

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Templates"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions ListeTemplate

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/ListeTemplate"}
```

| Propriété                 | Type | Obligatoire | Nullable    | Défini par |
| :------------------------ | :--- | :---------- | :---------- | :--------- |
| Propriétés Additionnelles | Any  | Optionnel   | can be null |            |

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Template

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Template"}
```

| Propriété                             | Type      | Obligatoire | Nullable         | Défini par                                                                                                                                    |
| :------------------------------------ | :-------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| [id](#id)                             | `string`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-template-properties-id.md "schemas/bind#/definitions/Template/properties/id")                             |
| [name](#name)                         | `string`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-template-properties-name.md "schemas/bind#/definitions/Template/properties/name")                         |
| [gabarit](#gabarit)                   | `object`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-translation.md "schemas/bind#/definitions/Template/properties/gabarit")                                   |
| [pdf](#pdf-1)                         | `object`  | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-translation.md "schemas/bind#/definitions/Template/properties/pdf")                                       |
| [toujoursProduire](#toujoursproduire) | `boolean` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-template-properties-toujoursproduire.md "schemas/bind#/definitions/Template/properties/toujoursProduire") |
| Propriétés Additionnelles             | Any       | Optionnel   | can be null      |                                                                                                                                               |

### id



`id`

*   est optionnel

*   ne peut être nul

#### Type de id

`string` ([id](frw-bind-definitions-template-properties-id.md))

### name



`name`

*   est optionnel

*   ne peut être nul

#### Type de name

`string` ([name](frw-bind-definitions-template-properties-name.md))

### gabarit



`gabarit`

*   est optionnel

*   ne peut être nul

#### Type de gabarit

`object` ([translation](frw-bind-definitions-translation.md))

### pdf



`pdf`

*   est optionnel

*   ne peut être nul

#### Type de pdf

`object` ([translation](frw-bind-definitions-translation.md))

### toujoursProduire

La propriété 'toujoursProduire' s'applique aux gabarits informationnels seulement et sert à forcer le traitement à produire le document même s'il n'y a aucun champs du formulaire qui y sont associés.

`toujoursProduire`

*   est optionnel

*   ne peut être nul

#### Type de toujoursProduire

`boolean` ([toujoursProduire](frw-bind-definitions-template-properties-toujoursproduire.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions Translation

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Translation"}
```

| Propriété | Type     | Obligatoire | Nullable         | Défini par                                                                                                              |
| :-------- | :------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------- |
| [fr](#fr) | `string` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-translation-properties-fr.md "schemas/bind#/definitions/Translation/properties/fr") |
| [en](#en) | `string` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-translation-properties-en.md "schemas/bind#/definitions/Translation/properties/en") |

### fr



`fr`

*   est optionnel

*   ne peut être nul

#### Type de fr

`string` ([fr](frw-bind-definitions-translation-properties-fr.md))

### en



`en`

*   est optionnel

*   ne peut être nul

#### Type de en

`string` ([en](frw-bind-definitions-translation-properties-en.md))

## Groupe de définitions Bind

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/Bind"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                   |
| :------------------------ | :------- | :---------- | :--------------- | :--------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$`          | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-valeurelementbind.md "schemas/bind#/definitions/Bind/patternProperties/^\[a-zA-Z0-9]+$") |
| Propriétés Additionnelles | Any      | Optionnel   | can be null      |                                                                                                                              |

### Modèle:`^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([ValeurElementBind](frw-bind-definitions-valeurelementbind.md))

#### Contraintes de ^\[a-zA-Z0-9]+$

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions ValeurElementBind

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/ValeurElementBind"}
```

| Propriété                 | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                    |
| :------------------------ | :------- | :---------- | :--------------- | :-------------------------------------------------------------------------------------------------------------------------------------------- |
| `^[a-zA-Z0-9]+$`          | `object` | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-valeurelementtemplate.md "schemas/bind#/definitions/ValeurElementBind/patternProperties/^\[a-zA-Z0-9]+$") |
| Propriétés Additionnelles | Any      | Optionnel   | can be null      |                                                                                                                                               |

### Modèle:`^[a-zA-Z0-9]+$`



`^[a-zA-Z0-9]+$`

*   est optionnel

*   ne peut être nul

#### Type de ^\[a-zA-Z0-9]+$

`object` ([ValeurElementTemplate](frw-bind-definitions-valeurelementtemplate.md))

#### Contraintes de ^\[a-zA-Z0-9]+$

**nombre minimum de propriétés**: le nombre minimum de propriétés pour cet objet est :`1`

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique

## Groupe de définitions ValeurElementTemplate

Référencer ce groupe en utilisant

```json
{"$ref":"schemas/bind#/definitions/ValeurElementTemplate"}
```

| Propriété                 | Type         | Obligatoire | Nullable         | Défini par                                                                                                                                            |
| :------------------------ | :----------- | :---------- | :--------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| [champs](#champs)         | Non spécifié | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-valeurelementtemplate-properties-champs.md "schemas/bind#/definitions/ValeurElementTemplate/properties/champs")   |
| [formule](#formule)       | Non spécifié | Optionnel   | ne peut être nul | [Fichier bind](frw-bind-definitions-valeurelementtemplate-properties-formule.md "schemas/bind#/definitions/ValeurElementTemplate/properties/formule") |
| Propriétés Additionnelles | Any          | Optionnel   | can be null      |                                                                                                                                                       |

### champs



`champs`

*   est optionnel

*   ne peut être nul

#### Type de champs

inconnu ([champs](frw-bind-definitions-valeurelementtemplate-properties-champs.md))

### formule



`formule`

*   est optionnel

*   ne peut être nul

#### Type de formule

inconnu ([formule](frw-bind-definitions-valeurelementtemplate-properties-formule.md))

### Propriétés Additionnelles

D’autres propriétés sont autorisées et n’ont pas à suivre un schéma spécifique
