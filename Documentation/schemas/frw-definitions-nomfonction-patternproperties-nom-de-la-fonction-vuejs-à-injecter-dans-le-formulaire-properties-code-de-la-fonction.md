# Schéma de Code de la fonction

```txt
https://example.com/schemas/custom#/definitions/NomFonction/patternProperties/^[a-zA-Z0-9]+$/properties/code
```

Doit respecter le format fourni dans l'exemple. Votre code va entre les accolades.

| Abstrait            | Extensible | Statut         | Identifiable             | Propriétés personnalisées | Propriétés Additionnelles | Limites d'accès | Défini dans                                                                        |
| :------------------ | :--------- | :------------- | :----------------------- | :------------------------ | :------------------------ | :-------------- | :--------------------------------------------------------------------------------- |
| Peut être instancié | Non        | Unknown status | Identifiabilité inconnue | Interdit                  | Autorisé                  | aucun           | [FRW.form.schema.json\*](../out/FRW.form.schema.json "ouvrir le schéma d'origine") |

## Type de code

`string` ([Code de la fonction](frw-definitions-nomfonction-patternproperties-nom-de-la-fonction-vuejs-à-injecter-dans-le-formulaire-properties-code-de-la-fonction.md))

## Exemple de code

```yaml
(){return 'bonjour!'}

```
