# Titre du Projet

Ce projet consiste en une application e-commerce simple. Il est scindé en deux parties principales : une partie front-end (dossier `spa`) réalisée avec React, et une partie back-end (dossier `node`) basée sur un serveur Express qui gère une base de données JSON.

## Structure du Projet

- **client** : Ce dossier contient le code source de l'application VueJS. Il inclut une Single Page Application (SPA) qui permet aux utilisateurs de visualiser, ajouter, modifier et supprimer des produits.

- **server** : Ce dossier contient le code source du serveur Express. Le serveur gère les requêtes RESTful pour créer, lire, mettre à jour et supprimer des données dans un base donne MYSQL.

## Prérequis

- Node.js (version 12 ou supérieure recommandée)
- Un navigateur web moderne
- MYSQL base de donne tp_vue

## Installation et Exécution

1. Clonez le dépôt sur votre machine locale.

```bash
git clone https://github.com/Vanessandrade7/tp3_webavance.git
```

2. Accédez au dossier du projet.

```bash
cd tp3_webavance
```

### Front-end (client)
1. Accédez au dossier client.

```bash
cd client
```

2. Installez les dépendances nécessaires avec npm (ou yarn).

```bash
npm install
# ou
yarn install
```

3. Démarrez l'application React.
```bash
npm run serve
# ou
yarn run serve
```

Votre application devrait maintenant être accessible à l'adresse http://localhost:8081.

### Back-end (Serveur Node)
1. Dans un autre terminal, accédez au dossier node.

```bash
cd server
```
2. Installez les dépendances nécessaires.
```bash
npm install
# ou
yarn install
```
3. Démarrez le serveur Express.

```bash
node server.js
```

Le serveur devrait maintenant être en fonctionnement et écouter sur http://localhost:8080.

Explication du Projet
Le projet est une simulation simplifiée d'une application e-commerce. Le front-end est une SPA qui permet une navigation fluide entre les pages et offre une interface utilisateur intuitive pour gérer les produits. Le back-end est un serveur Express simple qui gère les opérations CRUD sur un fichier JSON qui sert de base de données. Le projet illustre comment on peut structurer une application en séparant les préoccupations front-end et back-end, tout en fournissant des fonctionnalités basiques de gestion de produits dans un contexte e-commerce.