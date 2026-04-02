# Unified Yield Gateway

> A single interface for accessing T-Bills, liquidity pools, and delta-neutral strategies.

---

## Overview

The Unified Yield Gateway is the access layer connecting users to Haven's full range of yield strategies — spanning both DeFi and TradFi fixed-income markets — from a single interface.

No need to navigate multiple protocols, manage separate wallets, or track positions across chains manually. Haven aggregates it all.

---

## Supported Strategy Types

### 📄 T-Bills (Tokenized RWA)
Access U.S. Treasury Bill yields through tokenized RWA wrappers. The lowest-risk option in Haven's strategy suite — stable, predictable, and backed by U.S. government obligations.

- **Risk tier:** Low
- **Typical APY:** 4.5–5.5%
- **Best for:** Capital preservation, institutional allocation

### 💧 Liquidity Pools (DeFi)
Stablecoin and low-volatility lending pools across major protocols including Aave, Compound, and Morpho.

- **Risk tier:** Low–Medium
- **Typical APY:** 5–9%
- **Best for:** Yield maximization within stablecoin exposure

### ⚖️ Delta-Neutral Strategies (Quant)
Market-neutral strategies that earn funding rates and basis spreads regardless of price direction. Built for users seeking higher yield without directional crypto exposure.

- **Risk tier:** Medium–High
- **Typical APY:** 8–15%
- **Best for:** Sophisticated users, yield optimization

### 🗂 Blended Portfolios (Structured)
Pre-constructed allocations combining all strategy types with defined risk/return profiles. Managed autonomously by HavenClaw with HavenScore monitoring.

---

## Supported Assets

| Asset | Type | Avg APY | Risk Tier |
|---|---|---|---|
| USDC | Stablecoin | 5–8% | ✅ Low |
| USDT | Stablecoin | 5–7% | ✅ Low |
| Tokenized T-Bills | RWA | 4.5–5.5% | ✅ Low |
| DAI / sDAI | Stablecoin | 6–9% | 🔵 Medium |
| Delta-Neutral Positions | Structured | 8–15% | ⚠️ Medium-High |

---

## Supported Chains

* Ethereum Mainnet
* Arbitrum
* Base
* Optimism

Additional chains planned for Phase 4 — see [Roadmap](../resources/roadmap.md).

---

## Related

* [HavenClaw — How strategies are executed](havenclaw.md)
* [HavenScore — Risk scoring per protocol](havenscore.md)
* [Quick Start — Deploy your first strategy](../getting-started/quickstart.md)
