# FRW - API
Définition de l'API publique pour intéragir avec FRW.

## Version: v1

**Contact information:**  
MESS - SFPS  

### /api/v1/Conavigation/Creer/{shortInstance}

#### POST
##### Summary:

FRW241 - Générer un code de co-navigation

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| shortInstance | path |  | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 500 | Internal Server Error |

### /api/v1/Document/Telecharger/{nomFichierProtege}

#### GET
##### Summary:

FRW121 - Télécharger une pièce par nom de fichier protégé

##### Description:

Permet de récupérer une pièce jointe transmise par un citoyen

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| nomFichierProtege | path | Nom fichier protégé (provient du contenu du formulaire) | Yes | string |
| bypassSecurite | query | Permet de ne pas valider la sécurité. | No | boolean |
| X-NoPublicSystemeAutorise | header | Guid publique de système autorisé | No | string |
| X-ApiKey | header | Clée API | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 404 | Fichier demandé introuvable |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

null

### /api/v1/Document/Telecharger/{sessionUtilisateur}/{nomFichierProtege}

#### GET
##### Summary:

FRW121 - Télécharger une pièce avec session active

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| sessionUtilisateur | path | Session utilisateur (shortGuid) (provient de la barre adresse) | Yes | string |
| nomFichierProtege | path | Nom fichier protégé (provient du contenu du formulaire) | Yes | string |
| bypassSecurite | query | Permet de ne pas valider la sécurité. | No | boolean |
| onglet | query |  | No | boolean |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

### /api/v1/Document/Upload/{shortInstance}

#### POST
##### Summary:

FRW121 - Téléverser une pièce

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| shortInstance | path |  | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

### /api/v1/Document/Telecharger

#### GET
##### Summary:

FRW121 - Télécharger une pièce jointe

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| nomFichierOriginal | query | Nom original du fichier | No | string |
| nomFichierInterne | query | Nom interne du fichier | No | string |
| checksum | query | Checksum du nom interne du fichier | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 404 | Not Found |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

### /api/v1/Document/ObtenirPdfConfirmation/{sessionUtilisateur}

#### GET
##### Summary:

FRW328 - Récupérer le formulaire produit (PDF)

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| sessionUtilisateur | path |  | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 202 | Accepted |
| 204 | No Content |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 404 | Not Found |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

### /api/v1/InfosBancaires/ValiderInformationsBancaires

#### POST
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |

### /api/Log/Error

#### POST
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |

### /api/Log/Information

#### POST
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |

### /api/Paiement/ObtenirJetonMoneris/{idSystemeAutorise}/{typeFormulaire}/{version}/{shortInstance}

#### POST
##### Summary:

FRW341 - Obtenir un jeton pour le paiement

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idSystemeAutorise | path | Id du système autorisé | Yes | integer |
| typeFormulaire | path | Type du formulaire | Yes | string |
| version | path | Version | Yes | string |
| shortInstance | path | ShortInstance | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/v1/Recherche/ObtenirTexteForm/{version}/{shortInstance}

#### GET
##### Summary:

FRW218 - Obtenir le contenu pour la recherche

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| version | path | Version du formulaire | Yes | string |
| shortInstance | path | Numéro public de session (GUID) | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |

### /api/RIR/RechercherAdresse/{codePostal}/{noCivique}

#### GET
##### Summary:

FRW215 - Rechercher et obtenir une adresse postale normalisée

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| codePostal | path |  | Yes | string |
| noCivique | path |  | Yes | integer |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |

### /api/RIR/RechercherAdresseParCodePostal/{codePostal}

#### GET
##### Summary:

FRW215 - Rechercher et obtenir une adresse postale normalisée par code postal

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| codePostal | path |  | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |

### /api/v1/SIS/CreerFormulaireIndividu/{typeFormulaire}

#### POST
##### Summary:

FRW111 - Créer un formulaire Web pour un individu.

##### Description:

Permet de créer un formulaire pour un individu connu par le système autorisé.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| typeFormulaire | path | _Exemple:_ `3003` | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-NoPublicSystemeAutoriseDeleguant | header | Numéro public du système autorisé qui a délégué le contrôle sur son formulaire | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

null

### /api/v1/SIS/ObtenirFormulairesIndividu

#### POST
##### Summary:

FRW112 - Obtenir la liste des formulaires Web d'un individu

##### Description:

Permet d'obtenir tous les formulaires d'un individu selon les états passés en paramètres.

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-NoPublicSystemeAutoriseDeleguant | header | Numéro public du système autorisé qui a délégué le contrôle sur son formulaire | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

null

### /api/v1/SIS/ObtenirIdentifiantSessionFormulaire/{noFormulairePublic}

#### POST
##### Summary:

FRW113 - Obtenir un identifiant de session pour un formulaire

##### Description:

Permet de reprendre un formulaire pour un utilisateur le demandant

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| noFormulairePublic | path | Identifiant du formulaire pour lequel créer une session | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-NoPublicSystemeAutoriseDeleguant | header | Numéro public du système autorisé qui a délégué le contrôle sur son formulaire | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

null

### /api/v1/SIS/SupprimerFormulaire/{noFormulairePublic}

#### GET
##### Summary:

FRW114 - Supprimer un formulaire web

##### Description:

Permet de supprimer un formulaire demandé

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| noFormulairePublic | path | Identifiant du formulaire à supprimer | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-NoPublicSystemeAutoriseDeleguant | header | Numéro public du système autorisé qui a délégué le contrôle sur son formulaire | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

null

### /api/v1/SIS/CreerFormulaireRepriseDifferee/{typeFormulaire}

#### POST
##### Summary:

FRW117 - Créer un formulaire pour reprise en différée

##### Description:



##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| typeFormulaire | path | _Exemple:_ `3003` | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-NoPublicSystemeAutoriseDeleguant | header | Numéro public du système autorisé qui a délégué le contrôle sur son formulaire | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

null

### /api/v1/SIS/ObtenirSchema/{type}

#### GET
##### Summary:

Obtenir un schema

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| type | path |  | Yes | string |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-NoPublicSystemeAutoriseDeleguant | header | Numéro public du système autorisé qui a délégué le contrôle sur son formulaire | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

### /api/v1/SIS/DeployerSysteme

#### POST
##### Summary:

FRW166 - Déployer un système au complet

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| X-ApiKey | header | Clé Api | No | string |
| X-NoPublicSystemeAutorise | header | Numéro public du système autorisé | No | string |
| X-NoPublicSystemeAutoriseDeleguant | header | Numéro public du système autorisé qui a délégué le contrôle sur son formulaire | No | string |
| X-IdentifiantUtilisateur | header | Identifiant de l'utilisateur | No | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Succès |
| 400 | Paramètre manquant ou invalide |
| 401 | Accès non autorisé |
| 500 | Paramètre manquant, invalide ou erreur interne du serveur |

null

### /api/Soumettre/CreerCookie/{nsForm}

#### POST
##### Summary:

Créer un cookie de test

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| nsForm | path | Id formulaire | Yes | long |
| idParticipant | query | Id participant du workflow | No | long |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/Soumettre/Transmission/{shortInstance}

#### POST
##### Summary:

FRW311 - Gérer la soumission d'un formulaire dynamique

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| shortInstance | path | Id publique raccourcie de la session utilisateur | Yes | string |
| version | query | La version du fichier de config à utiliser | No | string |
| testerTransmission | query | Permet de bypasser les validations et retourner le résultat de la configuration de transmission | No | boolean |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/Soumettre/MiseAJour/{idSystemeAutorise}/{typeFormulaire}/{version}/{shortInstance}

#### POST
##### Summary:

Gérer la mise à jour de l'entrée dans la table des formulaires aux changements de section et au clic "Enregistrer"

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idSystemeAutorise | path | ex: 1 | Yes | integer |
| typeFormulaire | path | ex: 3003 | Yes | string |
| version | path | ex: 0 | Yes | string |
| shortInstance | path | ex: i3-AbG0-5UeQwX2MYv5E6w | Yes | string |
| estActionUtilisateur | query |  | No | boolean |
| estMiseAJourExpiration | query |  | No | boolean |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/Soumettre/ObtenirChampsObsoletes/{idSystemeAutorise}/{typeFormulaire}/{version}/{shortInstance}

#### POST
##### Summary:

Gérer la mise à jour de l'entrée dans la table des formulaires aux changements de section et au clic "Enregistrer"

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idSystemeAutorise | path | ex: 1 | Yes | integer |
| typeFormulaire | path | ex: 3003 | Yes | string |
| version | path | ex: 0 | Yes | string |
| shortInstance | path | Id de session | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/Soumettre/Verifier/{shortInstance}

#### POST
##### Summary:

Gérer la mise à jour de l'entrée dans la table des formulaires aux changements de section et au clic "Enregistrer"

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| shortInstance | path | ex: i3-AbG0-5UeQwX2MYv5E6w | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/Soumettre/DeconnecterSessionUtilisateur/{shortInstance}

#### POST
##### Summary:

Deconnecter la session de l'utilisateur si celle-ci est expirer

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| shortInstance | path | ex: i3-AbG0-5UeQwX2MYv5E6w | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/Soumettre/Signer/{shortInstance}

#### POST
##### Summary:

FRW21C : Création d'une signature numérique pour un participant

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| shortInstance | path |  | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |

### /api/Textes/Obtenir/{langue}/{systemeAutorise}/{typeFormulaire}/{version}

#### GET
##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| langue | path |  | Yes | string |
| systemeAutorise | path |  | Yes | integer |
| typeFormulaire | path |  | Yes | string |
| version | path |  | Yes | integer |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |

### /api/v1/Workflow/ObtenirSommaireWorkflow/{shortInstance}

#### GET
##### Summary:

FRW354 - Obtenir le sommaire d'un workflow

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| shortInstance | path | ShortInstance | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 401 | Unauthorized |

### /api/v1/Workflow/ModifierFormulaire/{idSystemeAutorise}/{typeFormulaire}/{version}/{shortInstance}

#### POST
##### Summary:

FRW356 - Modifier le formulaire en cours de workflow

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| idSystemeAutorise | path |  | Yes | integer |
| typeFormulaire | path |  | Yes | string |
| version | path |  | Yes | integer |
| shortInstance | path |  | Yes | string |
| Accept-Language | header | Spécifie la langue préférée pour les réponses (en-CA ou fr-CA) | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | OK |
| 400 | Bad Request |
| 401 | Unauthorized |
