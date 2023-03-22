# courrielReprise Schema

```txt
https://example.com/schemas/custom#/definitions/CourrielReprise
```

Paramètres associés au courriel de reprise.

| Abstract            | Extensible | Status         | Identifiable | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                   |
| :------------------ | :--------- | :------------- | :----------- | :---------------- | :-------------------- | :------------------ | :--------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | No           | Forbidden         | Forbidden             | none                | [FRW.form.schema.json\*](../out/FRW.form.schema.json "open original schema") |

## CourrielReprise Type

`object` ([courrielReprise](frw-definitions-courrielreprise.md))

# CourrielReprise Properties

| Property                                  | Type     | Required | Nullable       | Defined by                                                                                                                                                                          |
| :---------------------------------------- | :------- | :------- | :------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [courrielExpediteur](#courrielexpediteur) | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/courrielExpediteur") |
| [nomExpediteur](#nomexpediteur)           | `string` | Optional | cannot be null | [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/nomExpediteur")    |
| [objet](#objet)                           | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/objet")                                                |
| [corps](#corps)                           | `object` | Optional | cannot be null | [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/corps")                                                |

## courrielExpediteur

Adresse courriel expéditeur.

`courrielExpediteur`

*   is optional

*   Type: `string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/courrielExpediteur")

### courrielExpediteur Type

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur.md))

### courrielExpediteur Examples

```json
"NEPASREPONDRE@mtess.gouv.qc.ca"
```

## nomExpediteur

Nom de l'expéditeur expéditeur.

`nomExpediteur`

*   is optional

*   Type: `string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/nomExpediteur")

### nomExpediteur Type

`string` ([courrielExpediteur](frw-definitions-courrielreprise-properties-courrielexpediteur-1.md))

### nomExpediteur Examples

```json
"Formulaires en ligne - MESS"
```

## objet

Multilingue

`objet`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/objet")

### objet Type

`object` ([Translation](frw-definitions-translation.md))

### objet Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```

### objet Examples

```json
"Formulaire  « {0} » incomplet"
```

## corps

Multilingue

`corps`

*   is optional

*   Type: `object` ([Translation](frw-definitions-translation.md))

*   cannot be null

*   defined in: [Untitled schema](frw-definitions-translation.md "https://example.com/schemas/custom#/definitions/CourrielReprise/properties/corps")

### corps Type

`object` ([Translation](frw-definitions-translation.md))

### corps Default Value

The default value is:

```json
{
  "fr": "",
  "en": ""
}
```
