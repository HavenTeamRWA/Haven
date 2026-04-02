# OpenClaw Framework

> The AI agent execution framework powering Haven.

---

## What is OpenClaw?

OpenClaw is the AI agent framework that Haven is built on. It provides the infrastructure for tool-calling, multi-step reasoning, and cross-chain execution that makes autonomous yield management possible.

Developers can use OpenClaw to build their own AI-powered DeFi applications, leveraging Haven's yield and risk infrastructure as a skill layer via [HavenSkill](../core-products/havenskill.md).

{% hint style="info" %}
Haven is an official OpenClaw integration partner. HavenSkill is available in the OpenClaw skill registry and is maintained by the Haven team.
{% endhint %}

---

## OpenClaw + Haven Architecture

```
User Intent (Natural Language)
          ↓
OpenClaw Agent (reasoning + planning)
          ↓  calls skills
    ├── HavenSkill.query_yield_paths()
    ├── HavenSkill.score_protocol()
    └── HavenSkill.execute_strategy()
          ↓
HavenClaw Execution Engine
          ↓
On-chain smart contract execution
```

---

## Why OpenClaw?

| Capability | Description |
|---|---|
| Tool-calling | Agents can call external APIs and on-chain functions as structured tools |
| Multi-step reasoning | Complex strategies broken into sequential, verifiable steps |
| State awareness | Agent maintains context across multi-turn interactions |
| Composable skills | Modular skill registry — add Haven, remove Haven, combine with others |
| Cross-chain support | Native awareness of multi-chain execution environments |

---

## Building on OpenClaw + Haven

Any developer can build AI-native DeFi applications using OpenClaw as the agent layer and HavenSkill as the yield/risk data source.

**Use cases:**
- Autonomous treasury management for DAOs
- Yield-optimizing trading bots
- AI-driven portfolio rebalancers
- Risk-aware lending automation

→ See [HavenSkill](../core-products/havenskill.md) for installation and usage  
→ See [API Reference](api.md) for direct REST API access

---

## Related

* [HavenSkill — OpenClaw skill module](../core-products/havenskill.md)
* [API Reference](api.md)
