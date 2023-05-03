# FRW - API
Définition de l'API publique pour intéragir avec FRW.

## Version: v1

**Contact information:**  
MESS - SFPS  

### Security
**ApiKey**  

| apiKey | *API Key* |
| ------ | --------- |
| Name | X-ApiKey |
| In | header |
| Description | Clée API secrète du système autorisé |

**NoPublicSystemeAutorise**  

| apiKey | *API Key* |
| ------ | --------- |
| Name | X-NoPublicSystemeAutorise |
| In | header |
| Description | Numéro public du système autorisé |

---
### /api/v1/Document/Telecharger/{nomFichierProtege}

#### GET
##### Summary

FRW121 - Télécharger une pièce par nom de fichier protégé

##### Description

Permet de récupérer une pièce jointe transmise par un citoyen

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ------ |
| nomFichierProtege | path | Nom fichier protégé (provient du contenu du formulaire) | Yes | string |
| bypassSecurite | query | Permet de ne pas valider la sécurité. | No | boolean |
| X-NoPublicSystemeAutorise | header | Guid publique de système autorisé | No | string |
| X-ApiKey | header | Clée API | No | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success |  |
| 401 | Unauthorized | [ProblemDetails](#problemdetails) |
| 404 | Fichier demandé introuvable | [ProblemDetails](#problemdetails) |
| 500 | Server Error |  |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| ApiKey |  |
| NoPublicSystemeAutorise |  |

---
### /api/v1/SIS/CreerFormulaireIndividu/{typeFormulaire}

#### POST
##### Summary

FRW111 - Créer un formulaire Web pour un individu.

##### Description

Permet de créer un formulaire pour un individu connu par le système autorisé.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ------ |
| typeFormulaire | path | *Exemple:* `3003` | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| body | body | Le contenu du formulaire (pour pré-remplissage) ex: `{"form": {"champ1": "val1"} }` | No |  |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [RetourCreerReprendreFormulaireIndividu](#retourcreerreprendreformulaireindividu) |
| 401 | Unauthorized | [ProblemDetails](#problemdetails) |
| 500 | Server Error |  |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| ApiKey |  |
| NoPublicSystemeAutorise |  |

### /api/v1/SIS/ObtenirFormulairesIndividu

#### POST
##### Summary

FRW112 - Obtenir la liste des formulaires Web d'un individu

##### Description

Permet d'obtenir tous les formulaires d'un individu selon les états passés en paramètres.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ------ |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| body | body | Objet de critères de recherche | No | [EntrantRechercherFormulairesSIS](#entrantrechercherformulairessis) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [ [RetourRechercherFormulaires](#retourrechercherformulaires) ] |
| 401 | Unauthorized | [ProblemDetails](#problemdetails) |
| 500 | Server Error |  |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| ApiKey |  |
| NoPublicSystemeAutorise |  |

### /api/v1/SIS/ObtenirIdentifiantSessionFormulaire/{noFormulairePublic}

#### POST
##### Summary

FRW113 - Obtenir un identifiant de session pour un formulaire

##### Description

Permet de reprendre un formulaire pour un utilisateur le demandant

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ------ |
| noFormulairePublic | path | Identifiant du formulaire pour lequel créer une session | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| body | body | Contenu à remplacer dans le formulaire à reprendre (Ne permet que de remplacer un contexte ou un objet perso. ne remplace pas le contenu d'un formulaire.) | No |  |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [RetourCreerReprendreFormulaireIndividu](#retourcreerreprendreformulaireindividu) |
| 401 | Unauthorized | [ProblemDetails](#problemdetails) |
| 500 | Server Error |  |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| ApiKey |  |
| NoPublicSystemeAutorise |  |

### /api/v1/SIS/SupprimerFormulaire/{noFormulairePublic}

#### GET
##### Summary

FRW114 - Supprimer un formulaire web

##### Description

Permet de supprimer un formulaire demandé

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ------ |
| noFormulairePublic | path | Identifiant du formulaire à supprimer | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success |  |
| 401 | Unauthorized | [ProblemDetails](#problemdetails) |
| 500 | Server Error |  |

##### Security

| Security Schema | Scopes |
| --------------- | ------ |
| ApiKey |  |
| NoPublicSystemeAutorise |  |

---
### Models

#### Adresse

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| rue | string |  | No |
| municipalite | string |  | No |
| municipaliteNomLong | string |  | No |
| codePostal | string |  | No |

#### EntrantDeconnexion

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| expiration | long |  | No |

#### EntrantDeployerSysteme

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| zip | byte |  | No |

#### EntrantRechercherFormulairesSIS

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| etatsFormulaireRecherche | [ string ] |  | No |
| codeTypeFormulaire | string |  | No |
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
| dateEpuration | dateTime |  | No |
| numeroConfirmation | integer |  | No |

#### StringStringValuesKeyValuePair

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| key | string |  | No |
| value | [ string ] |  | No |
