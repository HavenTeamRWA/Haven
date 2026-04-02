# FAQ

Frequently asked questions about Haven's protocol, risk model, and integration.

---

## General

### Is Haven custodial?

No. Haven is fully non-custodial. Your assets remain in your own wallet-controlled vault at all times. Haven's AI agents have execution permissions only — they cannot withdraw or transfer funds to external addresses.

### What chains does Haven support?

Haven currently supports Ethereum mainnet, Arbitrum, Base, and Optimism. Additional chain support is planned for Phase 4 — see [Roadmap](roadmap.md).

### What are the fees?

Haven charges a performance fee on yield generated. There are no deposit or withdrawal fees. Exact fee structures are detailed in the [official documentation](https://docs.haven.financial/).

---

## Risk & Security

### How is HavenScore calculated?

HavenScore aggregates signals from four categories: on-chain whale activity, market liquidity and peg health, social sentiment, and smart contract risk factors. Each signal is weighted and combined into a 0–100 composite score that updates in real time.

### Have Haven's smart contracts been audited?

The Core Vault Contract has been audited. The Cross-chain Router audit is currently in progress. See the [Architecture](../getting-started/architecture.md) page for the full audit status table.

### Can I set up automatic exits if risk increases?

Yes. You can configure a minimum HavenScore floor in your vault settings. If a position's score drops below your threshold, Haven can automatically rebalance to a safer protocol or exit to stablecoin — depending on your preference.

---

## Integration & Development

### Can I use Haven as a developer?

Yes. HavenSkill is available for any OpenClaw-compatible AI agent. You can also access Haven's data and execution capabilities directly via the REST API. Apply for API access at [haven.financial](https://www.haven.financial).

### How do I install HavenSkill?

```bash
npm install @openclaw/haven-skill
# or
openclaw skill add haven
```

See the [HavenSkill documentation](../core-products/havenskill.md) for full usage examples.

### What is OpenClaw?

OpenClaw is the AI agent framework that Haven is built on. It provides tool-calling, multi-step reasoning, and cross-chain execution capabilities. See the [OpenClaw Framework page](../integration/openclaw.md) for details.

---

## Support

### Where can I get support?

* Join the community on [Telegram](https://t.me/AI_Haven)
* Follow updates on [Twitter/X](https://x.com/HavenAI_)
* Read technical deep-dives on [Medium](https://medium.com/@HavenAI)
* Browse the [official documentation](https://docs.haven.financial/)
