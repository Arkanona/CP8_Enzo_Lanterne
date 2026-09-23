### 1 Auditer le projet 

## Arborescence
```
CP8_Lanterne/
├── docs/
│   ├── deploiement-vercel.md
│   ├── validation.md
│   └── veille.md
├── src/
│   ├── data/
│   └── index.js
├── tests/
│   └── api.test.js
├── .env.example
├── .gitignore
├── package-lock.json
├── package.json
├── README.md
└── vercel.json
```
## Dépendances

Pour les dépendances il y a ``cors`` et ``express``.

## Version Node.js

La version de Node.js est 24 ou supérieure.

## Scripts

Pour les noms des scripts : ``start``, ``dev``, ``check`` et ``test``.

## Routes 

Les routes principales sont : 
- `GET /api/health`
- `GET /api/curiosities`
- `GET /api/curiosities?q=canal&limit=5`
- `GET /api/curiosities/:slug`


## Les fichiers qui ne doivent pas être transmis dans Git  
```
.env
node_modules
```

## Sources

Mes principales sources pour la recherche on était la documentation Vercel.

## Informations retenues

L'environnement et les variables d'environnements.

## 6 Sécuriser la configuration

- Allez dans les paramètres de votre projet sur le tableau de bord Vercel.
- Ouvrez la section Deployment Protection.
- Activez Vercel Authentication pour restreindre l'accès aux personnes autorisées de votre équipe.

`Vercel Authentification`, `Password Protection`, `Trusted IPs`.
Source `https://vercel.com/docs/deployment-protection/methods-to-protect-deployments`.

