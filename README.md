# Blockchain Wallet Application (Tezos)

This application is a wallet prototype for the **Tezos** blockchain, built with **Node.js** and **Express**. It allows users to interact with the Tezos network to manage account activation and configuration.

## 🚀 Features

- **Account Initialization**: Unlocking identities (specifically those from the fundraiser) via mnemonic, email, and password.
- **Account Activation**: Sending activation operations to the Tezos network.
- **Key Revelation (Reveal)**: Sending the reveal operation necessary to validate the address on the blockchain and enable future transactions.
- **Web Interface**: Using EJS for server-side view rendering.

## 🛠️ Tech Stack

- **Backend**: Node.js, Express
- **Blockchain**: [ConseilJS](https://github.com/Cryptonomic/ConseilJS) (Library for Tezos)
- **Template Engine**: EJS
- **Styling**: CSS (Public/stylesheets)

## 📁 Project Structure

- `app.js`: Entry point for the Express application.
- `bin/www`: Server startup script.
- `controller/`: Contains business logic (notably `TezosController.js`).
- `routes/`: Definition of API/Web endpoints.
- `views/`: EJS files for the user interface.
- `comptes.json`: Local storage for Tezos account information (mnemonic, secret, etc.).

## ⚙️ Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Blockchain_wallet_app

2. Install  dependencies :
   ```bash
   npm install
   ```

## 🖥️ Utilisation

To start the ddevelopment server :
```bash
npm start
```

By default, application is  accessible at  `http://localhost:3000`.

### Available Routes
- `GET /` : Homepage.
- `GET /create` : triggers the creation and activation logic for the configured account.

## ⚠️ Security Notes 
Sensitive information (mnemonics, private keys) is currently managed via the `comptes.json` file. **NNever use this storage method in production** or commit real private keys to a public repository.

## 📄 License
This project is under a free license. See the LICENSE file for more details.


