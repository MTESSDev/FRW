# Partenaires externes
La fonctionnalité de partenaires externes permet à un système autorisé de déléguer certaines interactions de ses formulaires (comme l'initiation et le suivi) à des entreprises privées ou organismes externes partenaires, sans pour autant leur donner les accès complets d'un système autorisé du gouvernement.

> Disponible à partir de la release [2026.x](https://github.com/MTESSDev/FRW/releases)

## Avantages de la fonctionnalité
- **Délégation et efficacité :** Permet aux partenaires de démarrer des formulaires et de pré-remplir les données pour leurs clients, allégeant ainsi le fardeau administratif du citoyen.
- **Suivi et traçabilité :** Le partenaire externe qui a initié un formulaire est enregistré dans la base de données de FRW, ce qui permet de générer des rapports d'utilisation (et potentiellement de la facturation) au prorata de l'usage de chaque partenaire.
- **Sécurité :** L'accès est strictement encadré par formulaire et par des clés de sécurité uniques, avec des jetons ("secrets") générés pour chaque instance de formulaire afin de limiter la portée des actions du partenaire.

## Cas d'utilisation
Voici quelques exemples génériques illustrant l'utilité des partenaires externes :

**Cas 1 : Processus d'inspection et de certification délégué** <br>
Un ministère gère l'émission de certificats de conformité, mais délègue l'inspection sur le terrain à des firmes privées d'experts. 

*Utilisation :* La firme d'inspection (partenaire externe) se connecte à son propre système d'entreprise pour démarrer le formulaire de certification de FRW au nom du citoyen. Elle pré-remplit les données techniques de l'inspection. Le citoyen reçoit ensuite le lien pour compléter sa section, payer et signer. L'agence gouvernementale reçoit le formulaire officiel complet.

**Cas 2 : Demandes d'aide financière via des établissements scolaires** <br>
Un organisme offre des bourses d'études, mais les demandes sont orchestrées par des établissements d'enseignement privés. 

*Utilisation :* L'école (partenaire externe) démarre le formulaire de demande pour ses étudiants. L'école peut ensuite suivre l'état d'avancement de la demande de l'étudiant (ex: "En cours", "Transmis") directement depuis son propre portail étudiant.

---

## Configuration (Pour le système autorisé)
En tant que système autorisé, vous êtes responsable de configurer et déployer vos partenaires externes et les associer à vos formulaires.

Le déploiement est effectué avec l'outil [azurepipeline-mtess-frw-deploiement](https://github.com/MTESSDev/azurepipeline-mtess-frw-deploiement).

### 1. Définir les partenaires externes
Vous devez créer un fichier nommé `partenairesExternes.yml` à la racine de votre système (au même niveau que vos répertoires de formulaires). Ce fichier permet de définir des regroupements et de déclarer vos partenaires. Ce fichier est pris en compte au moment de déployer vos configurations.

Voici un exemple de configuration :

```yaml
partenairesExternes:
  groupe_certification:
    - code: "FIRME_A"
      nom: "Firme d'inspection A inc."
      cle: "34d9e1c8-9b0c-4a7e-8f1b-5c3a2e5f6a7b"
    - code: "FIRME_B"
      nom: "Experts B"
      cle: "24d9e1c8-9b0c-4a7e-8f1b-5c3a2e5f6a7b"

  groupe_bourses:
    - code: "ECOLE_XYZ"
      nom: "Collège XYZ"
      cle: "12345678-9abc-def0-1234-56789abcdef0"
```

> **Règles de validation du code partenaire :**
> - Maximum de 30 caractères alphanumériques.
> - Non sensible à la casse.
> - Aucun espace ni caractères spéciaux (les tirets `-` et soulignés `_` sont permis).
> - Un partenaire externe ne peut être présent que dans un seul regroupement à la fois.

> **Retrait d'un partenaire :** Pour désactiver un partenaire, il suffit de retirer son bloc du fichier `partenairesExternes.yml` (ou de le mettre en commentaire) et de redéployer. FRW désactivera automatiquement ce partenaire en base de données.

### 2. Autoriser un regroupement dans un formulaire
Une fois les partenaires définis globalement, vous devez indiquer quel formulaire peut être utilisé par quel regroupement de partenaires. Cela se configure dans le fichier `form.yml` de votre formulaire.

```yaml
config:
  securite: 
    # Regroupements de partenaires externes autorisés
    partenairesExternesAutorises:
      - groupe_certification
```

*Seuls les partenaires appartenant au regroupement `groupe_certification` pourront interagir avec ce formulaire.*

---

## Intégration (Pour le partenaire externe)
Cette section explique comment le système informatique du partenaire externe peut interagir avec les API de FRW pour démarrer et suivre un formulaire.

### Démarrer un formulaire
Pour démarrer un nouveau formulaire au nom d'un client, le partenaire doit appeler l'API [InteragirFormPartenaire](../Swagger/readme.md#apiv1sisinteragirformpartenaire) `FRW131`.

1. **Préparer les données de pré-remplissage** (facultatif). Tout comme pour un système autorisé, le partenaire peut injecter des données connues pour alléger la saisie.
2. **Appel à l'API FRW131 :** Le partenaire appelle l'API en fournissant sa clé secrète de partenaire (`cle`) dans l'entête HTTP. FRW valide la clé, crée le formulaire et associe ce dernier au code du partenaire pour assurer la traçabilité.
3. **Retour de l'API :** L'API retourne un `No Public Session` ainsi qu'un `secret` chiffré.
    *   **Attention :** Ce `secret` est crucial. Le partenaire externe doit le sauvegarder dans son système, car il sera exigé pour tous les appels futurs concernant ce formulaire spécifique.
4. **Redirection de l'utilisateur :** Le partenaire construit l'URL et redirige son client vers le formulaire pour qu'il puisse le compléter :

    L'URL prend la forme suivante : `{Adresse du site FRW}/{langue}/Reprise?no={No Public Session}`

    TODO à ajuster pour le header `x-secret`

### Obtenir les informations et le statut d'un formulaire
Le partenaire externe peut, en tout temps après la création d'un formulaire, consulter l'état d'avancement de ce dernier via l'API [ObtenirInfosFormPartenaire](../Swagger/readme.md#apiv1sisobtenirinfosformpartenaire) `FRW118`.

1. **Appel à l'API FRW118 :** L'appel doit inclure :
    *   La `cle` du partenaire (en entête HTTP).
    *   Le `secret` du formulaire obtenu lors de la création (en entête HTTP).
2. **Informations retournées :**
    *   Le numéro public du formulaire.
    *   Le code du type de formulaire.
    *   L'état du formulaire (ex: *En cours*, *Transmis*).
    *   Les informations d'avancement du *workflow* (le cas échéant).
    *   **Si le formulaire est transmis :** Les données complètes du formulaire, le lien vers le PDF généré et les liens des pièces jointes (PJ) téléversées par le client.

### Télécharger une pièce jointe
Si le partenaire souhaite rapatrier les pièces jointes soumises par l'utilisateur une fois le formulaire transmis, il doit utiliser l'API de téléchargement existante de FRW (`FRW121`). 

Lors de cet appel, le partenaire doit obligatoirement inclure l'entête HTTP `x-secret` contenant le secret du formulaire. FRW validera cette information avant d'autoriser le téléchargement.

### Reprendre un formulaire
*À noter :* Actuellement, la reprise d'un formulaire directement via l'API par un partenaire externe n'est pas supportée. L'utilisateur (le citoyen) devra utiliser le mécanisme de reprise par courriel habituel fourni par FRW pour y accéder à nouveau ultérieurement.