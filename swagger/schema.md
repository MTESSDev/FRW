# FRW - API
Définition de l'API publique pour intéragir avec FRW.

### /api/v1/Document/Telecharger/{nomFichierProtege}

#### GET
##### Summary

FRW121 - Télécharger une pièce par nom de fichier protégé

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| nomFichierProtege | path | Nom fichier protégé (provient du contenu du formulaire) | Yes | string |
| X-NoPublicSystemeAutorise | header | Guid publique de système autorisé (facultative) | No | string |
| X-ApiKey | header | Clée API (facultative) | No | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success |  |
| 401 | Unauthorized | [ProblemDetails](#problemdetails) |

### /api/v1/SIS/CreerFormulaireIndividu/{typeFormulaire}

#### POST
##### Summary

FRW111 - Créer un formulaire Web pour un individu.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| typeFormulaire | path |  | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| body | body |  | No | [EntrantCreerFormulaireIndividu](#entrantcreerformulaireindividu) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [RetourCreerReprendreFormulaireIndividu](#retourcreerreprendreformulaireindividu) |

### /api/v1/SIS/ObtenirFormulairesIndividu

#### POST
##### Summary

FRW112 - obtenir les formulaire web d'un individu

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| body | body |  | No | [EntrantRechercherFormulairesSIS](#entrantrechercherformulairessis) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [ [RetourRechercherFormulaires](#retourrechercherformulaires) ] |

### /api/v1/SIS/ObtenirIdentifiantSessionFormulaire/{noFormulairePublic}

#### POST
##### Summary

FRW113 - Obtenir un identifiant de session pour un formulaire

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| noFormulairePublic | path |  | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| body | body |  | No |  |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [RetourCreerReprendreFormulaireIndividu](#retourcreerreprendreformulaireindividu) |

### /api/v1/SIS/SupprimerFormulaire/{noFormulairePublic}

#### GET
##### Summary

FRW114 - Supprimer un formulaire web

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| noFormulairePublic | path |  | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Success |

### /api/v1/SIS/DeployerSysteme

#### POST
##### Summary

FRWxxx - Déployer un système au complet

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| body | body |  | No | [EntrantDeployerSysteme](#entrantdeployersysteme) |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Success |

### Models

#### EntrantCreerFormulaireIndividu

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| form | object | Le contenu du formulaire (pour pré-remplissage) | No |
| ..AUTRES.. | object | N'importe quelles autres propriétés, vous pouvez choisir les noms à votre guise. | No |

#### EntrantDeployerSysteme

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| zip | byte |  | No |

#### EntrantRechercherFormulairesSIS

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| etatsFormulaireRecherche | [ string ] | `CRE`, `MAJ`, `TRANSMIS`, TODO à finir,   | No |
| codeTypeFormulaire | string | Code du formualaire ex. `3003` | No |
| noConfirmation | integer |  | No |
| noPublicFormulaire | string |  | No |

#### ProblemDetails

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| type | string |  | No |
| title | string |  | No |
| status | integer |  | No |
| detail | string |  | No |
| instance | string |  | No |

#### RetourCreerReprendreFormulaireIndividu

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| noPublicSession | string |  | No |
| noPublicForm | string |  | No |

#### RetourRechercherFormulaires

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| typeFormulaire | string |  | No |
| noPublicForm | string |  | No |
| identifiantUtilisateur | string |  | No |
| titreFrancais | string |  | No |
| titreAnglais | string |  | No |
| dateCreation | dateTime |  | No |
| dernierEtat | string |  | No |
| dateDernierEtat | dateTime |  | No |
