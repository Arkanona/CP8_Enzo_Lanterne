# Lanterne API

Lanterne est une API REST Express qui référence des curiosités locales : lieux discrets, détails architecturaux et petites histoires de quartier.

## Pré-requis

- Node.js 20 ou supérieur
- npm

## Installation et lancement local

```text
npm install
npm run check
npm test
npm start
```

L’API est disponible sur `http://localhost:3000`.

## Routes principales

- `GET /api/health`
- `GET /api/curiosities`
- `GET /api/curiosities?q=canal&limit=5`
- `GET /api/curiosities/:slug`

Le déploiement cible Vercel. Les variables d’environnement sont listées dans `.env.example`. Aucune donnée sensible ne doit être ajoutée au dépôt.

## Liens publique Vercel

`https://cp-8-lanterne-8pke.vercel.app/`

Exemple de routes possibles : 

- `https://cp-8-lanterne-8pke.vercel.app/api/health`
- `https://cp-8-lanterne-8pke.vercel.app/api/curiosities`
- `https://cp-8-lanterne-8pke.vercel.app/api/curiosities?q=canal&limit=5`
- `https://cp-8-lanterne-8pke.vercel.app/api/curiosities/:slug`

## Liens GitHub
`https://github.com/Arkanona/CP8_Lanterne`