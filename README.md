# Fanora L1 - Privacy-First Layer-1 Blockchain for Regulated Finance

**Fanora L1** is a production-ready Layer-1 blockchain built on Avalanche Subnets, designed specifically for regulated stablecoins, cross-border payments, and institutional treasury operations. It combines privacy-preserving technology with regulatory compliance through validator governance and audit hooks.

## 🌟 Key Features

- **Privacy-First Architecture**: Encrypted transactions, stealth addresses, and pluggable zero-knowledge primitives
- **Regulatory Compliance**: Validator governance, transaction freeze/pause capabilities, and comprehensive audit hooks
- **Snowman Consensus**: Leverages Avalanche's battle-tested consensus with permissioned validators
- **Institutional Grade**: Built for treasury operations, cross-border payments, and regulated stablecoin issuance
- **Modular Design**: Clean separation of concerns across runtime, consensus, crypto, mempool, and governance

## 🏗️ Architecture

```
Fanora-L1/
├── runtime/        # Core state machine and transaction processing
├── consensus/      # Snowman consensus adapter with governance hooks
├── crypto/         # Privacy primitives (stealth addresses, encrypted tx, ZK)
├── mempool/        # Encrypted transaction gossip and ordering
├── governance/     # On-chain proposals, voting, and validator management
├── cli/            # TypeScript CLI and SDK for node management
├── subnet/         # Avalanche subnet configuration and VM specs
├── docs/           # Comprehensive documentation
└── tests/          # End-to-end integration tests
```

## 🚀 Quick Start

### Prerequisites

- Rust 1.75+ and Cargo
- Node.js 18+ and npm
- Avalanche CLI (for subnet deployment)

### Installation

```bash
# Clone the repository
git clone https://github.com/your-org/fanora-l1.git
cd fanora-l1

# Build the runtime and consensus modules
cd runtime && cargo build --release
cd ../consensus && cargo build --release
cd ../crypto && cargo build --release
cd ../mempool && cargo build --release
cd ../governance && cargo build --release

# Install CLI tools
cd ../cli
npm install
npm run build
```

### Running a Validator Node

```bash
# Initialize node configuration
./cli/dist/index.js init --validator

# Start the node
./cli/dist/index.js start --config ./node-config.json
```

### Sending a Private Transaction

```bash
# Generate stealth address
./cli/dist/index.js crypto generate-stealth

# Send encrypted transaction
./cli/dist/index.js tx send \
  --to <stealth-address> \
  --amount 1000 \
  --encrypted \
  --private-key <your-key>
```

## 📚 Documentation

- [Architecture Overview](./docs/architecture.md)
- [Consensus Mechanism](./docs/consensus.md)
- [Privacy & Cryptography](./docs/privacy.md)
- [Governance System](./docs/governance.md)
- [Stablecoin Roadmap](./docs/stablecoin-roadmap.md)
- [CLI Reference](./docs/cli-usage.md)

## 🧪 Testing

```bash
# Run unit tests for all modules
cargo test --workspace

# Run end-to-end tests
cd tests
npm install
npm test
```

## 🛣️ Roadmap

### Phase 1: MVP (Current)
- ✅ Core runtime with encrypted transactions
- ✅ Snowman consensus integration
- ✅ Basic governance (proposals & voting)
- ✅ CLI for node management
- ✅ Stealth addresses and encrypted transactions

### Phase 2: Privacy Enhancement (Q1 2026)
- 🔄 Full zero-knowledge proof integration
- 🔄 Advanced stealth address schemes
- 🔄 Confidential asset transfers

### Phase 3: Stablecoin Infrastructure (Q2 2026)
- 📋 Multi-currency stablecoin support
- 📋 Regulatory compliance modules
- 📋 Cross-border payment rails

### Phase 4: Institutional Features (Q3 2026)
- 📋 Multi-signature treasury management
- 📋 Advanced audit and reporting tools
- 📋 Enterprise SDK and integrations

## 🔐 Security

Fanora L1 implements multiple layers of security:

- **Cryptographic Privacy**: Schnorr signatures, stealth addresses, encrypted transaction payloads
- **Consensus Security**: Permissioned validators with stake-based selection
- **Governance Controls**: On-chain freeze/pause mechanisms for emergency response
- **Audit Trail**: Comprehensive logging with privacy-preserving audit hooks

## 🤝 Contributing

We welcome contributions! Please see our [Contributing Guide](./CONTRIBUTING.md) for details.

## 📄 License

This project is licensed under the Apache 2.0 License - see the [LICENSE](./LICENSE) file for details.

## 🔗 Links

- [Website](https://fanora-l1.io)
- [Documentation](https://docs.fanora-l1.io)
- [Discord Community](https://discord.gg/fanora-l1)
- [Twitter](https://twitter.com/fanora_l1)

## 📞 Contact

For enterprise inquiries: enterprise@fanora-l1.io  
For technical support: support@fanora-l1.io

---

**Built with ❤️ for the future of regulated decentralized finance**
