# Cycle de vie et états

## Liste des états

| Code d'état | Description |
|---|---|
| CRE | Création, formulaire neuf, jamais ouvert encore |
| MAJ | Mis à jour par l'utilisateur |
| COURRIEL | Un courriel de reprise a été envoyé (mode anonyme) |
| REP | Repris par l'utilsateur |
| SUP | Supprimé par l'utilisateur |
| TRANSMIS | Transmis (soumis) par l'utilisateur |
| EPURE | Épuré par le traitement lot, formulaire trop vieux |
| REPAGENT | Lorsqu'un agent se connecte au formulaire en co-navigation |
| WORKFLOW | Lorsqu'une étape de workflow a été soumise |
| EXP | Lorsque le délai d'expiration du workflow a été atteint |
| MOD | Lorsqu'un formulaire en workflow est réinitialisé à l'étape initiale par l'utilisateur principal |

## Délais d'épuration

Les formulaires sont épurés après un certain délai selon le type du formulaire. Voici les délais en jours pour chaque type de formulaire.

| Description | Nombre de jours QA | Nombre de jours PROD |
|---|---:|---:|
| Formulaire confidentiel transmis | 0* | 0* |
| Formulaire confidentiel abandonné | 0* | 0* |
| Formulaire de longue durée transmis | 120 | 365 |
| Formulaire de longue durée non transmis | 30 | 365 |
| Formulaire transmis | 90 | 90 |
| Formulaire anonyme non transmis | 14 | 90 |
| Formulaire authentifié non transmis | 14 | 180 |
| Formulaire supprimé par l'utilisateur | 1 | 1 |
| Formulaire expiré | 30 | 30 |

_* 0 jour signifie que l'épuration est effectuée immédiatement après l'abandon ou la transmission_
