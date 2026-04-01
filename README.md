# Application Wallet Blockchain (Tezos)

Cette application est un prototype de portefeuille (wallet) pour la blockchain **Tezos**, construit avec **Node.js** et **Express**. Elle permet d'interagir avec le réseau Tezos pour gérer l'activation et la configuration de comptes.

## 🚀 Fonctionnalités

- **Initialisation de compte** : Déverrouillage d'identités (notamment issues de la levée de fonds/fundraiser) via mnémonique, email et mot de passe.
- **Activation de compte** : Envoi d'opérations d'activation vers le réseau Tezos.
- **Révélation de clé (Reveal)** : Envoi de l'opération de révélation nécessaire pour valider l'adresse sur la blockchain et permettre les futures transactions.
- **Interface Web** : Utilisation d'EJS pour le rendu des vues côté serveur.

## 🛠️ Stack Technique

- **Backend** : Node.js, Express
- **Blockchain** : [ConseilJS](https://github.com/Cryptonomic/ConseilJS) (Bibliothèque pour Tezos)
- **Moteur de template** : EJS
- **Style** : CSS (Public/stylesheets)

## 📁 Structure du Projet

- `app.js` : Point d'entrée de l'application Express.
- `bin/www` : Script de démarrage du serveur.
- `controller/` : Contient la logique métier (notamment `TezosController.js`).
- `routes/` : Définition des points de terminaison (endpoints) de l'API/Web.
- `views/` : Fichiers EJS pour l'interface utilisateur.
- `comptes.json` : Stockage local des informations d'un compte Tezos (mnémonique, secret, etc.).

## ⚙️ Installation

1. Clonez le dépôt :
   ```bash
   git clone <url-du-depot>
   cd Blockchain_wallet_app
   ```

2. Installez les dépendances :
   ```bash
   npm install
   ```

## 🖥️ Utilisation

Pour démarrer le serveur de développement :
```bash
npm start
```

Par défaut, l'application est accessible sur `http://localhost:3000`.

### Routes disponibles
- `GET /` : Page d'accueil.
- `GET /create` : Déclenche la logique de création et d'activation du compte configuré.

## ⚠️ Notes de sécurité
Les informations sensibles (mnémoniques, clés privées) sont actuellement gérées via le fichier `comptes.json`. **Ne jamais utiliser ce mode de stockage en production** ni commiter des clés privées réelles sur un dépôt public.

## 📄 Licence
Ce projet est sous licence libre. Voir le fichier LICENSE pour plus de détails.
