# RANX DAO Token

RANX DAO Token is a decentralized governance and utility token developed on the Avalanche blockchain. This repository contains the smart contract code and documentation for implementing the RANX DAO token, including tokenomics, staking, and governance functionality.

---

## Table of Contents

- [Overview](#overview)
- [Tokenomics](#tokenomics)
- [Features](#features)
- [Development Timeline](#development-timeline)
- [Environment Setup](#environment-setup)
- [Smart Contract Structure](#smart-contract-structure)
- [Deployment Guide](#deployment-guide)
- [Future Phases](#future-phases)
- [Contributing](#contributing)
- [License](#license)

---

## Overview

The **RANX DAO Token** serves as a governance and utility token, allowing users to:

- Participate in decentralized governance via voting.
- Stake tokens to earn rewards.
- Access additional utilities and premium features in future phases.

This token is built on Avalanche using **Rust** and deployed using Avalanche's **Subnet-EVM**.

---

## Tokenomics

- **Total Supply**: 1 billion tokens.
- **Allocation**:
  - 30%: Staking rewards.
  - 20%: Governance incentives.
  - 20%: Public and private sales.
  - 15%: Team and advisors (vesting over 4-5 years).
  - 15%: Reserve for future use.

- **Burn Mechanism**: A 0.2%-0.5% burn per transaction to reduce supply and increase scarcity over time.

---

## Features

### Governance
- Token holders can vote on proposals and influence platform decisions.
- Quadratic voting to ensure balanced representation.
- Proposals require a minimum stake to be created and voted upon.

### Staking
- Stake tokens to earn rewards.
- Rewards distributed proportionally based on staked tokens.

### Supply Control
- Minting and burning mechanisms implemented to manage token supply effectively.

---

## Development Timeline

### **Phase 1: Token Development**

| **Day** | **Tasks**                                                    | **Hours** |
|---------|--------------------------------------------------------------|-----------|
| Day 1   | Environment setup, tokenomics definition, and project setup. | 7         |
| Day 2   | Develop token contract and governance logic.                 | 7         |
| Day 3   | Implement staking contract and integration.                  | 7         |
| Day 4   | Create Avalanche subnet and deploy contracts to testnet.     | 7         |
| Day 5   | Perform integration testing and deploy to mainnet.           | 7         |
| Day 6   | Write documentation and prepare presentation.                | 7         |

---

### Week 1
- **Day 1**: Environment setup and planning.
- **Day 2**: Token contract development.
- **Day 3**: Staking logic and governance integration.

### Week 2
- **Day 4**: Subnet creation and testnet deployment.
- **Day 5**: Final testing and mainnet deployment.
- **Day 6**: Documentation and presentation preparation.

---

## Environment Setup

1. **Install Avalanche CLI**:
   ```bash
   npm install -g avalanche
   ```

2. **Install Rust**:
   ```bash
   curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
   ```

3. **Install AvalancheGo Node**:
   ```bash
   wget https://github.com/ava-labs/avalanchego/releases/latest/download/avalanchego-linux-amd64.tar.gz
   tar -xvf avalanchego-linux-amd64.tar.gz
   ./avalanchego
   ```

4. **Clone Repository**:
   ```bash
   git clone https://github.com/your-repo/ranx-dao.git
   cd ranx-dao
   ```

---

## Smart Contract Structure

### Token Contract (`token.rs`)
Implements core token functionalities:
- Minting
- Burning
- Transferring tokens.

### Governance Contract (`governance.rs`)
Defines:
- Proposal creation.
- Voting processes.
- Result tallying.

### Staking Contract (`staking.rs`)
Implements:
- Token staking.
- Reward calculation.
- Withdrawal mechanisms.

---

## **Project Structure**

```
ranx-dao/
├── src/
│   ├── token.rs         # Token logic (minting, burning, transfers)
│   ├── governance.rs    # Governance logic (proposals, voting)
│   ├── staking.rs       # Staking logic (rewards, withdrawals)
├── tests/
│   ├── token_tests.rs   # Unit tests for token contract
│   ├── governance_tests.rs # Unit tests for governance
│   ├── staking_tests.rs    # Unit tests for staking
├── Cargo.toml           # Project dependencies and metadata
└── README.md            # Documentation
```


## Deployment Guide

### Subnet Creation
1. Create a custom subnet:
   ```bash
   avalanche subnet create ranx_subnet
   ```

2. Configure and test the subnet locally.

### Testnet Deployment
1. Deploy contracts to the **Fuji Testnet**.
2. Verify functionality using **Avalanche Explorer**.

### Mainnet Deployment
1. Deploy final contracts on the **Avalanche Mainnet**:
   ```bash
   avalanche deploy ranx_subnet
   ```

2. Validate deployment via Avalanche tools and explorers.

---

## Future Phases

- **Phase 2**: Develop a frontend UI for token interactions (staking, governance, etc.).
- **Phase 3**: Expand token utility to integrate with additional platforms and applications.

---

## Contributing

We welcome contributions to enhance the RANX DAO Token. Please follow these steps:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes and push to your fork:
   ```bash
   git commit -m "Add feature"
   git push origin feature-name
   ```
4. Open a pull request.

---

## License

This project is licensed under the MIT License.
```

Here’s the entire `README.md` content in Markdown format for you to copy and paste:

```markdown
# RANX Project

The RANX Project is a decentralized system built on Avalanche's C-Chain, integrating governance, staking, a marketplace, and charity functionalities. This repository contains the smart contracts, deployment scripts, and tests for the RANX ecosystem.

## 📁 Folder Structure

```plaintext
RANX-Project/
├── contracts/
│   ├── RANXToken.sol         # Token contract (ERC-20 standard with governance features)
│   ├── StakingContract.sol   # Staking logic (tiers, rewards, penalties)
│   ├── Marketplace.sol       # Token-based purchases, donations, and burning mechanism
│   ├── Governance.sol        # Proposal creation, voting, and execution
│   ├── Charity.sol           # Charity-related functionality and donation tracking
│   └── interfaces/           # Shared interfaces for reusability
│       ├── IStaking.sol      # Interface for Staking Contract
│       ├── IMarketplace.sol  # Interface for Marketplace Contract
│       ├── ICharity.sol      # Interface for Charity Contract
│       └── IGovernance.sol   # Interface for Governance Contract
├── scripts/
│   ├── deploy.js             # Deployment script for all contracts
│   ├── deployToken.js        # Deployment script for RANX Token contract
│   ├── deployStaking.js      # Deployment script for Staking Contract
│   ├── deployMarketplace.js  # Deployment script for Marketplace Contract
│   ├── deployGovernance.js   # Deployment script for Governance Contract
│   ├── deployCharity.js      # Deployment script for Charity Contract
│   └── utils/                # Shared utilities for deployment and interaction
│       └── constants.js      # Constants like initial supply, addresses, etc.
├── test/
│   ├── RANXToken.test.js     # Unit tests for RANX Token contract
│   ├── StakingContract.test.js # Unit tests for Staking Contract
│   ├── Marketplace.test.js   # Unit tests for Marketplace Contract
│   ├── Governance.test.js    # Unit tests for Governance Contract
│   ├── Charity.test.js       # Unit tests for Charity Contract
│   └── integration.test.js   # Integration tests for contract interactions
├── artifacts/                # Compiled contracts (generated by Hardhat)
├── cache/                    # Cached files (generated by Hardhat)
├── node_modules/             # Node.js dependencies
├── hardhat.config.js         # Hardhat configuration file (networks, compiler, etc.)
├── package.json              # npm package file for dependencies
├── package-lock.json         # Lockfile for npm dependencies
├── README.md                 # Documentation for the project
├── .gitignore                # Ignore unnecessary files (e.g., node_modules, artifacts)
└── .env                      # Environment variables (e.g., private keys, RPC URLs)
```

## ⚙️ Setup Instructions

### Prerequisites
1. Install **Node.js** and **npm**.
2. Install **Hardhat** for Solidity development:
   ```bash
   npm install --save-dev hardhat
   ```

### Clone the Repository
```bash
git clone https://github.com/your-repo-url.git
cd RANX-Project
```

### Install Dependencies
```bash
npm install
```

### Configure Environment Variables
Create a `.env` file in the root directory and add the following:
```plaintext
PRIVATE_KEY=<your-private-key>
RPC_URL=https://api.avax.network/ext/bc/C/rpc
```

## 🚀 Deployment

To deploy all contracts on Avalanche's C-Chain, run:
```bash
npx hardhat run scripts/deploy.js --network avalanche
```

Deployment scripts for individual contracts are also available in the `scripts/` folder.

## 🧪 Testing

Run the unit and integration tests:
```bash
npx hardhat test
```

## 🛠️ Smart Contracts

### RANX Token Contract
- Implements the ERC-20 standard with governance features.
- Functions:
  - `mint(address to, uint256 amount)`
  - `burn(address from, uint256 amount)`
  - `transfer(address to, uint256 amount)`
  - `approve(address spender, uint256 amount)`
  - `balanceOf(address account)`

### Staking Contract
- Manages staking pools, rewards, and penalties.
- Functions:
  - `stake(uint256 amount, uint256 duration)`
  - `unstake(uint256 stakeId)`
  - `calculateRewards(address user)`
  - `penaltyCalculator(uint256 stakeId)`

### Marketplace Contract
- Handles token-based purchases, donations, and token burning.
- Functions:
  - `purchase(uint256 productId, uint256 amount)`
  - `donate(uint256 charityId, uint256 amount)`
  - `applyDiscount(uint256 userLifeRating)`

### Governance Contract
- Allows proposal creation, voting, and execution.
- Functions:
  - `submitProposal(string memory details, uint256 stakeAmount)`
  - `vote(uint256 proposalId, uint256 voteAmount, bool decision)`
  - `executeProposal(uint256 proposalId)`

### Charity Contract
- Facilitates donations and tracks donation history.
- Functions:
  - `donate(uint256 charityId, uint256 amount)`
  - `trackDonationHistory(address user)`
  - `fetchCharityDetails(uint256 charityId)`

## 📜 License
This project is licensed under the MIT License.

---

### 📧 Contact
For questions or contributions, reach out to the developers:

- **Daniel Doe**: [Your Email]
- **Pedro**: [Pedro's Email]
```

You can copy and paste this directly into your `README.md` file. Replace the placeholders with your actual details where needed!

This Markdown file is now fully consistent and ready to be uploaded as a `README.md` to your GitHub repository. Let me know if you’d like additional sections or edits!
