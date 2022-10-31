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
| X-NoPublicSystemeAutorise | header | Guid publique de système autorisé | Yes | string |
| X-ApiKey | header | Clée API | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Success |
| 401 | Unauthorized |

### /api/v1/SIS/CreerFormulaireIndividu/{typeFormulaire}

#### POST
##### Summary

FRW111 - Créer un formulaire Web pour un individu.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| typeFormulaire | path | _Example:_ `"3003"` | Yes | string |
| X-ApiKey | header | Clé Api | Yes | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | Yes | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur pour lequel le formulaire est créé | No | string |
| body | body |  | No | [EntrantCreerFormulaireIndividu](#entrantcreerformulaireindividu) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [RetourCreerReprendreFormulaireIndividu](#retourcreerreprendreformulaireindividu) |

### /api/v1/SIS/ObtenirFormulairesIndividu

#### POST
##### Summary

FRW112 - Obtenir les formulaire web d'un individu

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| X-ApiKey | header | Clé Api | Yes | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | Yes | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur pour lequel obtenir les formulaires | No | string |
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
| noFormulairePublic | path | Identifiant du formulaire pour lequel créer une session | Yes | string |
| X-ApiKey | header | Clé Api | Yes | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | Yes | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur pour lequel on demande une session | No | string |

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
| noFormulairePublic | path | Identifiant du formulaire à supprimer | Yes | string |
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
| X-ApiKey | header | Clé Api | Yes | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | Yes | string |
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
| etatsFormulaireRecherche | [ string ] | Liste des états à obtenir<br>_Example:_ `["foo","bar","baz"]` | No |
| codeTypeFormulaire | string | Code du formualaire ex. `3003` | No |
| noConfirmation | integer |  | No |
| noPublicFormulaire | string |  | No |

#### RetourCreerReprendreFormulaireIndividu

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| noPublicSession | string |  | No |
| noPublicForm | string |  | No |

#### RetourRechercherFormulaires

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| typeFormulaire | string | _Example:_ `3003` | No |
| noPublicForm | string | Identifiant unique du formulaire | No |
| identifiantUtilisateur | string | Identifiant de l'utilisateur à qui appartient le formulaire | No |
| titreFrancais | string | Titre français du formulaire extrait de la configuation | No |
| titreAnglais | string | Titre anglais du formulaire extrait de la configuation | No |
| dateCreation | dateTime | Date de création du formulaire | No |
| dernierEtat | string | Dernier état<br>_Example:_ `"MAJ"` | No |
| dateDernierEtat | dateTime | Date de la dernière modification ou ouverture du formulaire | No |
