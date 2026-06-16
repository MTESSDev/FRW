# Liste des formulaires transmis
Cette fonctionnalité permet aux différents partenaires (ministères et organismes) d'extraire de façon autonome la liste des formulaires transmis et facturés pour une période donnée (période d'un an maximum). L'extraction est envoyée par courriel sous forme de fichier CSV compressé (ZIP) et facilite grandement la reddition de comptes et le suivi de la facturation.

## 1. Configurations requises
Avant de pouvoir utiliser la page d'extraction, il est **obligatoire** d'autoriser les adresses courriels des utilisateurs dans la configuration de votre système autorisé (généralement dans le fichier `default.v0.form.yml`). 
Il est également possible d'associer vos formulaires à des codes de facturation spécifiques pour faciliter vos suivis.

**Exemple de configuration :**
```yaml
config:
  statistiques:
    formTransmis:
      courrielsAutorise:
        - prenom.nom@votre-organisme.gouv.qc.ca
        - finances@votre-organisme.gouv.qc.ca
      facturation:
        - typeForm: "3003"
          codeFacturation: CF3003
        - typeForm: "P700U"
          codeFacturation: CFP700U
```

## 2. Accéder à la page
La page est accessible via l'URL suivante, en remplaçant les variables par les informations de votre système :
`.../statistiques/transmis/{IdSystemeAutorise}?s={SystemeAutoriseGuid}`
- `{IdSystemeAutorise}` : Votre numéro de système autorisé.
- `{SystemeAutoriseGuid}` : Le GUID (clé publique) de votre système autorisé.

*Note : Si vous ne connaissez pas ces paramètres, veuillez contacter l'équipe FRW.*

## 3. Comment utiliser la page
1. **Courriel** : Saisissez votre adresse courriel. **Attention** : Celle-ci doit correspondre exactement à l'une des adresses autorisées dans la configuration de votre système (voir l'étape 1).
2. **Date de début et Date de fin** : Sélectionnez la période pour laquelle vous souhaitez obtenir les données.
   - La période de recherche se base sur la **date de transmission** des formulaires.
   - La plage de dates maximale autorisée est de **1 an**.
   - La date de fin ne peut pas se situer dans le futur.
3. Cliquez sur le bouton de soumission pour lancer la demande.

## 4. Résultat de l'extraction
Si votre courriel est autorisé et la demande est valide, l'extraction s'effectuera en arrière-plan. Vous recevrez ensuite un courriel contenant un fichier d'archive `.zip` en pièce jointe.

- L'archive contient les données demandées en format `.csv`. 
- Afin d'assurer la rapidité et la stabilité du système, chaque fichier `.csv` contient un maximum de 250 000 lignes. Si votre extraction dépasse ce nombre, l'archive contiendra plusieurs fichiers subdivisés (`formulairesTransmis_1.csv`, `formulairesTransmis_2.csv`, etc.).
- **Les informations incluses** : Numéro de confirmation, Date de création, Date de transmission, Code du système autorisé (qui permet d'identifier le Ministère/Organisme et le système), Code du partenaire externe (le cas échéant), et le Code de facturation.
