<p align="center">
  <img width="350" src="https://github.com/enviodev/.github/assets/82444671/602e8a3a-0ba7-46fc-b482-d77d016441d6" alt=" custom image"/>
<p align="center">

<p align="center">
Web3's backend. The fastest, most flexible way to index and query real-time & historical blockchain data.
</p>


<div align="center">

[![License](https://img.shields.io/badge/docs-docs.envio.dev-blue)](https://docs.envio.dev/docs/HyperIndex/licensing)
[![Discord](https://img.shields.io/badge/Discord-Join-7289da?logo=discord&logoColor=white)](https://discord.gg/Q9qt8gZ2fX)
[![Twitter](https://img.shields.io/twitter/follow/envio_indexer?style=social)](https://twitter.com/envio_indexer)
[![Docs](https://img.shields.io/badge/docs-docs.envio.dev-blue)](https://docs.envio.dev)

</div>

---

## What is HyperIndex?

[HyperIndex](https://docs.envio.dev/docs/HyperIndex/overview) is a **fast, multichain blockchain indexer** built by [Envio](https://envio.dev). It transforms on-chain events into production-ready APIs in minutes, not days, giving developers reliable, queryable backends for blockchain applications without managing complex infrastructure.

HyperIndex is powered by **[HyperSync](https://docs.envio.dev/docs/HyperSync/overview)**, Envio's proprietary data retrieval layer that is **2,000x faster than standard RPC endpoints**. The latest release processes **25,000 events per second** during historical backfill as standard. In independent benchmarks conducted by Sentio (May 2025), HyperIndex was the fastest blockchain indexer tested across every scenario: **4,472x faster than Subgraphs**, and **158x faster than the next best solution**.

---

## Why HyperIndex?

- **Fastest in independent benchmarks**: outperforms all competitors across every scenario tested by Sentio (May 2025)
- **25,000 events per second**: historical backfill speed as standard in the latest release
- **2,000x faster than RPC**: powered by HyperSync, Envio's optimised data retrieval layer
- **Truly multichain**: index any EVM chain, Solana, or Fuel in a single indexer with one unified API
- **Transform data into production-ready APIs in minutes, not days**: generate a full indexer from a contract address in seconds
- **Real-time + historical**: stream live events with minimal latency, seamlessly combined with historical backfill
- **Reorg & restart resilient**: automatic reorg handling with zero downtime rollback, your data is never corrupted
- **No vendor lock-in**: use Envio's hosted service or self-host, fully open source
- **Built for AI-assisted development**: local environment with test framework, designed to work with AI coding tools

---

## Performance

Independent benchmarks by Sentio (May 2025), Uniswap V2 Factory dataset:

| Indexer | Time | vs HyperIndex |
|---|---|---|
| **HyperIndex (Envio)** | **1 minute** | baseline |
| Subsquid | 15 minutes | 15x slower |
| Sentio | 2 hours 22 minutes | 142x slower |
| The Graph | 2 hours 23 minutes | 143x slower |
| Ponder | 2 hours 38 minutes | **158x slower** |

LBTC Token with RPC calls (the most realistic real-world indexing scenario):

| Indexer | Time | vs HyperIndex |
|---|---|---|
| **HyperIndex (Envio)** | **1 minute** | baseline |
| Sentio | 6 minutes | 6x slower |
| Ponder | 45 minutes | 45x slower |
| The Graph | 1 hour 3 minutes | 63x slower |

> Source: [Sentio benchmark repository](https://github.com/enviodev/open-indexer-benchmark/blob/main/sentio-benchmarks-may-2025/README.md), May 2025. Full details: [HyperIndex Performance Benchmarks](https://docs.envio.dev/docs/HyperIndex/benchmarks)

---

## Key Features

### Instant Indexer Generation
Point HyperIndex at any contract address and it auto-generates your entire indexer scaffold from the ABI: event handlers, schema, and GraphQL API. Go from zero to querying in minutes.

[Quickstart](https://docs.envio.dev/docs/HyperIndex/contract-import)

### Multichain Aggregation
Index contracts across multiple chains and query all your data from a single GraphQL API. Supports any EVM-compatible chain, Solana (experimental), and Fuel.

[Multichain Indexing](https://docs.envio.dev/docs/HyperIndex/multichain-indexing)

### Real-Time Event Streaming
Stream live blockchain events as they happen with minimal latency. HyperIndex handles the transition from historical backfill to real-time mode automatically.

### Reorg & Restart Resilient
Automatic blockchain reorganisation handling with zero downtime rollback. HyperIndex never corrupts your data, even through reorgs or indexer restarts.

### Block Handlers
Run custom logic on every block or at defined intervals, unlocking time-series data, aggregations, and bulk SQL updates.

[Block Handlers](https://docs.envio.dev/docs/HyperIndex/block-handlers)

### Factory Contracts & Dynamic Registration
Index data from over 1 million dynamically registered contracts, including nested factory contracts where contracts deploy further contracts.

[Dynamic Contracts](https://docs.envio.dev/docs/HyperIndex/dynamic-contracts)

### Off-Chain Data Integration
Combine on-chain events with off-chain data sources directly inside your event handlers.

### Migrate from Existing Indexers
Already running a subgraph or Alchemy indexer? HyperIndex includes migration tooling:
- [Migrate from The Graph](https://docs.envio.dev/docs/HyperIndex/migration-guide)
- [Migrate from Alchemy](https://docs.envio.dev/docs/HyperIndex/migrate-from-alchemy)

### Hosted Service or Self-Host
Deploy to Envio's managed hosted service with a single command, or self-host on your own infrastructure. No vendor lock-in.

[Hosted Service](https://docs.envio.dev/docs/HyperIndex/hosted-service)

---

## Supported Chains

HyperIndex supports:
- **Any EVM-compatible chain** (HyperSync available on 70+ networks)
- **[Solana](https://docs.envio.dev/docs/HyperIndex/solana)** (Experimental. Available since 3.0.0-alpha.3.
RPC-only source. HyperSync for Solana is not available yet; we’ll consider it if there’s demand.)
- **[Fuel Network](https://docs.envio.dev/docs/HyperIndex/fuel)**

[Full Supported Networks List](https://docs.envio.dev/docs/HyperIndex/supported-networks)

---

## Quickstart
Run the following command to initialize using a template:

```bash
pnpx envio init
```

Choose to scaffold from:
- A **contract address**: auto-generates your indexer from the ABI ([Quickstart](https://docs.envio.dev/docs/HyperIndex/contract-import))
- A **template**: choose from built-in starter templates
- An **existing subgraph**: migrate with minimal changes

[Getting Started Guide](https://docs.envio.dev/docs/HyperIndex/getting-started)

---

## Language Support

Write event handlers in:
- **TypeScript** (recommended)
- **JavaScript**
- **ReScript**

---

## Local Development

```bash
pnpm dev
```

This command automatically launches your local environment and opens the Hasura dashboard, where you can view indexed blockchain data.

[Envio Command Line Interface](https://docs.envio.dev/docs/HyperIndex/cli-commands)

---

## Documentation

Full documentation at **[docs.envio.dev](https://docs.envio.dev)**

| Section | Link |
|---|---|
| Overview | [HyperIndex Overview](https://docs.envio.dev/docs/HyperIndex/overview) |
| Getting Started | [Getting Started](https://docs.envio.dev/docs/HyperIndex/getting-started) |
| Showcase | [Showcase](https://docs.envio.dev/showcase) |
| Benchmarks | [Benchmarks](https://docs.envio.dev/docs/HyperIndex/benchmarks) |
| HyperSync | [HyperSync Overview](https://docs.envio.dev/docs/HyperSync/overview) |
| HyperRPC | [HyperRPC Overview](https://docs.envio.dev/docs/HyperRPC/overview-hyperrpc) |
| Configuration | [config.yaml](https://docs.envio.dev/docs/HyperIndex/configuration-file) |
| Event Handlers | [Event Handlers](https://docs.envio.dev/docs/HyperIndex/event-handlers) |
| Block Handlers | [Block Handlers](https://docs.envio.dev/docs/HyperIndex/block-handlers) |
| Multichain Indexing | [Multichain](https://docs.envio.dev/docs/HyperIndex/multichain-indexing) |
| Supported Networks | [Networks](https://docs.envio.dev/docs/HyperIndex/supported-networks) |
| Hosted Service | [Hosting](https://docs.envio.dev/docs/HyperIndex/hosted-service) |
| Pricing & Billing | [Pricing](https://docs.envio.dev/docs/HyperIndex/hosted-service-billing) |
| Self-Hosting | [Self-Host](https://docs.envio.dev/docs/HyperIndex/self-hosting) |
| Licensing | [Licensing](https://docs.envio.dev/docs/HyperIndex/licensing) |


---

## FAQ

<details>
<summary>What is HyperIndex used for?</summary>

HyperIndex is used to index blockchain events and make on-chain data queryable via a GraphQL API. Common use cases include DeFi dashboards, NFT marketplaces, protocol analytics, trading bots, and any application that needs fast, structured access to real-time or historical blockchain data.

</details>

<details>
<summary>How does HyperIndex compare to The Graph?</summary>

Independent benchmarks by Sentio (May 2025) show HyperIndex is significantly faster than The Graph across every tested scenario: 143x faster in the Uniswap V2 Factory benchmark and 63x faster in the LBTC with RPC calls benchmark (the most realistic real-world scenario). HyperIndex also supports Solana (experimental) and Fuel in addition to any EVM chain, handles reorgs automatically, and supports TypeScript, JavaScript, and ReScript.

</details>

<details>
<summary>What is HyperSync?</summary>

HyperSync is Envio's proprietary data retrieval layer that powers HyperIndex's speed advantage. It is 2,000x faster than standard RPC endpoints. HyperSync can also be used independently for custom data pipelines. See [HyperSync docs](https://docs.envio.dev/docs/HyperSync/overview-hypersync).

</details>

<details>
<summary>How fast are the sync speeds?</summary>

HyperIndex sync speeds are best-in-class. The latest release processes 25,000 events per second as standard. In independent benchmarks, HyperIndex synced millions of events in minutes rather than hours, and what would previously take weeks at scale (100M+ events) can now be completed in just over an hour. See the full [benchmark results](https://docs.envio.dev/docs/HyperIndex/benchmarks).

</details>

<details>
<summary>What chains are supported?</summary>

Any EVM-compatible chain is supported. Over 70+ EVM networks have HyperSync enabled for the fastest possible sync speeds. The Fuel network is also fully supported. For a full list of HyperSync-supported networks, see the [supported networks documentation](https://docs.envio.dev/docs/HyperSync/hypersync-supported-networks).

</details>

<details>
<summary>Do you support any non-EVM chains?</summary>

Yes. Envio supports the Fuel network and is looking to expand support to other non-EVM networks. Reach out on [Discord](https://discord.gg/Q9qt8gZ2fX) if you have a specific network in mind.

</details>

<details>
<summary>What is multichain indexing?</summary>

Multichain indexing allows you to index data from multiple blockchain networks (e.g., Ethereum and Base) within a single indexer, querying everything from one unified GraphQL API. HyperIndex supports two modes:

- **Unordered mode**: indexes data from each chain as fast as possible, optimising for speed
- **Time-ordered mode**: preserves the chronological order of events across all indexed chains, enabling operations on entities from different chains while maintaining temporal consistency

Multichain indexing is available on all pricing plans. See [Multichain Indexing docs](https://docs.envio.dev/docs/HyperIndex/multichain-indexing).

</details>

<details>
<summary>Does HyperIndex support multiple chains simultaneously?</summary>

Yes. HyperIndex natively aggregates events from multiple blockchains into a single database and GraphQL API. You define all chains in one config and query them uniformly.

</details>

<details>
<summary>Can I migrate from an existing subgraph or alternative indexer?</summary>

Yes. HyperIndex includes dedicated migration tooling for [The Graph subgraphs](https://docs.envio.dev/docs/HyperIndex/migrate-subgraph), [Alchemy indexers](https://docs.envio.dev/docs/HyperIndex/migrate-alchemy) and more, with full support.

</details>

<details>
<summary>What languages can I write handlers in?</summary>

TypeScript, JavaScript, and ReScript.

</details>

<details>
<summary>Can I self-host HyperIndex?</summary>

Yes. HyperIndex can be self-hosted on your own infrastructure. The generated folder includes a Dockerfile as a starting point for deploying to any cloud provider or on-premises setup. Envio also offers a fully managed hosted service with faster setup, optimised performance, automatic updates, and dedicated support. See [hosting options](https://docs.envio.dev/docs/HyperIndex/hosted-service).

</details>

<details>
<summary>What are indexing hours?</summary>

Indexing hours measure how long your indexers run on the hosted service. Each deployed indexer is called a deployment, and every hour a deployment runs counts as one indexing hour. For example, one deployment running for a full month uses approximately 730 indexing hours. Extra indexing hours allow you to run multiple deployments simultaneously, enabling zero-downtime upgrades and easy iteration.

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

Yes. Service Level Agreements are available for users on the dedicated plan, covering uptime guarantees, response times, and support levels tailored to your requirements. [Contact the team](https://discord.gg/Q9qt8gZ2fX) to discuss your needs.

</details>

<details>
<summary>Are long-term discounts available?</summary>

Yes. Discounts are available for longer-term commitments, generally at least 20% depending on the length of commitment. [Reach out](https://discord.gg/Q9qt8gZ2fX) to discuss options.

</details>

<details>
<summary>I still have more questions</summary>

Reach out on [Discord](https://discord.gg/Q9qt8gZ2fX) and the team will help!

</details>

---

## Community & Support

- 💬 [Discord](https://discord.gg/Q9qt8gZ2fX): get help, share projects, talk to the team
- 🐦 [X](https://twitter.com/envio_indexer): announcements and updates
- 🐛 [GitHub Issues](https://github.com/enviodev/hyperindex/issues): bug reports and feature requests
- 📖 [Docs](https://docs.envio.dev): full documentation

---

## Contributing

Contributions are welcome! Please open an issue to discuss what you'd like to change before submitting a PR.

---

## License

See [Licensing](https://docs.envio.dev/docs/HyperIndex/licensing) in the documentation.
