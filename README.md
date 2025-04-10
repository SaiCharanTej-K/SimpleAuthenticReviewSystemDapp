# SimpleAuthenticReviewSystemDapp
# 🛡️ Authentic Review System

A decentralized web application (dApp) that allows users to rate candidates in a trustworthy and tamper-proof way using Ethereum blockchain and smart contracts.

## 📌 Features

- Admin (deployer) can add candidates.
- Admin and users can submit ratings for candidates.
- All reviews are stored immutably on the blockchain.
- Only the admin (the deployer address) can add new candidates.

---

## 🚀 Getting Started

### ✅ Prerequisites

- [MetaMask](https://metamask.io/) browser extension
- [Remix IDE](https://remix.ethereum.org/) for writing and deploying smart contracts
- [Ganache](https://trufflesuite.com/ganache/) to simulate a local Ethereum blockchain
- Web3.js already included in your HTML (via CDN)

---

## 🛠️ Deployment Steps

### 1. Start Ganache

- Launch Ganache and start a new workspace.
- Copy the **private key** of one account (this will be the **admin**).
- Note the **RPC URL** (e.g., `http://127.0.0.1:7545`).

### 2. Setup MetaMask

- Open MetaMask.
- Import the **admin** account using the private key from Ganache.
- Add a custom network in MetaMask with Ganache's RPC URL.
- Select this account in MetaMask to use for deploying.

### 3. Compile & Deploy `Review.sol`

- Open [Remix IDE](https://remix.ethereum.org/).
- Paste the `Review.sol` smart contract in a new file.
- Set the compiler version to **0.8.14**.
- Compile the contract.
- Go to the **"Deploy & Run Transactions"** tab:
  - Set the **Environment** to `Injected Web3`.
  - Choose the Ganache-imported admin account from MetaMask.
  - Click **Deploy**.

---

## 📥 Integrate with Frontend (Important)

After successful deployment in Remix:

### 🔹 Copy ABI

1. Go to the **"Compilation" tab**.
2. Scroll down the compiling tab left side and on the bottom we can find abi code
3. ![image](https://github.com/user-attachments/assets/9f121452-1d51-43e3-97d0-1e93d12fd7f1)

![image](https://github.com/user-attachments/assets/45e3c813-ec51-497d-9bdf-5bff32074463)


4. Click on the **"ABI" copy icon**.
5. Paste this into the `script.js` like this:
   ```js
   const contractABI = [PASTE_HERE];
6. And in Deployment Tab we can find copy address and paste in `script.js`


![image](https://github.com/user-attachments/assets/eb5741d6-ff96-4523-8516-ca781b58aa60)

And finally run it using open with `Live Server` in VS Code.

