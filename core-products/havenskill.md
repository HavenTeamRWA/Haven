# HavenSkill

> One-click OpenClaw integration — instantly query, evaluate, and rank stablecoin investment paths.

---

## What is HavenSkill?

HavenSkill is a packaged OpenClaw skill module. Any AI agent built on the OpenClaw framework can install HavenSkill to gain instant access to Haven's yield data, risk scoring, and execution capabilities — without custom integration work.

{% hint style="info" %}
HavenSkill makes Haven composable. Third-party agents, trading bots, and DAO automation tools can leverage Haven's infrastructure as a skill layer rather than building from scratch.
{% endhint %}

---

## Skill Capabilities

| Method | Description |
|---|---|
| `query_yield_paths()` | Returns ranked stablecoin yield opportunities with current APY and HavenScore |
| `score_protocol(protocol_id)` | Returns real-time HavenScore for any supported protocol |
| `execute_strategy(params)` | Submits an allocation strategy for on-chain execution via HavenClaw |
| `monitor_position(vault_id)` | Subscribe to real-time alerts for a user's active Haven position |

---

## Installation

**Via npm:**

```bash
npm install @openclaw/haven-skill
```

**Via OpenClaw registry:**

```bash
openclaw skill add haven
```

---

## Usage Example

```typescript
import { HavenSkill } from '@openclaw/haven-skill';

const agent = new OpenClawAgent({
  skills: [new HavenSkill({ apiKey: process.env.HAVEN_API_KEY })]
});

// Query best yield paths
const paths = await agent.run('query_yield_paths', {
  minScore: 70,
  minApy: 5.0,
  asset: 'USDC'
});

// Returns ranked list of opportunities with APY and HavenScore
```

---

## Response Format

```json
{
  "paths": [
    {
      "protocol": "Aave V3",
      "asset": "USDC",
      "apy": 6.8,
      "haven_score": 88,
      "chain": "Arbitrum",
      "tvl_usd": 420000000
    },
    {
      "protocol": "Tokenized T-Bill",
      "asset": "USDC",
      "apy": 5.1,
      "haven_score": 96,
      "chain": "Ethereum",
      "tvl_usd": 85000000
    }
  ]
}
```

---

## Related

* [OpenClaw Framework — Full integration guide](../integration/openclaw.md)
* [API Reference — Direct REST API access](../integration/api.md)
* [HavenScore — Understanding risk scores](havenscore.md)
