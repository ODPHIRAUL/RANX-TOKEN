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

This Markdown file is now fully consistent and ready to be uploaded as a `README.md` to your GitHub repository. Let me know if you’d like additional sections or edits!
