# Liste des fonctionnalités offertes par FRW
1. Développement
   * Développement « low code » avec des fichiers de configurations YAML;
   * Bac à sable pour visualiser les modifications en temps réel sans besoin de déployer les changements;
1. Accès au formulaire
   * Anonyme à partir d’un site public;
   * Sécurisés à partir d’un portail authentifié;
1. Affichage
   * Multilingue (français et anglais);
   * Responsive (appareils mobiles et tablettes);
   <!-- markdown-link-check-disable -->
   * Respecte le [standard du gouvernement du Québec en ressources informationnelles (SGQRI 008 2.0)](https://www.tresor.gouv.qc.ca/fileadmin/PDF/ressources_informationnelles/AccessibiliteWeb/standard-access-web.pdf) 
   <!-- markdown-link-check-enable -->
1. Contrôles
   * Respect des règles du Système de design gouvernemental.;
   * Éventail élargi de contrôles disponibles;
     * Lien vers le [guide de configuration des formulaires](https://formulaires.it.mtess.gouv.qc.ca/Form/7/P700U/0/N);
     * Exemples : Contrôle d’adresse normalisé, ajout de pièces jointes;
   * Validations de champs prédéfinies;
1. Pré remplissage des données
   * Un système autorisé dans FRW peut envoyer des données pour pré remplir son formulaire afin d’éviter la saisie d’informations déjà connues.
1. Enregistrement et reprise
   * Anonyme : La reprise s’effectue via un lien envoyé par courriel nécessitant un mot de passe défini par l’utilisateur lors de l’enregistrement;
   * Authentifié : La solution FRW offre des APIs pour obtenir la liste des formulaires d’un utilisateur et reprendre des formulaires;
1. Transmission du formulaire
   * Validations avant transmission : Une page de révision est inclue dans la solution FRW afin d’effectuer toutes les validations sur le formulaire avant sa transmission;
   * Envoi des données du formulaire : Le système utilisant la solution FRW doit se prévoir un API qui recevra les données du formulaire envoyées lors de la transmission;
   * Production d’un fichier contenant les données du formulaire : La solution FRW permet de produire un fichier PDF contenant toute l’information saisie dans le formulaire à partir d’un gabarit Word ou d’un gabarit PDF avec champs de saisie dynamiques.
   * Envoi de courriel: La solution FRW peut envoyer des courriels lors de la transmission du formulaire. (Disponible à partir de la release 2024.2)
     * Le PDF du formulaire ainsi que les pièces jointes téléversées par l'utilisateur peuvent être ajoutées dans les courriels.
1. Sécurité
   * Données chiffrées;
   * Répond aux normes de sécurités du MESS;
