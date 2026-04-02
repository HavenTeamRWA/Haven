# Architecture

Haven is built as a modular AI-native protocol. Each layer is independently upgradeable, enabling rapid iteration without compromising security.

---

## System Layers

```
┌─────────────────────────────────────────────────────┐
│                   Interface Layer                    │
│      HavenClaw NL Interface · HavenSkill · Web App  │
└───────────────────────┬─────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│                  AI Agent Layer                      │
│    OpenClaw Framework · HavenScore · Strategy Engine │
└───────────────────────┬─────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│                  Execution Layer                     │
│  Cross-chain Router · Smart Contract Vault · Rebalancer │
└───────────────────────┬─────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────┐
│                  Protocol Layer                      │
│   T-Bill RWA · Liquidity Pools · Delta-Neutral Strategies │
└─────────────────────────────────────────────────────┘
```

---

## Layer Descriptions

### Interface Layer
The entry point for all users and developers. Includes the HavenClaw natural language interface, the HavenSkill OpenClaw module, and the web application dashboard.

### AI Agent Layer
The intelligence core of the protocol. OpenClaw provides the agent reasoning framework; HavenScore provides real-time risk signals; the Strategy Engine generates and optimizes allocation plans.

### Execution Layer
Handles on-chain operations. The cross-chain router coordinates multi-chain transactions; the Smart Contract Vault holds user assets non-custodially; the Rebalancer executes drift-triggered or time-based portfolio adjustments.

### Protocol Layer
The underlying yield-generating integrations — tokenized T-Bills, DeFi liquidity pools, and delta-neutral structured strategies.

---

## Security Model

All smart contracts are **non-custodial**. Users retain ownership of funds at all times. Strategy execution happens through permissioned vault contracts that can be revoked at any time.

| Component | Audit Status | Auditor |
|---|---|---|
| Core Vault Contract | ✅ Audited | TBD |
| Cross-chain Router | 🔄 In Progress | TBD |
| OpenClaw Agent Interface | 🔵 Internal Review | Internal |

---

## Next Steps

* [HavenClaw — Execution Engine](../core-products/havenclaw.md)
* [HavenScore — Risk Intelligence](../core-products/havenscore.md)
* [OpenClaw Framework](../integration/openclaw.md)
