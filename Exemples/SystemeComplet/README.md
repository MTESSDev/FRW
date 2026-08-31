# FRW - Exemples de config

| Exemple | Particularitées | Sortie|
|------|------|-----|
| 0000 | Cas simple de base, style "hello world" | Pdf mappé|
| 2601 | Complexité moyenne, formulaire "standard" | Pdf mappé |   
| 3003 | Gros formulaire de la mort, attention ça fait mal! | Pdf(s) mappés | 
| INF03| Fomulaire moyenne complexité | Fichier word |

## ⚠️ Important

Le nom du formulaire doit être **strictement identique** au nom du répertoire qui le contient.

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