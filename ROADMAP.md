# ROADMAP.md — CustomCrypocurrency (GymCoin)

## 12-Month Vision

Transform GymCoin from an educational proof-of-concept into a production-ready blockchain platform with modern cryptographic standards, scalable architecture, and cross-platform deployment.

### Q1: Foundation (Months 1–3)
- **Python 3.10+ migration** — Update all dependencies, replace deprecated APIs, add type hints throughout
- **Cryptography hardening** — Migrate from raw RSA to ECDSA (secp256k1), implement proper digital signatures replacing the current placeholder signature system
- **Transaction validation overhaul** — Fix the `hasValidTransactions()` bug (only validates first tx), add balance verification before transaction acceptance
- **Unit test suite** — Achieve >80% coverage on blockchain core, transaction validation, and mining logic
- **CI/CD pipeline** — GitHub Actions with automated testing, linting (ruff), and type checking (mypy)

### Q2: Security & Performance (Months 4–6)
- **Merkle tree transaction verification** — Replace linear transaction hashing with Merkle root computation for O(log n) verification
- **Memory pool optimization** — Implement priority queue for pending transactions, add transaction expiration
- **WebSocket node communication** — Replace HTTP polling with WebSocket connections for real-time chain updates
- **Rate limiting & DoS protection** — Implement request throttling on API endpoints, add block size limits
- **Encrypted peer communication** — TLS/HTTPS for all inter-node REST API calls

### Q3: Features & Scalability (Months 7–9)
- **Smart contract skeleton** — Basic scripting engine for programmable transactions
- **Wallet system** — HD wallet generation (BIP-32/39), multi-address support per user
- **Transaction fee market** — Dynamic fee calculation based on block utilization
- **Docker deployment** — Containerized node deployment with docker-compose for multi-node orchestration
- **Prometheus/Grafana monitoring** — Metrics collection for block time, tx throughput, node health

### Q4: Production Readiness (Months 10–12)
- **Consensus algorithm upgrade** — Transition from longest-chain to weighted Proof-of-Stake hybrid
- **Cross-platform builds** — Native packages for Linux, macOS, Windows with conda/pyinstaller
- **REST API versioning** — v2 API with OpenAPI/Swagger documentation
- **Performance benchmarks** — Automated benchmarking suite targeting 500+ TPS sustained throughput
- **Documentation & onboarding** — Comprehensive developer docs, architecture diagrams, contribution guidelines

## Technical Debt

| Priority | Item | Impact | Effort |
|----------|------|--------|--------|
| **Critical** | `hasValidTransactions()` only validates first transaction in block | Security vulnerability | Low |
| **Critical** | Signature system uses placeholder `"made"` instead of real cryptographic verification | Security vulnerability | Medium |
| **Critical** | Hardcoded Flask SECRET_KEY in `__init__.py` | Security vulnerability | Low |
| **High** | `console.log("error 5")` JavaScript call in Python code (`blockchain.py:130`) | Runtime error | Low |
| **High** | `storage.py` contains orphaned duplicate of `resolveConflicts` | Code duplication | Low |
| **High** | No CSRF protection on API endpoints | Security gap | Medium |
| **Medium** | String-based node identifiers instead of proper P2P addressing | Scalability | Medium |
| **Medium** | No block size limit enforcement in mining | Performance | Low |
| **Medium** | `private.pem` and `receiver.pem` committed to repository | Security risk | Low |
| **Low** | Inconsistent naming conventions (camelCase vs snake_case) | Code quality | Medium |
| **Low** | No `__init__.py` type stubs or mypy configuration | Developer experience | Medium |
| **Low** | `__pycache__` directories committed | Repository hygiene | Low |

## Future Features

1. **Zero-Knowledge Proof Transactions** — Implement zk-SNARKs for private transactions that verify without revealing sender/receiver/amount
2. **Layer-2 Payment Channels** — Off-chain transaction channels for high-throughput micro-transactions
3. **Governance Token System** — On-chain voting for protocol parameter changes (difficulty, block size, rewards)
4. **Cross-Chain Bridge** — Interoperability layer connecting GymCoin to Ethereum testnets via relay contracts
5. **Mobile Wallet App** — React Native or Flutter wallet with QR code scanning for transaction initiation
6. **Staking Dashboard** — Delegated Proof-of-Stake interface for token holders to earn yield
7. **NFT Minting Module** — Non-fungible token creation and marketplace for digital assets
8. **AI-Powered Anomaly Detection** — Machine learning model for identifying fraudulent transaction patterns
9. **Hardware Wallet Integration** — Ledger/Trezor support for cold storage key management
10. **Lightning Network Equivalent** — Channel-based payment routing for instant settlements
