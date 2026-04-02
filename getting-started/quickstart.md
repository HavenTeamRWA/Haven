# Quick Start

Get up and running with Haven in minutes. Connect your wallet, define your yield strategy, and let the AI handle the rest.

---

## Prerequisites

{% hint style="warning" %}
Make sure you have a Web3 wallet (MetaMask, Rabby, or WalletConnect-compatible) and USDC/USDT stablecoins to deposit before proceeding.
{% endhint %}

---

## Step 1 — Connect Your Wallet

Visit [haven.financial](https://www.haven.financial) and connect via MetaMask, Rabby, or any WalletConnect-supported wallet. Haven supports all major EVM chains including Ethereum mainnet, Arbitrum, Base, and Optimism.

---

## Step 2 — Define Your Risk Profile

Set your yield target and acceptable risk tier:

| Tier | Description | Typical APY |
|---|---|---|
| **Conservative** | T-Bills + stable lending only | 4.5–6% |
| **Balanced** | Mix of stable and structured strategies | 6–10% |
| **Aggressive** | Delta-neutral + higher-yield pools | 10–18% |

HavenScore will monitor all your positions in real time according to the tier you select.

---

## Step 3 — Describe Your Strategy

Use HavenClaw's natural language interface. You can type something like:

> _"Allocate 60% to T-Bills, 40% to stablecoin pools, rebalance weekly"_

Or choose from a pre-built strategy template in the dashboard.

**Example HavenClaw prompt and output:**

```
// Prompt
"Maximize stablecoin yield with low risk.
 Prefer T-Bill exposure where APY > 4.5%.
 Auto-compound daily, rebalance if drift > 5%."

// HavenClaw output
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

## Step 4 — Deposit and Activate

Approve the smart contract and deposit your assets. Haven's AI engine begins autonomous execution immediately.

You can monitor, adjust, or exit your position at any time from the dashboard.

---

## Next Steps

* [Learn how Haven's architecture works](architecture.md)
* [Deep dive into HavenClaw](../core-products/havenclaw.md)
* [Understand HavenScore risk tiers](../core-products/havenscore.md)
