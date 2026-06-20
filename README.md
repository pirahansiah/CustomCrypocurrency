# Custom Cryptocurrency

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.x-000000?logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A custom cryptocurrency implementation with blockchain, Flask web interface, and node-to-node communication.

## Overview

A proof-of-concept cryptocurrency ("GymCoin") demonstrating blockchain fundamentals including cryptographic hashing, digital signatures, transaction validation, and peer-to-peer node communication.

## Architecture

```
┌─────────────┐     ┌─────────────┐
│   Node 1    │◄───►│   Node 2    │
│  (run.py)   │     │  (run2.py)  │
└──────┬──────┘     └──────┬──────┘
       │                   │
       ▼                   ▼
┌──────────────────────────────────┐
│         Flask Web UI             │
│      (gymcoin/templates/)        │
├──────────────────────────────────┤
│         Blockchain Core          │
│    (gymcoin/blockchain.py)       │
│  • SHA-256 Hashing               │
│  • RSA Digital Signatures        │
│  • Proof of Work Consensus       │
│  • Transaction Validation        │
└──────────────────────────────────┘
```

## Key Components

| Component | File | Description |
|-----------|------|-------------|
| **Blockchain** | `gymcoin/blockchain.py` | Core blockchain with mining, transactions, proof-of-work |
| **Models** | `gymcoin/models.py` | Data models for blocks, transactions, wallets |
| **Routes** | `gymcoin/routes.py` | Flask API endpoints |
| **Forms** | `gymcoin/forms.py` | Web interface forms |
| **Storage** | `gymcoin/storage.py` | Persistent data storage |

## Modern Blockchain Landscape (2025-2026)

### Current Technologies

| Technology | Description | Maturity |
|------------|-------------|----------|
| **Ethereum 2.0 (Dencun)** | Proof-of-Stake with proto-danksharding | Production |
| **Solana** | High-throughput L1 with 65K TPS | Production |
| **Polygon zkEVM** | Zero-knowledge rollup for Ethereum | Production |
| **Bitcoin Lightning** | Layer-2 payment channels | Production |
| **Cosmos SDK** | Interoperable blockchain framework | Production |

### Modern Development Tools

- **[Hardhat](https://hardhat.org/)** — Ethereum development environment with debugging
- **[Foundry](https://github.com/foundry-rs/foundry)** — Fast, portable toolkit for smart contract development (2024+)
- **[Anchor](https://www.anchor-lang.com/)** — Solana program framework
- **[Ethers.js v6](https://docs.ethers.org/)** — Modern Ethereum JavaScript library
- **[Web3.py](https://web3py.readthedocs.io/)** — Python Ethereum library
- **[Substrate](https://substrate.io/)** — Rust-based blockchain SDK by Parity
- **[Hyperledger Fabric](https://www.hyperledger.org/)** — Enterprise permissioned blockchain

### Blockchain in 2025-2026

- **DePIN** — Decentralized Physical Infrastructure Networks
- **RWA Tokenization** — Real-world asset tokenization (BlackRock BUIDL fund)
- **Zero-Knowledge Proofs** — zk-SNARKs, zk-STARKs for privacy and scalability
- **Account Abstraction (ERC-4337)** — Smart contract wallets with gas sponsorship
- **AI + Blockchain** — Decentralized AI training, on-chain inference verification

## Quick Start

```bash
# Install dependencies
pip install flask cryptography

# Run two nodes
python run.py    # Node 1 (port 80)
python run2.py   # Node 2 (port 81)
```

## References

- Nakamoto, S. (2008). Bitcoin: A Peer-to-Peer Electronic Cash System.
- Wood, G. (2014). Ethereum: A Secure Decentralised Generalised Transaction Ledger.
- Buterin, V. (2023). Ethereum Roadmap: The Surge, Verge, Purge, and Splurge.

## Author

**Dr. Farshid Pirahansiah** — [LinkedIn](https://linkedin.com/in/pirahansiah) | [GitHub](https://github.com/pirahansiah)
