<p align="center">
  <img width="100%" src="https://raw.githubusercontent.com/enviodev/.github/main/profile/assets/envio-banner.gif" alt="Envio">
</p>

<h1 align="center">Build custom blockchain APIs &amp; analytics</h1>

<p align="center">
  Real-time, with enterprise SLAs. Production-ready for teams &amp; AI agents.
</p>

<p align="center">
  <a href="https://envio.dev"><img src="https://raw.githubusercontent.com/enviodev/.github/main/profile/assets/button-try-it-free.svg" height="40" alt="Try it free"></a>&nbsp;
  <a href="https://docs.envio.dev"><img src="https://raw.githubusercontent.com/enviodev/.github/main/profile/assets/button-read-the-docs.svg" height="40" alt="Read the docs"></a>&nbsp;
  <a href="https://envio.dev/pricing"><img src="https://raw.githubusercontent.com/enviodev/.github/main/profile/assets/button-contact-sales.svg" height="40" alt="Contact sales"></a>
</p>

<p align="center">
  <a href="https://github.com/enviodev/hyperindex"><img src="https://img.shields.io/github/stars/enviodev/hyperindex?style=flat&label=HyperIndex%20stars&color=24292F" alt="HyperIndex stars"></a>
  <a href="https://discord.gg/envio"><img src="https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white" alt="Discord"></a>
  <a href="https://t.me/+BeS5ihVUFONjNGFk"><img src="https://img.shields.io/badge/Telegram-join-26A5E4?logo=telegram&logoColor=white" alt="Telegram"></a>
  <a href="https://twitter.com/envio_indexer"><img src="https://img.shields.io/badge/X-follow-000000?logo=x&logoColor=white" alt="X"></a>
  <a href="https://docs.envio.dev/llms.txt"><img src="https://img.shields.io/badge/llms.txt-for_agents-24292F" alt="llms.txt"></a>
</p>

<table align="center"><tr><td>

```bash
pnpx envio init
```

</td></tr></table>

<p align="center"><sub>Start from a contract address, a template or an existing subgraph</sub></p>

<br>

<p align="center">
  Envio builds custom blockchain APIs and analytics. Teams use it to turn smart contract activity into real-time APIs, to pull raw onchain data into their own pipelines, and to run it all on managed infrastructure, from a free plan up to Dedicated deployments with an SLA. It works across any EVM chain, plus Solana and Fuel.
</p>

## Solutions

| What you need | How Envio does it |
|---|---|
| **[Build APIs and analytics](https://docs.envio.dev/docs/HyperIndex/overview)** | Turn contract activity into a custom dataset and serve it as a production GraphQL API |
| **[Query raw chain data](https://docs.envio.dev/docs/HyperSync/overview)** | Pull logs, transactions, blocks and traces into your own pipelines and analytics |
| **[Stream events to your systems](https://docs.envio.dev/docs/HyperIndex/effect-api#sending-notifications-webhooks)** | Trigger webhooks or push events to your own streams when something changes onchain |
| **[Give AI agents onchain data](https://docs.envio.dev/docs/HyperIndex/quickstart-with-ai)** | Give agents reliable onchain data, or use them to build production tools on Envio |
| **[Migrate your subgraphs](https://docs.envio.dev/docs/HyperIndex/migration-guide)** | Let Envio migrate and host your subgraphs, or port them to HyperIndex with AI |
| **[Hands-on help](https://envio.dev/pricing/services)** | Envio engineers on your project for migrations, performance tuning and architecture reviews |

## Products

| Product | What it does |
|---|---|
| **[HyperIndex](https://docs.envio.dev/docs/HyperIndex/overview)** | Indexing framework. TypeScript handlers in, real-time GraphQL API out. 6–879x faster in the [open indexer benchmark](https://github.com/enviodev/open-indexer-benchmark) |
| **[Envio Cloud](https://docs.envio.dev/docs/HyperIndex/hosted-service)** | Managed hosting. Deploy by pushing to your deployment branch, promote without downtime, monitor with logs and alerts |
| **[Subgraph Hosting](https://docs.envio.dev/docs/HyperIndex/migration-guide)** | Managed migration. Envio runs your subgraphs on HyperIndex behind a subgraph-compatible endpoint |
| **[HyperSync](https://docs.envio.dev/docs/HyperSync/overview)** | Blockchain data API. Up to 2,000x faster than JSON-RPC, with clients for Rust, Python, Node.js and Go |
| **[Solana HyperSync](https://docs.envio.dev/docs/HyperSync/solana)** | Solana transactions, instruction calls, logs and account activity from one endpoint |
| **[HyperRPC](https://docs.envio.dev/docs/HyperRPC/overview-hyperrpc)** | Read-only JSON-RPC. Up to 5x faster than geth, erigon and reth, with no code changes |

## Built for production

| | |
|---|---|
| **SLA** | Up to 99.99% uptime on Dedicated plans, backed by service credits |
| **Support** | 24/7 on-call for Dedicated customers |
| **Regions** | Multi-region failover |
| **Migration** | Step-by-step [migration guides](https://docs.envio.dev/docs/HyperIndex/migration-guide), or let Envio do it with Subgraph Hosting |

[Compare plans and contact sales →](https://envio.dev/pricing)

## Quickstart

1. Run `pnpx envio init` and pick a contract address, a template or a subgraph.
2. Run `pnpm dev` to start it locally and explore the data.
3. Deploy to [Envio Cloud](https://docs.envio.dev/docs/HyperIndex/hosted-service) by pushing to your deployment branch.

Needs Node.js 22.15 or newer, and Docker to run locally. pnpm is recommended. [Getting started guide →](https://docs.envio.dev/docs/HyperIndex/getting-started)

## Build with AI agents

| | |
|---|---|
| **Docs for agents** | [llms.txt](https://docs.envio.dev/llms.txt) and [llms-full.txt](https://docs.envio.dev/llms-full.txt) |
| **Docs MCP server** | `https://docs.envio.dev/mcp`, with `docs_search` and `docs_fetch` ([guide](https://docs.envio.dev/docs/HyperIndex/mcp-server)) |
| **Skills** | `pnpx envio init` adds [HyperIndex skills](https://github.com/enviodev/hyperindex/tree/main/packages/cli/templates/static/shared/.claude/skills) to every new project |
| **Quickstart** | [Quickstart with AI](https://docs.envio.dev/docs/HyperIndex/quickstart-with-ai), from a contract address to a deployed API |

## Repositories

| Repository | What it is |
|---|---|
| [hyperindex](https://github.com/enviodev/hyperindex) | The HyperIndex framework and CLI |
| [hypersync-client-rust](https://github.com/enviodev/hypersync-client-rust) · [python](https://github.com/enviodev/hypersync-client-python) · [node](https://github.com/enviodev/hypersync-client-node) · [go](https://github.com/enviodev/hypersync-client-go) | Official HyperSync clients |
| [open-indexer-benchmark](https://github.com/enviodev/open-indexer-benchmark) | Reproducible benchmark of blockchain indexers, refreshed by CI |
| [uniswap-v4-indexer](https://github.com/enviodev/uniswap-v4-indexer) | The real-time Uniswap V4 API behind v4.xyz |

## Resources

<table>
<tr>
<td valign="top">

**Get started**
- [Overview](https://docs.envio.dev/docs/HyperIndex/overview)
- [Getting started](https://docs.envio.dev/docs/HyperIndex/getting-started)
- [Quickstart with AI](https://docs.envio.dev/docs/HyperIndex/quickstart-with-ai)
- [Customer stories](https://docs.envio.dev/blog?tag=case-studies)
- [Benchmarks](https://github.com/enviodev/open-indexer-benchmark)

</td>
<td valign="top">

**Building**
- [config.yaml](https://docs.envio.dev/docs/HyperIndex/configuration-file)
- [schema.graphql](https://docs.envio.dev/docs/HyperIndex/schema)
- [Event handlers](https://docs.envio.dev/docs/HyperIndex/event-handlers)
- [Block handlers](https://docs.envio.dev/docs/HyperIndex/block-handlers)
- [Multichain indexing](https://docs.envio.dev/docs/HyperIndex/multichain-indexing)

</td>
<td valign="top">

**Running in production**
- [Envio Cloud](https://docs.envio.dev/docs/HyperIndex/hosted-service)
- [Pricing and billing](https://docs.envio.dev/docs/HyperIndex/hosted-service-billing)
- [Self-hosting](https://docs.envio.dev/docs/HyperIndex/self-hosting)
- [API tokens](https://docs.envio.dev/docs/HyperSync/api-tokens)
- [Licensing](https://docs.envio.dev/docs/HyperIndex/licensing)

</td>
</tr>
</table>

## FAQ

<details>
<summary><b>Product</b></summary>
<br>

<details>
<summary>What is HyperIndex used for?</summary>

HyperIndex turns smart contract events into a real-time GraphQL API. You choose the contracts and events, write TypeScript handlers that shape the data, and HyperIndex keeps it up to date and handles chain reorganisations. Teams use it for dashboards, protocol analytics and any app that needs structured onchain data. See the [HyperIndex overview](https://docs.envio.dev/docs/HyperIndex/overview).

</details>

<details>
<summary>What is HyperSync?</summary>

HyperSync is Envio's blockchain data API and the data layer behind HyperIndex. It queries logs, transactions, blocks and traces, filtered on the server, and is up to 2,000x faster than JSON-RPC. Official clients are available for Rust, Python, Node.js and Go. See the [HyperSync docs](https://docs.envio.dev/docs/HyperSync/overview).

</details>

<details>
<summary>What is HyperRPC?</summary>

HyperRPC is a read-only JSON-RPC endpoint built on HyperSync. It is up to 5x faster than geth, erigon and reth for data-heavy reads such as `eth_getLogs`, and existing RPC tools can point at it without code changes. See the [HyperRPC docs](https://docs.envio.dev/docs/HyperRPC/overview-hyperrpc).

</details>

<details>
<summary>How does Envio's performance compare?</summary>

HyperIndex is 6–879x faster in the [open indexer benchmark](https://github.com/enviodev/open-indexer-benchmark). Every number there comes from code in the repository, which you can run yourself, and scheduled CI keeps the results current.

</details>

<details>
<summary>Can one indexer cover several chains?</summary>

Yes. A single HyperIndex indexer can index contracts on several chains and serve all of the data from one GraphQL API. See [multichain indexing](https://docs.envio.dev/docs/HyperIndex/multichain-indexing).

</details>

</details>

<details>
<summary><b>Chains</b></summary>
<br>

<details>
<summary>Which chains are supported?</summary>

Any EVM chain. HyperSync runs natively on every network in the [supported networks list](https://docs.envio.dev/docs/HyperSync/hypersync-supported-networks), and other EVM chains work over RPC. [Solana](https://docs.envio.dev/docs/HyperIndex/solana) (new) and [Fuel](https://docs.envio.dev/docs/HyperIndex/fuel) are supported too.

</details>

<details>
<summary>How does Solana support work?</summary>

Solana indexing runs on [HyperSync for Solana](https://docs.envio.dev/docs/HyperSync/solana). Handlers match program instructions with `indexer.onInstruction` and decode them with your Anchor IDL, and `indexer.onSlot` covers per-slot logic. Solana indexers are TypeScript only. See the [Solana docs](https://docs.envio.dev/docs/HyperIndex/solana).

</details>

<details>
<summary>Are transaction traces supported?</summary>

Yes, on the chains with trace endpoints listed in [supported networks](https://docs.envio.dev/docs/HyperSync/hypersync-supported-networks), including Ethereum, Base and Gnosis. Trace data is an add-on on the [HyperSync pricing page](https://envio.dev/pricing/hypersync).

</details>

</details>

<details>
<summary><b>Hosting and pricing</b></summary>
<br>

<details>
<summary>Can I self-host HyperIndex?</summary>

Yes. Run it on your own infrastructure with Docker, using the [self-hosting guide](https://docs.envio.dev/docs/HyperIndex/self-hosting). Self-hosted indexers need an [API token](https://docs.envio.dev/docs/HyperSync/api-tokens) for HyperSync access.

</details>

<details>
<summary>Do I need an API token?</summary>

Yes, for HyperSync access in local development and self-hosted deployments. `envio init` can open the token page and write the token to your project. See [API tokens](https://docs.envio.dev/docs/HyperSync/api-tokens).

</details>

<details>
<summary>What are the limits on the free development plan?</summary>

Deployments are deleted when they exceed 20GB of storage or are older than 30 days. A two-stage deletion process starts when a deployment reaches 100,000 events processed, 5GB of storage, or 7 days without requests. See [pricing and billing](https://docs.envio.dev/docs/HyperIndex/hosted-service-billing) and [plans](https://envio.dev/pricing).

</details>

<details>
<summary>Is there a discount for paying yearly?</summary>

Yes. Production plans can be billed yearly at a lower price than paying month to month, and Dedicated plans are custom priced. See [hosting pricing](https://envio.dev/pricing/hosting).

</details>

</details>

<details>
<summary><b>Enterprise</b></summary>
<br>

<details>
<summary>Is there an SLA?</summary>

Yes. Dedicated plans come with a written SLA, with options up to 99.99% uptime backed by service credits, plus 24/7 on-call support. [Compare plans and contact sales](https://envio.dev/pricing).

</details>

<details>
<summary>Can Envio migrate our subgraphs?</summary>

Yes. Envio can migrate and host your subgraphs with Subgraph Hosting, or you can port them yourself with the [migration guide](https://docs.envio.dev/docs/HyperIndex/migration-guide) or [with AI](https://docs.envio.dev/docs/HyperIndex/migrate-with-ai).

</details>

<details>
<summary>Can Envio engineers help on our project?</summary>

Yes. Envio engineers can work on your project for migrations, performance tuning, architecture reviews and dedicated engineering hours. See [services](https://envio.dev/pricing/services).

</details>

</details>

---

<p align="center">
  <a href="https://envio.dev">Website</a> ·
  <a href="https://docs.envio.dev">Docs</a> ·
  <a href="https://discord.gg/envio">Discord</a> ·
  <a href="https://t.me/+BeS5ihVUFONjNGFk">Telegram</a> ·
  <a href="https://twitter.com/envio_indexer">X</a> ·
  <a href="https://www.youtube.com/@envio_indexer">YouTube</a> ·
  <a href="https://envio.beehiiv.com/subscribe">Newsletter</a>
</p>
<p align="center"><sub>Questions? Ask on <a href="https://discord.gg/envio">Discord</a> or <a href="https://t.me/+BeS5ihVUFONjNGFk">Telegram</a>. Contributions start with an <a href="https://github.com/enviodev/hyperindex/issues">issue</a>. See <a href="https://docs.envio.dev/docs/HyperIndex/licensing">licensing</a> for terms.</sub></p>
