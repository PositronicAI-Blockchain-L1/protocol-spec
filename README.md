<div align="center">

<img src="logo.png" width="120" alt="Positronic">

# Positronic Protocol Specification

### Formal specification of the Positronic (ASF) Layer-1 protocol

[![Chain ID](https://img.shields.io/badge/Chain_ID-420420-00E5FF?style=for-the-badge)](https://positronic-ai.network)
[![Consensus](https://img.shields.io/badge/Consensus-PoNC-7c3aed?style=for-the-badge)](https://positronic-ai.network/whitepaper.html)
[![Status](https://img.shields.io/badge/Status-Living_Document-brightgreen?style=for-the-badge)]()

</div>

---

## Overview

This repository contains the formal protocol specification for the **Positronic (ASF)** blockchain — the world's first Layer-1 with AI-validated consensus.

The specification defines the rules, data structures, algorithms, and invariants that all compliant Positronic node implementations must follow.

## Specification Modules

| Module | Description | Status |
|--------|-------------|--------|
| **PSpec-001** | Block Header & Body Format | Final |
| **PSpec-002** | Transaction Encoding (PRC-TX) | Final |
| **PSpec-003** | Proof of Neural Consensus (PoNC) | Final |
| **PSpec-004** | DPoS v2 — Delegation & Elections | Final |
| **PSpec-005** | BFT Finality Gadget | Final |
| **PSpec-006** | AI Scoring Pipeline (TAD / MSAD / SCRA / ESG) | Final |
| **PSpec-007** | Slashing Conditions & Enforcement | Final |
| **PSpec-008** | PRC-20 Token Standard | Final |
| **PSpec-009** | PRC-721 NFT Standard | Final |
| **PSpec-010** | PRC-3643 RWA Tokenization | Final |
| **PSpec-011** | Cross-Chain Bridge Protocol | Final |
| **PSpec-012** | Decentralized Identity (W3C DID) | Final |
| **PSpec-013** | ZKML Proof System | Final |
| **PSpec-014** | Neural Self-Preservation | Final |
| **PSpec-015** | Post-Quantum Signatures (ML-DSA-44) | Final |
| **PSpec-016** | Gasless Meta-Transactions | Final |
| **PSpec-017** | AI Agent Marketplace Protocol | Final |
| **PSpec-018** | Emergency Governance System | Final |
| **PSpec-019** | FOCG Game Engine Protocol | Final |
| **PSpec-020** | TRUST Soulbound Token | Final |

## Chain Parameters

```
Chain ID .............. 420420
Symbol ................ ASF
Total Supply .......... 1,000,000,000 ASF (deflationary)
Block Time ............ ~12 seconds
Hash Algorithm ........ SHA-512
Signatures ............ Ed25519 + ML-DSA-44 (post-quantum)
Consensus ............. PoNC (AI) + DPoS v2 + BFT
Block Reward .......... 24 ASF
Fee Burn .............. 20% of all TX fees
Validators ............ Unlimited (21 producers/epoch)
Founder Pre-mine ...... 0 ASF
```

## Consensus Architecture

```
                    +-----------------------------+
                    |      Transaction Pool        |
                    +-------------+---------------+
                                  |
                    +-------------v---------------+
                    |   AI Validation Gate (PoNC)   |
                    |                               |
                    |  TAD --+                      |
                    |  MSAD -+-- Meta-Model -- Score|
                    |  SCRA -+                      |
                    |  ESG --+                      |
                    +-------------+---------------+
                                  |
               +------------------+----------------+
               |                  |                |
          Score < 0.85       0.85 - 0.95      Score > 0.95
          +----v----+       +----v-----+     +----v----+
          | ACCEPT  |       |QUARANTINE|     | REJECT  |
          +----+----+       +----------+     +---------+
               |
    +----------v------------------+
    |   DPoS v2 Block Production   |
    |   (21 elected producers)     |
    +----------+------------------+
               |
    +----------v------------------+
    |   BFT Finality (2/3 + 1)    |
    +-----------------------------+
```

## Tokenomics

| Allocation | Percentage |
|------------|-----------|
| Node Mining | 50% |
| Play-to-Mine | 20% |
| AI Treasury (DAO) | 15% |
| Community | 5% |
| Team (4-year vesting) | 5% |
| Security (Bug Bounty) | 5% |
| **Founder** | **0%** |

## Implementation Status

The reference implementation is written in Python with a native C extension for performance-critical cryptographic operations.

- **224 source modules**
- **7,123 passing tests** across 179 test files
- **213 RPC methods**
- **32 development phases** — all complete
- **5-round red team penetration testing** (312 attack tests)

## Contributing

Protocol improvement proposals can be submitted as issues in this repository. Major changes require governance approval through the on-chain DAO voting system.

## Links

| Resource | Link |
|----------|------|
| Website | [positronic-ai.network](https://positronic-ai.network) |
| Whitepaper | [Read](https://positronic-ai.network/whitepaper.html) |
| Litepaper | [Read](https://positronic-ai.network/litepaper.html) |
| API Docs | [213 Methods](https://positronic-ai.network/docs/) |
| Explorer | [Browse](https://positronic-ai.network/explorer/) |

---

<div align="center">

**Zero pre-mine. Zero VC. Code-driven, not hype-driven.**

*Positronic Network — AI-secured blockchain infrastructure.*

</div>
