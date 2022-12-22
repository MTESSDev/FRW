# FRW - API
Définition de l'API publique pour intéragir avec FRW.

## Version: 1

### /api/v1/SIS/CreerFormulaireIndividu/{typeFormulaire}

#### POST
##### Summary

FRW111 - Créer un formulaire Web pour un individu.
> Permet de créer un formulaire pour un individu connu par le système autorisé.

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

FRW112 - Obtenir la liste des formulaires Web d'un individu
> Permet d'obtenir tous les formulaires d'un individu selon les états passés en paramètres.

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
> Permet de reprendre un formulaire pour un utilisateur le demandant

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| noFormulairePublic | path | Identifiant du formulaire pour lequel créer une session | Yes | string |
| X-ApiKey | header | Clé Api | Yes | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | Yes | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur pour lequel on demande une session | No | string |
| body | body | Contenu à remplacer dans le formulaire à reprendre (Ne permet que de remplacer un contexte ou un objet perso. ne remplace pas le contenu d'un formulaire.) | No | [EntrantObtenirIdentifiantSessionFormulaire](#entrantobteniridentifiantsessionformulaire) |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | Success | [RetourCreerReprendreFormulaireIndividu](#retourcreerreprendreformulaireindividu) |

### /api/v1/SIS/SupprimerFormulaire/{noFormulairePublic}

#### GET
##### Summary

FRW114 - Supprimer un formulaire web
> Permet de supprimer un formulaire demandé

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

### Models

#### EntrantCreerFormulaireIndividu

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| form | object | Le contenu du formulaire (pour pré-remplissage) | No |

#### EntrantRechercherFormulairesSIS

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| etatsFormulaireRecherche | [ string ] | Liste des états à obtenir<br>_Example:_ `["CRE","REP","MAJ","TRANSMIS"]` | No |
| codeTypeFormulaire | string | Code du formualaire ex. `3003` - NON IMPLÉMENTÉ POUR LE MOMENT | No |
| noConfirmation | integer | Numéro confirmant la transmission donné à l'utilisateur - NON IMPLÉMENTÉ POUR LE MOMENT<br>_Example:_ `12345311` | No |
| noPublicFormulaire | string | Identifiant unique du formulaire - NON IMPLÉMENTÉ POUR LE MOMENT | No |

#### EntrantObtenirIdentifiantSessionFormulaire

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| EntrantObtenirIdentifiantSessionFormulaire | object |  |  |

#### RetourCreerReprendreFormulaireIndividu

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| noPublicSession | string | Identifiant de session unique, utilisable une seule fois | No |
| noPublicForm | string | Identifiant unique du formulaire | No |

#### RetourRechercherFormulaires

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| typeFormulaire | string | Nom du répertoire déployé (nom du formulaire dans l'URL)<br>_Example:_ `3003` | No |
| noPublicForm | string | Identifiant unique du formulaire | No |
| identifiantUtilisateur | string | Identifiant de l'utilisateur à qui appartient le formulaire | No |
| titreFrancais | string | Titre français du formulaire extrait de la configuation | No |
| titreAnglais | string | Titre anglais du formulaire extrait de la configuation | No |
| dateCreation | dateTime | Date de création du formulaire | No |
| dernierEtat | string | Dernier état<br>_Example:_ `"MAJ"` | No |
| dateDernierEtat | dateTime | Date de la dernière modification ou ouverture du formulaire | No |
