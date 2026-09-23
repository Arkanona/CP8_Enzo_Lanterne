### 2 Préparer le projet Vercel

## Relier le projet

J'ai du relier le projet GitHub à Vercel, j'ai installer Vercel sur mon Github.

## Environnements

L'environnement `Preview` permet de déployer et de tester des modifications dans un environnement réel sans affecter votre site de production.

L'environnement de `Production` est la version active de votre site ou application, destinée aux utilisateurs.

## Variables d'environnements

Les variables d'environnement sont des paires clé-valeur configurées en dehors de votre code source, permettant à chaque valeur de varier selon l'environnement. Ces valeurs sont chiffrées au repos et visibles par tout utilisateur ayant accès au projet. 

## Déploiement

Pour déployer le projet on doit se rendre sur `https://vercel.com/`, crée un compte ou se connecter.
J'ai ensuite choisi d'installer Vercel sur mon GitHub.
Une fois cela fait j'ai selectionner mon projet et je les déployer.

En essayant de déployer le projet il y'a eu un warning pour la version de Node et une erreur par rapport au build.
J'ai mis à jour la version de Node.js qui était en `>=20` → `24.x`. 
J'ai renommé le fichier `api` en `src`.
Et le déploiement à pu être effectué à `11h01`.

## Déploiement sans GitHub

Utiliser la Vercel CLI 
C'est idéale pour les applications dynamiques (React, Next.js, Vue, etc.) :
- Installez l'outil en ligne de commande : `npm i -g vercel`.
- Ouvrez un terminal dans le dossier de votre projet.
- Connectez-vous à votre compte : `vercel login`.
- Lancez le déploiement en tapant : `vercel`.
- Pour un déploiement direct en production, utilisez : `vercel --prod`

## 5 Documenter la mise à jour et le retour arrière

J'ai ajouter un fichier `test.js` j'ai ensuite push le projet, une fois cela fait j'ai fait un `instant rollback` sur Vercel et je suis revenu sur la version précédente.
