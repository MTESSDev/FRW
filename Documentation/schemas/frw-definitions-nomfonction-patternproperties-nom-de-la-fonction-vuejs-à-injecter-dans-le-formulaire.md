# Schéma de Nom de la fonction Vue.js à injecter dans le formulaire

```txt
https://example.com/schemas/custom#/definitions/NomFonction/patternProperties/^[a-zA-Z0-9]+$
```



| Abstrait            | Extensible | Statut         | Identifiable | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Non          | Interdit                  | Interdit                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de ^\[a-zA-Z0-9]+$

`object` ([Nom de la fonction Vue.js à injecter dans le formulaire](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire.md))

# Propriétés de ^\[a-zA-Z0-9]+$

| Propriété     | Type     | Obligatoire | Nullable         | Défini par                                                                                                                                                                                                                                                                |
| :------------ | :------- | :---------- | :--------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [code](#code) | `string` | Obligatoire | ne peut être nul | [Schéma sans nom](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire-properties-code-de-la-fonction.md "https://example.com/schemas/custom#/definitions/NomFonction/patternProperties/^\[a-zA-Z0-9]+$/properties/code") |

## code

Doit respecter le format fourni dans l'exemple. Votre code va entre les accolades.

`code`

*   est requis

*   ne peut être nul

### Type de code

`string` ([Code de la fonction](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire-properties-code-de-la-fonction.md))

### Exemple de code

```yaml
(){return 'bonjour!'}

```
