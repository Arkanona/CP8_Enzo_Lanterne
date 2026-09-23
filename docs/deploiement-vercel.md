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

<!-- Corrigé -->
## Déploiment Vercel

Depuis la racine du projet :
```
vercel link
> Create a new project
> Name : Nommez le projet ou appuyer sur entrée
> Connect this Git repository to automatically deploy changes on every push : Y
> Code directory : Laisser par défaut
> Customise settings : N
```

Cela crée un nouveau projet vide sur Vercel. 
Vous devez configurer les variables d'environnement.
Menu `Environnement variables` → `Add environnement variable`
Choisir `Config`
Ajouer les clés qui sont dans `.env.example`
Configurer la variable d'environnement en fonction de l'environnement (production)
ensuite déployer avec `vercel`, cela permet de déployer la version en production (premièere version)

## Déployer la version de dev

1. Créer une branche develop : `git checkout -b develop`
2. Déployer avec `vercel`
3. Configurer les variables d'environnement pour la version Preview
4. Lancer un Redeploy sur la version Preview


## Mise à jour 

Pour publier une nouvelle version :

1. Passer sur la branche develop : `git switch develop`
2. Mettre à jour le projet
3. Mettre à jour les test si le comportement change
4. Lancer `npm run check` et `npm test`
5. Créer un commit explicite
6. Déployer la preview : `vercel`
7. Vérifier les routes
8. Publier en production

### Publier en production

Pour publier en production : 

1. Fusionner la branche develop avec la branche main
2. Lancer `vercel --prod`

## Retour en arrière

En cas d'échec, selectionner le déploiement précédent dans l'historique Vercel et le promouvoir en production