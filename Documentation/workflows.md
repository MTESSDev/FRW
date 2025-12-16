# workflows

## Qu’est-ce qu’un workflow?
Le workflow est un type d'aiguillage qui permet d'impliquer plusieurs participants dans la complétion d'un formulaire séparé en plusieurs étapes.

La configuration du workflow vous permet de déterminer :
- Qui peut remplir quelles sections et dans quel ordre,
- Qui peut voir quelles informations aux différentes étapes,
- Quelles conditions doivent être réunies pour passer d'une étape à l'autre,
- Quelles notifications sont envoyées.

Exemple d'utilisation

Cas 1 : Processus Légal (Avec Signature)
Le citoyen soumet une demande -> L'analyste vérifie la conformité -> Le directeur appose sa signature électronique -> Le permis officiel est généré et envoyé.

Cas 2 : Processus Opérationnel (Sans Signature) 
Un couple fait une demande, la première personne remplit sa partie -> Le conjoint complète avec ses informations -> Le ministère reçoit la demande complète.

## Guide d'utilisation
### Config transmission
Le workflow est configuré dans le fichier VOTRE_FORM.v1.transmission.yml.

Voici un exemple de configuration de workflow.

```yml
workflows:
  - id: karate
    roles: 
      # Le premier rôle défini est l'utilisateur principal; 
      # C'est celui qui initie le formulaire, et c'est le seul qui peut le réinitialiser 
      # à l'étape initial en cas de modification.
      - id: sensei 
        label: 
          fr: "Sensei"
          en: "YesNoSensei"
      - id: eleve
        label: 
          fr: "Élève"
          en: "Student"
    etapes:
      # La 1e étape doit toujours être "initial".
      - id: initial 
        evenements:
          
          # Transmission initiale du formulaire, déclenche les tâches configurées dessous
          quandQuelqunTransmet: 
    
            # Créé les participants dont le rôle est "eleve" en extrayant les informations saisies dans le formulaire. 
            # Ces participants sont envoyés vers l'étape "contribution".
            - tache: interventionParticipant 
              options: 
                  role: eleve
                  vers: contribution
                  chargerCourrielsWorkflow: true 
                  modeBoutonTesterTransmission: simuler
            
            - tache: interventionParticipant
              options: 
                  role: sensei
                  chargerCourrielsWorkflow: true
                  modeBoutonTesterTransmission: simuler 
            
            # Pour chaque participant dont le rôle est "eleve" : 
            # - Génère un courriel du gabarit "demandeContribution" avec les informations de ce participant;
            # - Ce gabarit doit être défini sous "gabaritsCourriels:" de la présente config;
            # - Envoie ce courriel.
            - tache: envoyerCourrielParticipant
              options: 
                  role: eleve
                  gabarit: demandeContribution
            
            # Inscris une tâche asynchrone qui va s'exécuter après le délai de 48 heures et qui va expirer 
            # le formulaire et envoyer un courriel d'expiration (du gabarit "formExpire") à chaque participant
            - tache: expirerFormulaire
              options:
                  gabarit: formExpire # doit être défini sous gabaritsCourriels de la présente config
                  delaiExpirationHeures: 48
                  langue: fr

      # L'étape "contribution", vers laquelle les participants ont été envoyés à l'étape initial, est définie ici.
      - id: contribution 
        evenements:
          
          # Le dernier participant qui transmet sa partie de formulaire à l'étape "contribution" 
          # va déclencher l'exécution des tâches
          quandLeDernierTransmet:  
            
            - tache: interventionParticipant
              options: 
                role: sensei
                vers: transmission
                chargerCourrielsWorkflow: true   
                modeBoutonTesterTransmission: simuler 
            
            - tache: envoyerCourrielParticipant
              options: 
                role: sensei
                gabarit: dernSigTransmis
                modeBoutonTesterTransmission: simuler 

      # La dernière étape doit toujours s'appeler "transmission"
      - id: transmission 
        evenements:
          quandQuelqunTransmet:
            - tache: genererWord
            - tache: traiterDocumentsSoumis
            - tache: ajouterEstampille
            - tache: envoyerCourrielParticipant 
              options: 
                  role: sensei
                  gabarit: finFinal2
                  modeBoutonTesterTransmission: simuler 
                  filtresDocuments:
                    - typeFiltre: tacheSource
                      valeurs: genererWord

# Les gabarits de courriels sont définis ici
# Voir le guide fichiers-transmission.md pour le détail complet.
gabaritsCourriels:
  - id: demandeContribution
    [...]
  - id: dernSigTransmis
    [...]
  - id : formExpire
    [...]
```

### Config form
Vous devez ensuite configurer l'aiguillage, les "filtre étapes" et les courrielWorkflow dans votre formulaire. 

Voir le P700U Guide utilisateur FRW section [Aiguillage en mode workflow](https://formulaires.it.mtess.gouv.qc.ca/fr/Form/7/P700U/0/N/#p=sectWf). 




