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

**Génération de la clé :**
Il est de votre responsabilité de générer la clé de partenaire de votre choix; celle-ci peut prendre la forme d'un GUID ou d'une chaîne de caractères.

**Règles de validation du code partenaire :**
- Maximum de 30 caractères alphanumériques.
- Non sensible à la casse.
- Aucun espace ni caractères spéciaux (les tirets `-` et soulignés `_` sont permis).
- Un partenaire externe ne peut être présent que dans un seul regroupement à la fois.

**Retrait d'un partenaire :** Pour désactiver un partenaire, il suffit de retirer son bloc du fichier `partenairesExternes.yml` (ou de le mettre en commentaire) et de redéployer. FRW désactivera automatiquement ce partenaire en base de données.

### 2. Autoriser un regroupement dans un formulaire
Une fois les partenaires définis, vous devez indiquer quels regroupements peuvent utiliser quel formulaire. Cela se configure dans le fichier `form.yml` de votre formulaire, avec la clé `securite.partenairesExternesAutorises` :

```yaml
config:
  securite:
    # Regroupements de partenaires externes autorisés
    partenairesExternesAutorises:
      - groupe_certification
```

*Seuls les partenaires appartenant au regroupement `groupe_certification` pourront interagir avec ce formulaire.*

**Règles :**
- Les valeurs de la liste sont les noms de **regroupement** déclarés dans `partenairesExternes.yml` (ex: `groupe_certification`), et non les codes ou les clés des partenaires.
- La comparaison ne tient pas compte de la casse.
- **Refus par défaut :** si la clé `partenairesExternesAutorises` est absente ou vide, aucun partenaire externe ne peut utiliser le formulaire. Ajoutez-la à chaque formulaire que vous ouvrez à des partenaires.
- La liste est lue dans le fichier du **formulaire** seulement (pas dans `default.vX.form.yml`) : chaque formulaire déclare ses propres regroupements autorisés.
- La configuration est prise en compte au moment de déployer vos configurations.

**Comportement pour le partenaire :**

| Situation | Réponse |
|---|---|
| Clé de partenaire invalide ou partenaire retiré | HTTP 401 |
| Clé valide, mais regroupement du partenaire absent de `partenairesExternesAutorises` du formulaire | HTTP 403 |

Cette validation s'applique à la création d'un formulaire (FRW111), à l'obtention de sa structure (FRW119) et au déclenchement d'une transmission personnalisée (FRW122).