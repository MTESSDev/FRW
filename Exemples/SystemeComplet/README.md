# FRW - Exemples de config

| Exemple | Particularitées | Sortie|
|------|------|-----|
| 0000 | Cas simple de base, style "hello world" | Pdf mappé|
| 2601 | Complexité moyenne, formulaire "standard" | Pdf mappé |   
| 3003 | Gros formulaire de la mort, attention ça fait mal! | Pdf(s) mappés | 
| INF03| Fomulaire moyenne complexité | Fichier word |

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