<p align="center">
  <img width="350" src="https://raw.githubusercontent.com/enviodev/brandkit/main/logos/envio-logo-primary.png" alt="Envio"/>
</p>

<p align="center">
Web3's backend. The fastest, most flexible way to index and query real-time and historical blockchain data.
</p>

<div align="center">

[![GitHub Stars](https://img.shields.io/github/stars/enviodev/hyperindex?style=social)](https://github.com/enviodev/hyperindex)
[![Discord](https://img.shields.io/badge/Discord-Join-7289da?logo=discord&logoColor=white)](https://discord.gg/envio)
[![X](https://img.shields.io/badge/X-Follow-000000?logo=x&logoColor=white)](https://twitter.com/envio_indexer)
[![Docs](https://img.shields.io/badge/docs-docs.envio.dev-blue)](https://docs.envio.dev)

</div>

---

## What is Envio?

Envio is the fastest, most flexible way to get on-chain data across any EVM chain, plus Solana and Fuel.

The Envio stack:

- **[HyperIndex](https://docs.envio.dev/docs/HyperIndex/overview)**: a fast, multichain blockchain indexer. Transforms on-chain events into production-ready GraphQL APIs in minutes, not days. Independently benchmarked as the fastest indexer tested across every scenario by [Sentio (May 2025)](https://github.com/enviodev/open-indexer-benchmark/blob/main/sentio-benchmarks-may-2025/README.md).
- **[HyperSync](https://docs.envio.dev/docs/HyperSync/overview)**: the data retrieval layer powering HyperIndex. Up to 2,000x faster than standard RPC endpoints, available natively on 79+ networks. Can also be used standalone for custom data pipelines via REST or SDKs in Rust, Python, JavaScript, and Go.
- **[HyperRPC](https://docs.envio.dev/docs/HyperRPC/overview-hyperrpc)**: a read-only JSON-RPC endpoint powered by HyperSync. Up to 5x faster than traditional nodes like geth, erigon, and reth for data-intensive operations. Drop-in replacement for existing RPC-based tooling.
- **[Envio Cloud](https://docs.envio.dev/docs/HyperIndex/hosted-service)**: a fully managed hosting solution for HyperIndex. Git-based deployments, zero-downtime version switching, built-in monitoring and alerting (Discord, Slack, Telegram, Email), and IP/domain whitelisting. Self-hosting is also fully supported.

---

## Case studies

- **Polymarket**: replaced 8 subgraphs with one TypeScript indexer on Polygon, syncing 4 billion events in 6 days. [Read the case study](https://docs.envio.dev/blog/polymarket-hyperindex-case-study)
- **Sablier**: consolidated 12 separate indexer deployments into a single multichain indexer, now indexing across 18 EVM chains. [Read the case study](https://docs.envio.dev/blog/case-study-sablier)
- **Limitless Exchange**: powers a daily prediction market on Base with real-time on-chain data and a custom GraphQL API. [Read the case study](https://docs.envio.dev/blog/case-study-limitless-prediction-market)
- **Bridgg**: aggregates deposit and withdrawal data across 12 OP Superchain networks, indexing 11 million events in one deployment. [Read the case study](https://docs.envio.dev/blog/case-study-bridgg-op-superchain)
- **zkPass**: verifies identity and transactions across 8 EVM networks using ZK proofs while keeping user data private. [Read the case study](https://docs.envio.dev/blog/zkpass-shaping-future-of-data-privacy)

[View all case studies](https://docs.envio.dev/blog?tag=case-studies)

---

## Performance

Independent benchmarks by [Sentio (May 2025)](https://github.com/enviodev/open-indexer-benchmark/blob/main/sentio-benchmarks-may-2025/README.md), Uniswap V2 Factory dataset (raw indexing speed):

| Indexer | Time | vs HyperIndex |
|---|---|---|
| **HyperIndex (Envio)** | **1 minute** | baseline |
| Subsquid | 15 minutes | 15x slower |
| Sentio | 2 hours 22 minutes | 142x slower |
| The Graph | 2 hours 23 minutes | 143x slower |
| Ponder | 2 hours 38 minutes | **158x slower** |

LBTC Token with RPC calls (the most realistic real-world scenario, where contract reads are required):

| Indexer | Time | vs HyperIndex |
|---|---|---|
| **HyperIndex (Envio)** | **1 minute** | baseline |
| Sentio | 6 minutes | 6x slower |
| Ponder | 45 minutes | 45x slower |
| The Graph | 1 hour 3 minutes | 63x slower |

> Source: [Sentio benchmark repository](https://github.com/enviodev/open-indexer-benchmark/blob/main/sentio-benchmarks-may-2025/README.md), May 2025. Full details: [HyperIndex Performance Benchmarks](https://docs.envio.dev/docs/HyperIndex/benchmarks)

---

## Key Features

| Feature | Description |
|---|---|
| **[Instant Indexer Generation](https://docs.envio.dev/docs/HyperIndex/contract-import)** | Point HyperIndex at any contract address. It auto-generates your entire indexer scaffold from the ABI: event handlers, schema, and GraphQL API. |
| **[Multichain Aggregation](https://docs.envio.dev/docs/HyperIndex/multichain-indexing)** | Index contracts across multiple chains and query all your data from a single GraphQL API. Supports any EVM chain, Solana (beta), and Fuel. |
| **Real-Time Event Streaming** | Stream live blockchain events with minimal latency. Transition from historical backfill to real-time mode automatically. |
| **Reorg and Restart Resilient** | Automatic reorganisation handling with zero downtime rollback. Your data is never corrupted. |
| **[Block Handlers](https://docs.envio.dev/docs/HyperIndex/block-handlers)** | Run custom logic on every block or at defined intervals. Unlocks time-series data, aggregations, and bulk SQL updates. |
| **[Factory Contracts](https://docs.envio.dev/docs/HyperIndex/dynamic-contracts)** | Index data from over 1 million dynamically registered contracts, including nested factories. |
| **[Trace Support](https://docs.envio.dev/blog/tracking-native-eth-transfers-hypersync)** | Index transaction traces directly via HyperSync, including native ETH transfers. Available on Ethereum, Base, Arbitrum, Gnosis, and Monad. |
| **Off-Chain Data Integration** | Combine on-chain events with off-chain data sources directly inside your event handlers. |
| **[AI-Assisted Development](https://docs.envio.dev/docs/HyperIndex/quickstart-with-ai)** | Generated projects ship with Cursor and Claude skills, agent-friendly templates, and an MCP server. Agents can scaffold, configure, and deploy end to end. |
| **[Migration Tooling](https://docs.envio.dev/docs/HyperIndex/migration-guide)** | Dedicated migration support from The Graph, Ponder, and Alchemy. AI-assisted migration available. |
| **[Envio Cloud or Self-Host](https://docs.envio.dev/docs/HyperIndex/hosted-service)** | Deploy to Envio Cloud with a single command, or self-host on your own infrastructure. No vendor lock-in. |

---

## Supported Chains

HyperIndex supports:

- **Any EVM-compatible chain** (HyperSync available natively on 79+ networks; non-HyperSync EVM chains work via RPC)
- **[Solana](https://docs.envio.dev/docs/HyperIndex/solana)** (beta. Powered by HyperSync for Solana. Instruction-level handlers via `indexer.onInstruction`, IDL-aware decoding, inner instructions (CPIs), and token balance changes. Slot handlers via `indexer.onSlot`. TypeScript only.)
- **[Fuel Network](https://docs.envio.dev/docs/HyperIndex/fuel)**

[Full Supported Networks List](https://docs.envio.dev/docs/HyperSync/hypersync-supported-networks)

---

## Quickstart

### Prerequisites

- [Node.js](https://nodejs.org/en/download/current) v22 or newer
- [pnpm](https://pnpm.io/installation) v8 or newer
- [Docker Desktop](https://www.docker.com/products/docker-desktop/) (only required for running indexers locally)
- Windows users: [WSL](https://learn.microsoft.com/en-us/windows/wsl/install)

### Initialize an indexer

```bash
pnpx envio init
```

Choose to scaffold from:

- A **contract address**: auto-generates your indexer from the ABI ([Quickstart](https://docs.envio.dev/docs/HyperIndex/contract-import))
- A **template**: choose from built-in starter templates (ERC20, Greeter, and more)
- An **existing subgraph**: migrate with minimal changes

[Getting Started Guide](https://docs.envio.dev/docs/HyperIndex/getting-started) | [Quickstart with AI](https://docs.envio.dev/docs/HyperIndex/quickstart-with-ai)

### Run locally

```bash
pnpm dev
```

This launches your local environment and opens the Hasura dashboard, where you can view indexed blockchain data. To stop and clean up:

```bash
pnpm envio stop
```

### Deploy

Deploy to Envio Cloud with a single command. See the [Envio Cloud documentation](https://docs.envio.dev/docs/HyperIndex/hosted-service) for full details.

---

## Language Support

Write event handlers in TypeScript (recommended), JavaScript, or ReScript.

---

## Documentation

Full documentation at **[docs.envio.dev](https://docs.envio.dev)**.

**Get started**

- [HyperIndex Overview](https://docs.envio.dev/docs/HyperIndex/overview)
- [Getting Started](https://docs.envio.dev/docs/HyperIndex/getting-started)
- [Quickstart with AI](https://docs.envio.dev/docs/HyperIndex/quickstart-with-ai)
- [Showcase](https://docs.envio.dev/showcase)
- [Benchmarks](https://docs.envio.dev/docs/HyperIndex/benchmarks)

**Products**

- [HyperSync Overview](https://docs.envio.dev/docs/HyperSync/overview)
- [HyperRPC Overview](https://docs.envio.dev/docs/HyperRPC/overview-hyperrpc)
- [Solana (beta)](https://docs.envio.dev/docs/HyperIndex/solana)
- [Fuel](https://docs.envio.dev/docs/HyperIndex/fuel)

**Building**

- [config.yaml](https://docs.envio.dev/docs/HyperIndex/configuration-file)
- [schema.graphql](https://docs.envio.dev/docs/HyperIndex/schema)
- [Event Handlers](https://docs.envio.dev/docs/HyperIndex/event-handlers)
- [Block Handlers](https://docs.envio.dev/docs/HyperIndex/block-handlers)
- [Multichain Indexing](https://docs.envio.dev/docs/HyperIndex/multichain-indexing)
- [MCP Server](https://docs.envio.dev/docs/HyperIndex/mcp-server)
- [Supported Networks](https://docs.envio.dev/docs/HyperSync/hypersync-supported-networks)

**Hosting and operations**

- [Envio Cloud](https://docs.envio.dev/docs/HyperIndex/hosted-service)
- [Pricing and Billing](https://docs.envio.dev/docs/HyperIndex/hosted-service-billing)
- [Self-Hosting](https://docs.envio.dev/docs/HyperIndex/self-hosting)
- [API Tokens](https://docs.envio.dev/docs/HyperSync/api-tokens)
- [Licensing](https://docs.envio.dev/docs/HyperIndex/licensing)

---

## FAQ

<details>
<summary>What is HyperIndex used for?</summary>

HyperIndex is used to index blockchain events and make on-chain data queryable via a GraphQL API. Common use cases include DeFi dashboards, NFT marketplaces, protocol analytics, trading bots, and any application that needs fast, structured access to real-time or historical blockchain data.

</details>

<details>
<summary>How does HyperIndex compare to The Graph?</summary>

Independent benchmarks by Sentio (May 2025) show HyperIndex is significantly faster than The Graph across every tested scenario: 143x faster in the Uniswap V2 Factory benchmark and 63x faster in the LBTC with RPC calls benchmark (the most realistic real-world scenario). HyperIndex also supports Solana (beta) and Fuel in addition to any EVM chain, handles reorgs automatically, and supports TypeScript, JavaScript, and ReScript handlers instead of AssemblyScript.

</details>

<details>
<summary>What is HyperSync?</summary>

HyperSync is Envio's proprietary data retrieval layer that powers HyperIndex's speed advantage. It is up to 2,000x faster than standard RPC endpoints, using optimised binary encoding and parallel fetching. HyperSync can also be used independently for custom data pipelines via REST or SDKs in Rust, Python, JavaScript, and Go. See the [HyperSync docs](https://docs.envio.dev/docs/HyperSync/overview).

</details>

<details>
<summary>What is HyperRPC?</summary>

HyperRPC is a read-only JSON-RPC endpoint powered by HyperSync. Early benchmarks show up to 5x performance improvement over traditional nodes like geth, erigon, and reth for data-intensive operations. It works as a drop-in replacement for existing RPC-based tooling with no integration changes needed. See the [HyperRPC docs](https://docs.envio.dev/docs/HyperRPC/overview-hyperrpc).

</details>

<details>
<summary>How fast are the sync speeds?</summary>

HyperIndex sync speeds are best-in-class. In independent benchmarks, HyperIndex synced millions of events in minutes rather than hours, and what would previously take weeks at scale (100M+ events) can now be completed in just over an hour. See the full [benchmark results](https://docs.envio.dev/docs/HyperIndex/benchmarks).

</details>

<details>
<summary>What chains are supported?</summary>

Any EVM-compatible chain is supported. 79+ EVM networks have HyperSync enabled for the fastest possible sync speeds; non-HyperSync EVM chains work via RPC. Fuel and Solana (beta) are also supported. For a full list of HyperSync-supported networks, see the [supported networks documentation](https://docs.envio.dev/docs/HyperSync/hypersync-supported-networks).

</details>

<details>
<summary>Do you support any non-EVM chains?</summary>

Yes. HyperIndex supports the Fuel network and Solana (beta). Solana indexing runs on HyperSync for Solana, with instruction-level handlers, IDL-aware decoding, CPI support, and token balance changes. Envio is looking to expand non-EVM coverage further. Reach out on [Discord](https://discord.gg/envio) if you have a specific network in mind.

</details>

<details>
<summary>How does Solana support work?</summary>

Solana support is in beta. Indexing runs on [HyperSync for Solana](https://docs.envio.dev/docs/HyperSync/solana), the same data engine behind EVM indexing, so historical backfills are fast. You match program instructions by discriminator with `indexer.onInstruction`, and HyperIndex decodes the arguments and accounts using your Anchor IDL or an inline schema. Inner instructions (CPIs), token balances and balance changes, transaction metadata and program logs are all available. `indexer.onSlot` covers per-slot logic and RPC enrichment through the Effect API. Solana indexers are TypeScript only. See the [Solana documentation](https://docs.envio.dev/docs/HyperIndex/solana) for details.

</details>

<details>
<summary>Does HyperIndex support transaction traces?</summary>

Yes. HyperSync supports trace queries on Ethereum, Base, Arbitrum, Gnosis, and Monad, enabling efficient indexing of native ETH transfers and internal contract calls that do not emit logs. Reach out on [Discord](https://discord.gg/envio) if you need trace support for an additional chain.

</details>

<details>
<summary>What is multichain indexing?</summary>

Multichain indexing allows you to index data from multiple blockchain networks (for example, Ethereum and Base) within a single indexer, querying everything from one unified GraphQL API. HyperIndex supports two modes:

- **Unordered mode**: indexes data from each chain as fast as possible, optimising for speed
- **Time-ordered mode**: preserves the chronological order of events across all indexed chains, enabling operations on entities from different chains while maintaining temporal consistency

Multichain indexing is available on all pricing plans. See [Multichain Indexing docs](https://docs.envio.dev/docs/HyperIndex/multichain-indexing).

</details>

<details>
<summary>Can I migrate from an existing subgraph or alternative indexer?</summary>

Yes. HyperIndex includes dedicated migration tooling for [The Graph subgraphs](https://docs.envio.dev/docs/HyperIndex/migration-guide), [Ponder](https://docs.envio.dev/docs/HyperIndex/migrate-from-ponder), and [Alchemy](https://docs.envio.dev/docs/HyperIndex/migrate-from-alchemy). For an assistant-led workflow, see [Migrate with AI](https://docs.envio.dev/docs/HyperIndex/migrate-with-ai).

</details>

<details>
<summary>What languages can I write handlers in?</summary>

TypeScript, JavaScript, and ReScript.

</details>

<details>
<summary>Can I self-host HyperIndex?</summary>

Yes. HyperIndex can be self-hosted on your own infrastructure. The generated folder includes a Dockerfile as a starting point for deploying to any cloud provider or on-premises setup. API tokens are required for HyperSync access in self-hosted deployments. Envio Cloud is also available as a fully managed alternative with faster setup, optimised performance, automatic updates, and dedicated support. See [Envio Cloud](https://docs.envio.dev/docs/HyperIndex/hosted-service) and [API Tokens](https://docs.envio.dev/docs/HyperSync/api-tokens).

</details>

<details>
<summary>Are HyperSync API tokens required?</summary>

Yes. As of 3 November 2025, API tokens are required for HyperSync access. Indexers deployed to Envio Cloud have access to HyperSync that does not require a custom API token. For local development and self-hosted deployments, tokens can be generated from the Envio app, and an automatic CLI login flow is available to make local development smoother. See [API Tokens](https://docs.envio.dev/docs/HyperSync/api-tokens) for details.

</details>

<details>
<summary>What are indexing hours?</summary>

Indexing hours measure how long your indexers run on Envio Cloud. Each deployed indexer is called a deployment, and every hour a deployment runs counts as one indexing hour. For example, one deployment running for a full month uses approximately 730 indexing hours. Extra indexing hours allow you to run multiple deployments simultaneously, enabling zero-downtime upgrades and easy iteration.

</details>

<details>
<summary>What are zero-downtime deployments?</summary>

Zero-downtime deployments let you update your indexer without any service interruption. Deploy a new version alongside your current one, and once it's ready, use the Promote to Production feature to instantly switch your production GraphQL endpoint with no downtime for your users or applications.

</details>

<details>
<summary>What limits are there on the development plan?</summary>

The free development plan includes automatic deletion policies to ensure fair resource allocation.

Hard limits:

- Deployments exceeding 20GB of storage will be automatically deleted
- Deployments older than 30 days will be automatically deleted

Soft limits (whichever comes first):

- 100,000 events processed
- 5GB storage used
- No requests for 7 days

When soft limits are breached, a two-stage deletion process begins: a 7-day grace period where the indexer continues to function normally, followed by 3 days of read-only access, then full deletion. See [Pricing](https://envio.dev/pricing) for production plan options.

</details>

<details>
<summary>Is there an SLA?</summary>

Yes. Service Level Agreements are available for users on the dedicated plan, covering uptime guarantees, response times, and support levels tailored to your requirements. [Contact the team](https://discord.gg/envio) to discuss your needs.

</details>

<details>
<summary>Are long-term discounts available?</summary>

Yes. Discounts are available for longer-term commitments, generally at least 20% depending on the length of commitment. [Reach out](https://discord.gg/envio) to discuss options.

</details>

<details>
<summary>I still have more questions</summary>

Reach out on [Discord](https://discord.gg/envio) and the team will help!

</details>

---

## Community and Support

- [Discord](https://discord.gg/envio)
- [X](https://twitter.com/envio_indexer)
- [YouTube](https://www.youtube.com/@envio_indexer)
- [GitHub Issues](https://github.com/enviodev/hyperindex/issues)
- [Docs](https://docs.envio.dev)
- [Newsletter](https://envio.beehiiv.com/subscribe)

---

## Contributing

Contributions are welcome. Please open an [issue](https://github.com/enviodev/hyperindex/issues) to discuss what you'd like to change before submitting a PR.

---

## License

See [Licensing](https://docs.envio.dev/docs/HyperIndex/licensing) in the documentation.
