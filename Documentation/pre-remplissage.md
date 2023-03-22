# Pré-remplir les données d'un formulaire

Ce guide explique comment fournir des données afin de pré-remplir des champs du formulaire comme le nom ou l'adresse.

Vous devez créer un service de pré remplissage dans votre système qui fait cette opération.

Le but de ce service est de produire un contenu de formulaire correspondant au format attendu par FRW en y ajoutant les valeurs déterminées par votre système.

Voici comment nous suggérons de procéder:

<h2>Paramètres d'entrée du service de pré remplissage</h2>

| Nom du paramètre | Description |
| ---- | ---------- |
| Type formulaire | Correspond au nom du répertoire FRW de votre formulaire |
| Dictionnaire d'objet | Dictionnaire clé-valeur qui contiendra toutes les valeurs que vous désirez fournir au formulaire |

<h2>Traitement à effectuer</h2>
<ol>
  <li>Définir la structure des données de pré remplissage pour chaque type de formulaire</li>
  Vous pouvez utiliser des fichiers de configuration pour gérer cette partie.
  Voici un exemple de configuration de pré remplissage dans lequel on défini les noms des champs du formulaire (à gauche) et les valeurs reçues en paramètre d'entrée (à droite):<br>
  preRemplissage: |
  {
    "form": {
        "adulte1NomFamille": {{{Json GD_NM_INDV}}},
        "adulte1Prenom": {{{Json GD_NM_PREN_INDV}}},
        "adulte1DateNaissance": {{{Json GD_D_NAIS}}},
        "adulte1Nas1": {{{Json GD_N_NAS}}},
        "adulte1Sexe": "{{#ifCond GD_C_SEXE '=' "M"}}Masculin{{else}}Feminin{{/ifCond}}",
        "adulte1Cp12": {{{Json GD_N_CP10 GD_N_CP12_JUM}}},
        "adulte1Nam": {{{Json GD_N_NAM}}},
        "adulte1Adresse": [
          {
            "NoCivique": {{{Json GD_A_NUMR_CIVQ}}},
            "Appartement": {{{Json GD_A_NUMR_APPR}}},
            "CodePostal": {{{Json GD_A_COD_POST}}},
            "Rue": {{{Json GD_A_RUE_RANG_CASR}}},
            "Municipalite": {{{Json GD_A_NOM_MUNC}}},
            "Province": "Québec"
          }]
    },
    #La partie estampille permet d'envoyer des données du système dans l'estampille apposée sur le fichier produit par FRW lorsqu'applicable.
    "estampille": {
        "texteAuthentification": "{{{TexteAuthentification}}}"
    }
  }
  <li>Le service doit récupérer la structure définie au point précédent et remplacer les balises par les valeurs reçues en paramètre d'entrée.</li>
  <li>Le service retourne l'information en sortie.</li>
</ol>

<h2>Paramètres de sortie du service de pré remplissage</h2>

| Nom du paramètre | Description |
| ---- | ---------- |
| Contenu formulaire | Contient la structure de pré remplissage avec les valeurs remplacées en format JSON |
