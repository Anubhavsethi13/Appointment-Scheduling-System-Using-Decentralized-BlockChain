# Appointment-Scheduling-System-Using-Decentralized-BlockChain
Decentralized Appointment Scheduling System

A blockchain-based appointment booking system built using Solidity, Hardhat, React.js, Node.js, MetaMask, and IPFS.
The project eliminates the limitations of traditional centralized scheduling systems by ensuring security, transparency, and immutability using blockchain smart contracts.

🚀 Project Overview

This project provides a decentralized platform where service providers can create appointment slots and clients can book them securely.
All core logic—slot creation, booking, conflict detection, and cancellation—is handled by smart contracts deployed on an Ethereum-compatible blockchain (e.g., Hardhat local network or Polygon testnet).

Sensitive appointment metadata is stored securely on IPFS, while only the CID is stored on-chain to maintain privacy and reduce gas costs.

🛠️ Tech Stack
Blockchain & Contracts

Solidity

Hardhat

Ethers.js

OpenZeppelin Libraries

Frontend

React.js

MetaMask Integration

Axios

Backend

Node.js

Express.js

NFT.Storage / Pinata for IPFS uploads

Other Tools

IPFS

Mocha & Chai (Testing)

Visual Studio Code

Git & GitHub

📁 Project Structure
blockchain-scheduler/
├── contracts/
│   └── AppointmentScheduler.sol
├── scripts/
│   └── deploy.js
├── test/
│   └── scheduler.test.js
├── frontend/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── AppointmentABI.json
│   │   └── components/
│   └── package.json
├── backend/
│   ├── index.js
│   ├── package.json
│   └── .env (ignored)
├── hardhat.config.js
├── package.json
└── README.md

⚙️ Installation & Setup
1. Clone the Repository
git clone https://github.com/yourusername/blockchain-scheduler.git
cd blockchain-scheduler

2. Install Root Dependencies
npm install

3. Compile Smart Contracts
npx hardhat compile

4. Run Local Blockchain (Hardhat Node)
npx hardhat node


Copy one of the private keys printed in the terminal and import it into MetaMask.
RPC: http://127.0.0.1:8545 │ Chain ID: 31337

5. Deploy Contract Locally

In a new terminal:

npx hardhat run scripts/deploy.js --network localhost


Copy the deployed contract address.

6. Backend Setup (IPFS Upload Service)
cd backend
npm install


Create a .env file:

NFT_STORAGE_API_KEY=your_api_key
PORT=5001


Run backend:

node index.js

7. Frontend Setup
cd frontend
npm install


Copy ABI:

cp ../artifacts/contracts/AppointmentScheduler.sol/AppointmentScheduler.json ./src/AppointmentABI.json


Update contract address in App.jsx:

const CONTRACT_ADDRESS = "your_deployed_contract_address";


Run frontend:

npm start

🧪 Running Tests
npx hardhat test

🌐 Deploying to Polygon Mumbai Testnet
Add variables to .env:
MUMBAI_RPC_URL=https://polygon-mumbai.infura.io/v3/YOUR_KEY
PRIVATE_KEY=0xYOUR_TEST_PRIVATE_KEY


Deploy:

npx hardhat run scripts/deploy.js --network mumbai

🔐 Security Features

Smart contract controls slot creation & booking

Tamper-proof blockchain ledger

No central authority

Off-chain encrypted storage via IPFS

Smart contract enforced rules (no double booking)

📌 Key Features

Decentralized scheduling

Provider slot creation

Client booking system

Smart contract automation

IPFS metadata handling

Web-based UI with wallet integration

📸 Screenshots

(Add your own screenshots here)

🤝 Contributing

Pull requests are welcome.
For major changes, open an issue first to discuss the proposed updates.

📄 License

MIT License © 2025

⭐ Support the Project

If you found this project helpful, consider giving it a ⭐ on GitHub!
