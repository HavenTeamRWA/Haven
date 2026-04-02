# API Reference

> Direct REST API access to Haven's yield data and execution capabilities.

---

## Base URL

```
https://api.haven.financial/v1
```

---

## Authentication

All API requests require a Bearer token in the Authorization header.

```http
Authorization: Bearer YOUR_HAVEN_API_KEY
Content-Type: application/json
```

API keys are available to registered developers. Apply at [haven.financial](https://www.haven.financial).

---

## Endpoints

### GET /v1/yield/paths

Returns ranked yield opportunities across all supported protocols.

**Request body:**

```json
{
  "filter": {
    "min_score": 70,
    "min_apy": 5.0,
    "asset": "USDC",
    "chain": "arbitrum"
  }
}
```

**Response:**

```json
{
  "paths": [
    {
      "protocol": "Aave V3",
      "asset": "USDC",
      "apy": 6.8,
      "haven_score": 88,
      "chain": "arbitrum",
      "tvl_usd": 420000000
    }
  ]
}
```

---

### GET /v1/score/:protocol\_id

Returns the current HavenScore and signal breakdown for a specific protocol.

**Example:**

```
GET /v1/score/aave-v3-arbitrum
```

**Response:**

```json
{
  "protocol_id": "aave-v3-arbitrum",
  "score": 88,
  "tier": "safe",
  "signals": {
    "whale_activity": 91,
    "market_health": 85,
    "sentiment": 87,
    "contract_risk": 90
  },
  "updated_at": "2026-04-02T10:00:00Z"
}
```

---

### POST /v1/strategy/execute

Submit a strategy for on-chain execution via HavenClaw.

**Request body:**

```json
{
  "wallet": "0xYOUR_WALLET_ADDRESS",
  "allocations": {
    "aave-v3-arbitrum": 0.55,
    "tbill-tokenized-eth": 0.30,
    "delta-neutral-base": 0.15
  },
  "rebalance_trigger": "5%",
  "compound_freq": "daily"
}
```

**Response:**

```json
{
  "strategy_id": "str_abc123",
  "status": "pending_confirmation",
  "simulation": {
    "estimated_apy": "6.8%",
    "gas_estimate_usd": 4.20
  }
}
```

---

### GET /v1/position/:vault\_id

Returns the current status and performance of an active vault position.

---

## Rate Limits

| Plan | Requests / minute |
|---|---|
| Free | 30 |
| Developer | 300 |
| Enterprise | Unlimited |

---

## Related

* [HavenSkill — OpenClaw SDK (higher-level abstraction)](../core-products/havenskill.md)
* [OpenClaw Framework](openclaw.md)
