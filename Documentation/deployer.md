# Déployer

[Voir la documentation de l'outil de déploiement Azure DevOps](https://marketplace.visualstudio.com/items?itemName=MTESS.mtess-frw-deploiement)

## ⚠️ Important

Afin de respecter la nomenclature FRW et d'assurer le bon fonctionnement du traitement automatisé, le nom du formulaire doit être **strictement identique** au nom du répertoire qui le contient.

Les fichiers `.bind.yml`, `.transmission.yml`, `.form.yml`, etc. doivent également reprendre ce même nom comme préfixe. Toute différence de nom, de casse (majuscules/minuscules) ou de structure entraînera un échec du traitement.

✅ Correct

```text
3003/
└── 3003.v1.transmission.yml
└── 3003.v1.bind.yml
└── 3003.v1.form.yml
```

❌ Incorrect

```text
3003/
└── transmission.yml
└── bind.3003.yml
└── 3003-01.v1.form.yml
```