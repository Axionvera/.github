<div align="center">

# Axionvera

### Infrastructure for programmable finance on Stellar.

Axionvera is building developer infrastructure, financial primitives, SDKs, and application tooling for teams building on Stellar and Soroban.

Our focus is making it easier to build reliable financial applications without repeatedly rebuilding contract integrations, transaction flows, wallet handling, event infrastructure, and application-facing SDK layers.

<br />

![Stellar](https://img.shields.io/badge/Built%20on-Stellar-7B61FF?style=for-the-badge)
![Soroban](https://img.shields.io/badge/Smart%20Contracts-Soroban-000000?style=for-the-badge)
![TypeScript](https://img.shields.io/badge/SDK-TypeScript-3178C6?style=for-the-badge)
![Rust](https://img.shields.io/badge/Contracts-Rust-DEA584?style=for-the-badge)

<br />

**Build financial products. Integrate faster. Ship on Stellar.**

</div>

---

## What is Axionvera?

Axionvera is a growing infrastructure layer for digital-finance applications built on Stellar.

The project focuses on the technical components that repeatedly appear when building real applications on top of smart contracts:

- typed contract interfaces
- transaction preparation and submission
- wallet signing
- Soroban RPC integration
- contract error handling
- event retrieval and decoding
- reusable application SDKs
- React integrations
- payment and reward workflows
- developer-facing infrastructure

Instead of every application implementing these systems independently, Axionvera aims to provide reusable building blocks that can support multiple financial products.

---

## The Problem

Building an application on-chain involves much more than writing a smart contract.

A production application also needs to handle:

- wallet connections
- transaction construction
- simulation
- signing
- submission
- confirmation
- RPC communication
- contract errors
- event parsing
- frontend state
- application-specific abstractions

These layers are often rebuilt for every project.

That creates duplicated work, inconsistent implementations, and more surface area for errors.

Axionvera is building infrastructure that reduces that duplication.

---

## What We Are Building

Axionvera is developing a set of interoperable components around Stellar and Soroban.

| Layer | Purpose |
|---|---|
| Smart Contracts | Financial primitives and application logic deployed through Soroban |
| Axionvera SDK | Typed TypeScript interfaces for interacting with contracts and Stellar infrastructure |
| Transaction Infrastructure | Preparation, simulation, signing, submission, and transaction lifecycle handling |
| Event Infrastructure | Typed Soroban event decoding, retrieval, and pagination |
| Wallet Infrastructure | Wallet-independent signing and connection abstractions |
| React Integration | Hooks and providers for application developers |
| Financial Modules | Payments, campaigns, incentives, rewards, and other programmable-finance workflows |
| Developer Tooling | Testing, compatibility checks, mocks, configuration, and integration utilities |

These components are designed to work independently while sharing common infrastructure.

---

## Axionvera SDK

The Axionvera SDK is currently the most developed infrastructure layer within the ecosystem.

It is a TypeScript SDK for applications interacting with Stellar and Soroban.

The SDK currently provides infrastructure for:

- typed smart-contract interfaces
- live Soroban contract reads
- Soroban transaction preparation
- transaction simulation
- wallet signing
- signed transaction submission
- transaction result handling
- contract-specific errors
- Soroban event decoding
- live RPC event retrieval
- event pagination
- React hooks
- reusable contract helpers
- network configuration
- testing and mocking infrastructure

The objective is to give application developers a higher-level interface while preserving access to lower-level Stellar primitives when needed.

---

## Campaign Infrastructure

One of the first complete vertical integrations built on top of the SDK is the Axionvera Campaign system.

Campaigns provide programmable infrastructure for distributing rewards based on verifiable user activity.

A campaign can define:

- a campaign administrator
- a reward asset
- a campaign duration
- reward rules
- authorised verifiers
- per-agent reward limits
- allocated rewards
- claimed rewards
- remaining campaign funds

This creates a reusable primitive for applications that need incentive programmes, referral systems, merchant campaigns, user rewards, or activity-based distributions.

### Current Campaign SDK Coverage

The Campaign integration currently covers the complete public contract interface:

**21 contract methods**

- 9 read methods
- 12 write methods

It also includes:

- 27 mapped contract error conditions
- 12 typed event variants
- live Stellar RPC event retrieval
- ledger-range event queries
- cursor-based pagination
- reward accounting helpers
- React read hooks
- React transaction hooks
- wallet signing
- transaction submission

---

## Testnet Progress

The Campaign stack has been exercised end-to-end against Stellar testnet.

The verified lifecycle includes:

1. Contract initialization
2. Campaign creation
3. Campaign funding
4. Activation-rule creation
5. Verifier registration
6. Reward verification and allocation
7. Agent reward claiming
8. Campaign pause
9. Campaign resume
10. Campaign close
11. Withdrawal of unused campaign funds
12. Post-transaction state reads
13. Live RPC event retrieval
14. Typed event decoding

The same lifecycle produced contract events that were retrieved directly through Stellar RPC and decoded through the Axionvera SDK.

This moves the SDK beyond interface definitions and mocks into live Soroban integration.

---

## Built Around Stellar

Stellar is the primary blockchain environment for Axionvera's current financial infrastructure work.

Axionvera uses Stellar for:

- asset movement
- account-based transactions
- programmable payments
- smart contracts through Soroban
- contract events
- application settlement
- financial application infrastructure

Soroban provides the programmable layer used by Axionvera contracts, while Stellar provides the surrounding network, asset, account, and transaction infrastructure.

Axionvera's SDK is intended to make those capabilities easier to integrate into real applications.

---

## Architecture

Axionvera follows a layered architecture.

```text
Applications
     │
     ▼
React / Product Integrations
     │
     ▼
Axionvera SDK
     │
     ├── Contract APIs
     ├── Transaction Infrastructure
     ├── Wallet Integration
     ├── Event Infrastructure
     └── Network Utilities
     │
     ▼
Stellar RPC + Soroban
     │
     ▼
Axionvera Smart Contracts
```

The goal is to keep contract logic, network transport, wallet interactions, and application state separated.

This allows each layer to evolve without tightly coupling the entire stack.

---

## Core Projects

<table>
  <tr>
    <td width="33%" valign="top">
      <h3>Axionvera SDK</h3>
      <p>
        Developer infrastructure for interacting with Stellar, Soroban, and
        Axionvera contracts.
      </p>
      <ul>
        <li>Typed contract APIs</li>
        <li>Live Soroban reads and writes</li>
        <li>Wallet signing</li>
        <li>Transaction submission</li>
        <li>Event infrastructure</li>
        <li>React integrations</li>
      </ul>
    </td>
    <td width="33%" valign="top">
      <h3>Axionvera Contracts</h3>
      <p>
        Soroban smart contracts providing reusable financial and application
        primitives.
      </p>
      <ul>
        <li>Campaigns</li>
        <li>Rewards</li>
        <li>Financial primitives</li>
        <li>Contract events</li>
        <li>Access control</li>
        <li>Application integrations</li>
      </ul>
    </td>
    <td width="33%" valign="top">
      <h3>Axionvera Applications</h3>
      <p>
        Products and interfaces built on top of the infrastructure layer.
      </p>
      <ul>
        <li>Financial applications</li>
        <li>Wallet experiences</li>
        <li>Dashboards</li>
        <li>Payment workflows</li>
        <li>Campaign interfaces</li>
        <li>Developer tools</li>
      </ul>
    </td>
  </tr>
</table>

---

## Engineering Approach

Axionvera is being developed with an emphasis on infrastructure that can survive beyond a prototype.

### Typed interfaces

Contract interactions should expose predictable TypeScript interfaces rather than requiring applications to work directly with raw Soroban values.

### Separation of concerns

Contract interaction, transaction submission, wallet signing, events, and frontend state are implemented as separate layers.

### Real-network validation

Where possible, SDK functionality is tested not only through mocks but also against deployed Stellar testnet contracts.

### Regression protection

New infrastructure is accompanied by tests covering successful operations, validation behaviour, contract failures, and integration boundaries.

### Reusable primitives

Infrastructure developed for one contract should be reusable when integrating future contracts.

---

## Current Development

Core development of Axionvera is currently being driven directly through the project rather than primarily through external contributor activity.

Recent development has focused on establishing the underlying Stellar infrastructure required for more complex products.

Major areas completed or under active development include:

- live Soroban reads
- live Soroban writes
- transaction preparation
- wallet signing
- transaction submission
- transaction lifecycle handling
- typed contract errors
- contract event infrastructure
- live RPC event queries
- React integrations
- complete Campaign contract support

The Campaign integration alone is covered as part of a repository regression suite containing more than 700 passing tests.

---

## Roadmap

Axionvera's next phase is focused on moving from foundational infrastructure toward broader product integrations.

### Infrastructure

- Extend live SDK support to additional contracts
- Improve transaction lifecycle and confirmation handling
- Expand contract event infrastructure
- Improve wallet integrations
- Continue strengthening SDK reliability and developer experience

### Financial primitives

- Expand campaign and reward infrastructure
- Build additional reusable financial modules
- Support richer payment and settlement workflows
- Explore additional programmable-finance use cases

### Application layer

- Build product interfaces around the SDK
- Improve React integrations
- Develop reusable wallet and transaction UX
- Connect financial primitives into complete user workflows

### Production readiness

- Expand network integration testing
- Strengthen observability and failure handling
- Improve compatibility testing
- Prepare selected infrastructure for production deployment

---

## Origins

Axionvera began as an open-source initiative focused heavily on contribution, experimentation, and creating well-structured repositories that developers could learn from and improve.

That period helped establish many of the project's engineering principles:

- clear module boundaries
- strong documentation
- meaningful tests
- maintainable architecture
- transparent development
- reusable infrastructure

The project has since evolved.

Today, Axionvera is increasingly focused on building its own infrastructure and products, with development driven directly by the project and a stronger emphasis on Stellar-based financial systems.

The open-source foundation remains important, but it is no longer the defining purpose of Axionvera.

It is part of how the project was built.

---

## Why Axionvera?

Axionvera's long-term thesis is simple:

> Financial applications should not have to rebuild the same blockchain infrastructure every time they launch.

Smart contracts are only one layer of a working financial product.

Wallets, transactions, errors, events, frontend integrations, network communication, and reusable developer interfaces are equally important.

Axionvera is building those layers together.

---

## Vision

The long-term goal is to create a reusable infrastructure stack for financial applications built on Stellar.

A developer should be able to use Axionvera to move from:

```text
Smart Contract
```

to:

```text
Smart Contract
      ↓
Typed SDK
      ↓
Wallet + Transactions
      ↓
Events + Application State
      ↓
Production Application
```

without rebuilding each integration layer from scratch.

As the ecosystem develops, Axionvera aims to support increasingly sophisticated applications across:

- payments
- rewards
- incentives
- programmable financial workflows
- asset infrastructure
- financial applications
- developer platforms

---

<div align="center">

## Building on Stellar

Axionvera is building the infrastructure between smart contracts and real financial applications.

<br />

**Programmable finance. Developer infrastructure. Built on Stellar.**

</div>
