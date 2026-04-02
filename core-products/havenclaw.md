# HavenClaw

> AI execution engine — translating natural language into cross-chain strategy deployment.

---

## What is HavenClaw?

HavenClaw is Haven's primary AI agent interface. It accepts natural language strategy descriptions, parses intent, and generates executable on-chain operations — all within seconds.

It connects directly to the **OpenClaw** agent framework to leverage tool-calling, multi-chain state awareness, and real-time yield data aggregation.

{% hint style="info" %}
HavenClaw understands DeFi-native language. You can say _"chase the best stable yield, avoid Curve"_ and it will accurately translate that into a set of protocol exclusions and allocation preferences.
{% endhint %}

---

## Key Features

| Feature | Details |
|---|---|
| Natural language input | Plain English strategy descriptions → machine-executable allocations |
| Cross-chain awareness | Unified view across Ethereum, Arbitrum, Base, and more |
| Auto-rebalancing | Drift-triggered or time-based portfolio rebalancing |
| Strategy templates | Pre-built strategies for common yield profiles |
| Execution simulation | Preview gas costs and expected outcomes before confirming |

---

## How It Works

### 1. Parse Intent
Your natural language input is processed by the HavenClaw AI model to extract yield targets, risk preferences, and protocol preferences.

### 2. Fetch Live Data
HavenClaw queries live APY data, liquidity depth, and HavenScore risk ratings across all supported protocols.

### 3. Generate Allocation Plan
An optimal allocation is calculated and presented for user confirmation, with simulated outcomes and gas estimates.

### 4. Execute On-chain
Upon confirmation, HavenClaw submits the transaction bundle across chains via the cross-chain router.

---

## Example

```
// Input prompt
"Maximize stablecoin yield with low risk.
 Prefer T-Bill exposure where APY > 4.5%.
 Auto-compound daily, rebalance if drift > 5%."

// Generated strategy
{
  "strategy": "Conservative Fixed Income",
  "allocations": {
    "T-Bills (tokenized)": "55%",
    "USDC lending":        "30%",
    "delta-neutral LP":    "15%"
  },
  "rebalance_trigger": "5% drift",
  "compound_freq":     "daily",
  "estimated_apy":     "6.2–7.8%"
}
```

---

## Related

* [HavenScore — Risk monitoring for every position](havenscore.md)
* [OpenClaw Framework — The agent layer powering HavenClaw](../integration/openclaw.md)
* [Quick Start — Deploy your first strategy](../getting-started/quickstart.md)
