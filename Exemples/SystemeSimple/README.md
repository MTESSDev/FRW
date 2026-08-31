# FRW - Exemples de config pour un système "simple" de base

## ⚠️ Important

Afin de respecter la nomenclature FRW et d'assurer le bon fonctionnement du traitement automatisé, le nom du formulaire doit être **strictement identique** au nom du répertoire qui le contient.

Les fichiers `.bind.yml`, `.form.yml`, etc. doivent également reprendre ce même nom comme préfixe. Toute différence de nom, de casse (majuscules/minuscules) ou de structure entraînera un échec du traitement.


✅ Correct

```text
FORMXYZ/
└── FORMXYZ.v1.bind.yml
└── FORMXYZ.v1.form.yml
```

❌ Incorrect

```text
FORMXYZ/
└── bind.yml
└── form.FORMXYZ.yml
```