# Foundry Smart Contract Lottery

This project implements a decentralized lottery (raffle) smart contract using Solidity and Foundry. It was built as part of the **Cyfrin Foundry Fundamentals** course and covers key concepts including contract deployment, testing, automation, and interaction with Chainlink VRF & Keepers (Automation).

## 🧠 Key Features

- Lottery smart contract with entrance fee
- Chainlink VRF for provable randomness
- Chainlink Automation for auto-execution
- Full suite of unit and integration tests
- Automated deployment and helper scripts
- Modular config for testnet/mainnet environments

## 🧪 Tech Stack

- [Foundry](https://book.getfoundry.sh/) - Smart contract development toolchain
- Solidity - Smart contract language
- Chainlink - VRF and Automation integrations
- Anvil - Local testnet
- Sepolia - Ethereum testnet

## 📂 Project Structure

```
.
├── src/                  # Smart contract source code
│   └── Raffle.sol
├── script/               # Deployment and interaction scripts
│   ├── DeployRaffle.s.sol
│   ├── HelperConfig.s.sol
│   └── Interactions.s.sol
├── test/                 # Unit and integration tests
│   ├── unit/
│   │   └── RaffleTest.t.sol
│   ├── intergration/
│   │   └── Integrations.t.sol
│   └── Mocks/
│       └── LinkToken.sol
├── lib/                  # Submodules (Chainlink, Forge Std, Solmate, etc.)
├── foundry.toml          # Foundry config file
├── Makefile              # Automation commands
├── .gitmodules           # Submodule declarations
└── README.md             # You're here!
```

## 🚀 Quick Start

### 1. Clone the repo and init submodules
```bash
git clone --recurse-submodules https://github.com/awflick/foundry-smart-contract-lottery-cu.git
cd foundry-smart-contract-lottery-cu
```

### 2. Install Foundry
```bash
curl -L https://foundry.paradigm.xyz | bash
foundryup
```

### 3. Build & Test
```bash
forge build
forge test
```

### 4. Run Scripts
```bash
forge script script/DeployRaffle.s.sol --broadcast --rpc-url $SEPOLIA_RPC_URL --private-key $PRIVATE_KEY
```

> 💡 Make sure you have `.env` variables set for RPC URL, private key, and Chainlink configs.

## 📖 Course Reference

This repository is part of the **[Cyfrin Foundry Fundamentals](https://github.com/PatrickAlphaC/foundry-fund-me-f23)** course taught by [Patrick Collins](https://github.com/PatrickAlphaC), designed to teach professional-grade smart contract development using Foundry.

## ✅ Todo / Ideas

- [ ] Add a front-end interface for raffle entry and status display
- [ ] Add time-based constraints on lottery draws
- [ ] Extend support to other networks (e.g., Polygon, Arbitrum)

## 📜 License

MIT License — free to use and modify for educational and personal projects.
