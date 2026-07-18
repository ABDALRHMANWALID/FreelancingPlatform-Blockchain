# Decentralized Freelancing Platform

> A decentralized application (dApp) that enables clients and freelancers to collaborate through secure on-chain escrow payments, eliminating the need for a centralized intermediary.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Solidity](https://img.shields.io/badge/Solidity-0.8.x-363636?logo=solidity)
![Foundry](https://img.shields.io/badge/Foundry-Framework-orange)
![Next.js](https://img.shields.io/badge/Next.js-15-black?logo=next.js)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5.x-3178C6?logo=typescript)
![Wagmi](https://img.shields.io/badge/Wagmi-v2-red)
![Viem](https://img.shields.io/badge/Viem-Latest-purple)

---

## 📖 Overview

This project is a decentralized freelancing marketplace where clients can hire freelancers securely using blockchain technology.

Instead of relying on a centralized platform to manage payments, funds are locked inside an escrow smart contract and released only after the client approves the submitted work. Every critical action is recorded on-chain, providing transparency, security, and trust between participants.

The project is intended as a complete learning resource for building production-ready Web3 applications using modern development tools and best practices.

---

## ✨ Features

### Client

* Connect wallet
* Create freelance jobs
* Set project budget and deadline
* Review freelancer proposals
* Accept a proposal
* Deposit funds into escrow
* Review submitted work
* Approve work
* Release payment
* Cancel open jobs
* Raise disputes

### Freelancer

* Connect wallet
* Browse available jobs
* Submit proposals
* Track proposal status
* Submit completed work
* Receive escrow payments
* Build an on-chain reputation

### Platform

* Escrow-based payments
* Transparent on-chain transactions
* Reputation system
* Treasury management
* Event-driven architecture
* Secure payment workflow
* Dispute resolution

---

# 🏗️ Project Structure

```text
.
├── smart-contract/
├── frontend/
├── docs/
├── README.md
└── .gitignore
```

---

# 📁 Smart Contract Structure

```text
smart-contract/

├── src/
│   ├── FreelancePlatform.sol
│   ├── Escrow.sol
│   ├── Treasury.sol
│   ├── Reputation.sol
│   │
│   ├── interfaces/
│   │      IFreelancePlatform.sol
│   │
│   └── libraries/
│          Errors.sol
│          Events.sol
│          Types.sol
│
├── script/
│      Deploy.s.sol
│      Interaction.s.sol
│
├── test/
│      FreelancePlatform.t.sol
│      Escrow.t.sol
│      Treasury.t.sol
│
├── foundry.toml
└── remappings.txt
```

---

# 💻 Frontend Structure

```text
frontend/

src/

├── app/
│   ├── page.tsx
│   ├── layout.tsx
│   ├── jobs/
│   ├── dashboard/
│   ├── profile/
│   ├── create-job/
│   └── applications/
│
├── components/
├── providers/
├── hooks/
├── contracts/
├── lib/
├── services/
├── config/
├── actions/
├── types/
├── assets/
└── styles/
```

---

# 📦 Smart Contracts

## FreelancePlatform.sol

The main contract responsible for:

* Creating jobs
* Managing proposals
* Selecting freelancers
* Tracking the job lifecycle
* Creating escrow agreements

---

## Escrow.sol

Responsible for securely holding client funds.

### Responsibilities

* Accept deposits
* Lock funds
* Release payments
* Refund clients
* Handle disputes

---

## Reputation.sol

Maintains freelancer statistics.

* Reputation score
* Completed jobs
* Success rate
* Total earnings

---

## Treasury.sol

Collects platform fees.

---

# 🔄 Workflow

```text
Client
   │
   ▼
Create Job
   │
   ▼
Job Open
   │
   ▼
Freelancers Apply
   │
   ▼
Client Selects Freelancer
   │
   ▼
Funds Locked in Escrow
   │
   ▼
Freelancer Submits Work
   │
   ▼
Client Reviews
   │
 ┌───────────────┐
 │               │
 ▼               ▼
Approve      Raise Dispute
 │               │
 ▼               ▼
Release      Arbitration
 │               │
 └───────┬───────┘
         ▼
      Completed
```

---

# 📡 Events

* JobCreated
* ProposalSubmitted
* ProposalAccepted
* EscrowFunded
* WorkSubmitted
* PaymentReleased
* JobCancelled
* RefundIssued
* DisputeRaised
* DisputeResolved

---

# 🔐 Security

* ReentrancyGuard
* Ownable
* Access Control
* Custom Errors
* Checks-Effects-Interactions Pattern
* Pull Payment Pattern
* Pausable (Optional)

---

# 🧪 Testing

Implemented using **Foundry**.

The test suite covers:

* Job creation
* Proposal submission
* Proposal acceptance
* Escrow funding
* Work submission
* Payment release
* Refunds
* Disputes
* Unauthorized access
* Event emission
* Reentrancy protection

---

# ⚙️ Tech Stack

## Blockchain

* Solidity
* Foundry
* OpenZeppelin

## Frontend

* Next.js (App Router)
* React
* TypeScript
* Tailwind CSS
* Shadcn/ui
* Wagmi
* Viem
* RainbowKit
* TanStack Query
* React Hook Form
* Zod

## Development

* Anvil
* Forge
* Cast
* Sepolia Testnet

---

# 🚀 Getting Started

## Clone the repository

```bash
git clone <repository-url>

cd <repository-folder>
```

---

## Install Smart Contract Dependencies

```bash
cd smart-contract

forge install

forge build
```

---

## Start Local Blockchain

```bash
anvil
```

---

## Deploy Contracts

```bash
forge script script/Deploy.s.sol \
--rpc-url http://127.0.0.1:8545 \
--broadcast
```

---

## Install Frontend Dependencies

```bash
cd frontend

npm install
```

---

## Start the Development Server

```bash
npm run dev
```

---

# 🛣️ Roadmap

## Version 1

* Wallet connection
* Create jobs
* Submit proposals
* Escrow payments
* Work submission
* Payment release

## Version 2

* Milestone-based payments
* ERC20 support
* Ratings & Reviews
* Notifications
* IPFS integration
* User profiles

## Version 3

* DAO arbitration
* The Graph integration
* Multi-signature dispute resolution
* Analytics dashboard
* Mobile optimization

---

# 🎯 Learning Objectives

This project demonstrates:

* Smart Contract Development
* Solidity Best Practices
* Foundry Framework
* Smart Contract Testing
* Smart Contract Security
* Next.js App Router
* Wagmi & Viem Integration
* Wallet Authentication
* Event-driven dApps
* Escrow Systems
* Modern Web3 Architecture

---

# 🤝 Contributing

Contributions, feature requests, and improvements are welcome. Feel free to open an issue or submit a pull request.

---

# 📄 License

Licensed under the **MIT License**.
