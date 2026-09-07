# 🔗 MediChain — Blockchain-Based Medicine Tracking & Verification System

MediChain is a full-stack decentralized application that tackles counterfeit medicine in healthcare supply chains. It gives every medicine batch a secure, tamper-proof identity on the blockchain — traceable from manufacturer, to distributor, to pharmacy, to the end customer.

Built as a project for the Blockchain (CS-472) course at University of Wah, under the guidance of Ma'am Muniba Khan.

---

## 📌 Problem Statement

Counterfeit and substandard medicines are a serious global health risk, especially in supply chains that lack transparency. Once a medicine leaves the manufacturer, there is often no reliable way to verify its authenticity, origin, or handling history before it reaches the patient.

MediChain solves this by recording every stage of a medicine's journey on an immutable, publicly verifiable blockchain ledger.

---

## ✨ Features

- **Manufacturer Module** — Register new medicine batches (name, batch ID, manufacturer, dates, dosage, quantity, storage instructions) directly on the blockchain, and generate QR codes for each batch.
- **Distributor Module** — Receive shipments, log shipment details (date, location, notes), and transfer ownership to the next stage in the supply chain.
- **Pharmacy Module** — Receive and manage inventory from verified distributors.
- **Customer Verification (Verify QR)** — Anyone can scan a QR code or enter a Batch ID to instantly verify a medicine's authenticity and full journey.
- **Blockchain Explorer** — View a live, transparent ledger of every transaction and block, including smart contract function calls, timestamps, and transaction hashes.
- **QR Code Generator** — Automatically generates a unique, scannable QR code for every registered medicine batch.
- **MetaMask Integration** — Secure wallet-based authentication for all blockchain interactions.

---

## 🛠️ Tech Stack

| Layer              | Technology                          |
|--------------------|--------------------------------------|
| Smart Contracts    | Solidity (`^0.8.0`)                  |
| Blockchain Network | Ethereum — Sepolia Testnet           |
| Frontend           | React                                |
| Wallet Integration | MetaMask                             |
| Contract           | `MedicineRegistry.sol`               |

---

## 🧱 Smart Contract Overview

The core contract, `MedicineRegistry.sol`, handles:
- Registering new medicine batches on-chain (`registerMedicine`)
- Storing structured medicine data (batch ID, name, manufacturer, generic name, dates, etc.)
- Initializing the blockchain instance (`initBlockchain`)
- Tracking ownership transfers as a batch moves through the supply chain

---

## 📷 Screenshots

*(Add screenshots of the Dashboard, Manufacturer Module, Distributor Module, Verify QR page, and Blockchain Explorer here — drag and drop them into this section on GitHub, or reference an `/assets` or `/screenshots` folder.)*

---

## ⚙️ Getting Started

### Prerequisites
- Node.js and npm installed
- MetaMask browser extension
- A wallet funded with Sepolia testnet ETH ([faucet link](https://sepoliafaucet.com))

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/medichain.git
cd medichain

# Install dependencies
npm install

# Start the development server
npm start
```

### Smart Contract Deployment
```bash
# Compile contracts
npx hardhat compile

# Deploy to Sepolia testnet
npx hardhat run scripts/deploy.js --network sepolia
```

> Update your `.env` file with your own RPC URL and wallet private key before deploying. **Never commit your `.env` file.**

---

## 🔐 Environment Variables

Create a `.env` file in the root directory with the following (do not commit this file):

```
SEPOLIA_RPC_URL=your_rpc_url_here
PRIVATE_KEY=your_wallet_private_key_here
```

---

## 👥 Team

- **Hira Syed**
- **Shameen Qayyum**

**Instructor:** Ma'am Muniba Khan — CS-472 Blockchain

---

## 📄 License

This project was developed for academic purposes as part of the CS-472 Blockchain course.

---

## 🙌 Acknowledgements

Thanks to our instructor and course team for guidance throughout the development of this project.
