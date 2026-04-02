# HavenScore

> Real-time AI risk intelligence for every yield-bearing position.

---

## What is HavenScore?

HavenScore is Haven's proprietary risk scoring system. It assigns a dynamic risk score (0–100) to every supported protocol and strategy, updating in real time as market conditions change.

Scores are calculated from four signal categories: on-chain activity, market data, social sentiment, and smart contract health.

---

## Signal Sources

### 🐋 Whale Activity (On-chain)
Tracks large wallet movements and liquidity exits as early warning signals for protocol stress or impending de-pegs.

### 📊 Price & Liquidity (Market Data)
Real-time TVL changes, stablecoin peg stability, slippage depth, and borrowing rate anomalies.

### 💬 Social Signals (Sentiment)
Protocol-level sentiment aggregated from X/Twitter, governance forums, and Discord communities.

### 🔐 Smart Contract Health (Protocol)
Audit status, admin key exposure, upgrade proxy risk, and historical exploit patterns.

---

## Score Tiers

| Score Range | Tier | Recommended Action |
|---|---|---|
| 80–100 | ✅ Safe | Full allocation permitted |
| 60–79 | 🔵 Moderate | Allocation with monitoring |
| 40–59 | ⚠️ Caution | Reduce exposure, review weekly |
| 0–39 | 🔴 High Risk | Auto-exit triggered (if enabled) |

---

## Automated Risk Management

{% hint style="info" %}
Users can configure HavenScore thresholds to trigger automatic exits or rebalances when a position's score drops below their defined floor — enabling fully autonomous risk management without manual oversight.
{% endhint %}

To enable auto-exit:

1. Open your vault settings in the dashboard
2. Set a **minimum score floor** (e.g. 60)
3. Choose action: **Rebalance** (move to safer protocol) or **Exit** (return to stablecoin)

---

## Related

* [HavenClaw — Strategy execution](havenclaw.md)
* [Unified Yield Gateway — Supported protocols and assets](gateway.md)
