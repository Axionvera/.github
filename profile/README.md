<div align="center">

# Axionvera

### Programmable rewards for businesses, fintechs, startups, and the agents who help them grow.

Axionvera enables organisations to create reward campaigns, define qualifying actions, verify agent activity, and distribute rewards through Stellar.

<br />

![Built on Stellar](https://img.shields.io/badge/Built%20on-Stellar-7B61FF?style=for-the-badge)
![Smart Contracts](https://img.shields.io/badge/Smart%20Contracts-Soroban-000000?style=for-the-badge)
![SDK](https://img.shields.io/badge/SDK-TypeScript-3178C6?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active%20Development-0E8A16?style=for-the-badge)

<br />

**Create campaigns. Verify activity. Reward agents.**

</div>

---

## What is Axionvera?

Axionvera is a programmable rewards platform for businesses, fintechs, and startups that work with agents, partners, referrers, field teams, ambassadors, contractors, or other performance-based contributors.

A business can use Axionvera to:

- create and fund a reward campaign;
- define the activities it wants to incentivise;
- set reward amounts and limits;
- authorise trusted verifiers;
- verify when an agent completes a qualifying action;
- allocate rewards to that agent;
- allow agents to view and claim what they have earned;
- track campaign activity through on-chain events.

The goal is to make agent reward programmes easier to operate, easier to verify, and more transparent.

---

## The Problem

Many businesses depend on agents to drive growth.

These agents may:

- onboard merchants;
- acquire customers;
- make referrals;
- complete field tasks;
- support distribution;
- promote products;
- drive transactions;
- activate new users;
- complete sales milestones;
- perform other measurable activities.

But rewarding them can quickly become operationally difficult.

Businesses often have to manage:

- spreadsheets;
- manual approvals;
- fragmented payment processes;
- unclear reward calculations;
- delayed payouts;
- duplicated claims;
- difficult reconciliation;
- limited transparency for agents;
- internal disputes over whether an action was completed.

As agent networks grow, these problems become harder to manage.

Axionvera is designed to provide a programmable system for handling that process.

---

## How Axionvera Works

The core Axionvera flow is simple:

```text
Business / Fintech / Startup
            │
            ▼
   Create Reward Campaign
            │
            ▼
 Define Qualifying Actions
            │
            ▼
       Fund Campaign
            │
            ▼
 Agent Performs an Action
            │
            ▼
 Trusted Verifier Confirms It
            │
            ▼
      Reward Is Allocated
            │
            ▼
       Agent Claims Reward
            │
            ▼
      Settlement on Stellar
```

The business controls the campaign.

The verifier confirms whether an eligible activity occurred.

The agent receives the resulting reward.

The smart contract keeps the campaign accounting and reward state consistent.

---

## Example

A fintech wants to grow its merchant network.

It creates a campaign with the following rule:

> Onboard a verified merchant and earn 5 USDC.

The campaign flow could look like this:

```text
Fintech
  │
  ├── Creates campaign
  ├── Funds campaign
  ├── Defines "Verified Merchant" reward = 5 USDC
  └── Authorises verifier
              │
              ▼
        Agent onboards merchant
              │
              ▼
        Merchant is verified
              │
              ▼
       5 USDC reward allocated
              │
              ▼
           Agent claims
```

The same model can support many other forms of performance-based incentives.

---

## Who Axionvera Is For

### Businesses

Companies running field, referral, sales, distribution, merchant, or partner programmes can create structured reward campaigns without managing every reward manually.

### Fintechs

Fintech platforms can use campaigns to reward agents who acquire merchants, activate customers, facilitate transactions, complete KYC-related workflows, or drive adoption.

### Startups

Early-stage companies can launch incentive programmes without building a complete campaign, reward-accounting, wallet, and settlement system from scratch.

### Agent Networks

Organisations managing large numbers of independent agents can use Axionvera as a transparent reward layer between verified activity and payout.

---

## Possible Use Cases

Axionvera's campaign model can support a wide range of incentive programmes.

| Use Case | Example Reward |
|---|---|
| Merchant acquisition | Reward an agent after a merchant is successfully onboarded |
| Customer referrals | Reward a referrer after the referred customer completes a qualifying action |
| Field sales | Reward representatives for verified sales milestones |
| Distribution | Reward agents for successful product distribution |
| Fintech adoption | Reward agents for activating customers or merchants |
| Community programmes | Reward ambassadors for approved community activities |
| Affiliate programmes | Reward partners for verified conversions |
| Gig or task networks | Reward workers for successfully completed tasks |
| Transaction incentives | Reward agents for driving qualifying transaction activity |
| Growth campaigns | Reward measurable actions tied to business objectives |

The qualifying activity does not need to happen directly on-chain.

An authorised verifier can confirm that the activity occurred before the reward is allocated.

---

## Why Stellar?

Axionvera uses Stellar as the settlement and programmable-finance layer beneath the product.

Stellar provides infrastructure suited to reward distribution, including:

- fast transaction settlement;
- low transaction costs;
- support for digital assets;
- global account-based payments;
- programmable smart contracts through Soroban;
- transparent transaction history;
- contract events;
- infrastructure that can support cross-border reward programmes.

For Axionvera, Stellar is not the user experience.

It is the infrastructure underneath the user experience.

A business should be able to focus on:

```text
Who should be rewarded?
What action should they complete?
How much should they earn?
Who is allowed to verify it?
```

while Axionvera handles the underlying campaign and settlement logic.

---

## Campaigns

Campaigns are the core primitive of Axionvera.

A campaign can contain:

- a campaign administrator;
- a reward asset;
- a campaign name;
- a start time;
- an end time;
- a maximum reward per agent;
- campaign funding;
- one or more activation rules;
- authorised verifiers;
- agent reward allocations;
- claims;
- unused campaign funds.

Campaigns can also move through a controlled lifecycle.

```text
Active
  │
  ├── Pause
  │     │
  │     └── Resume
  │
  └── Close
```

This gives businesses control over when reward allocation is allowed while preserving valid rewards that have already been earned.

---

## Activation Rules

Businesses define the activities they want to reward through activation rules.

An activation rule links a named milestone to a reward amount.

For example:

```text
Campaign:
Merchant Growth Q4

Rules:
Verified Merchant       → 5 USDC
First 10 Transactions   → 10 USDC
Premium Merchant        → 20 USDC
```

When an authorised verifier confirms that an agent has completed one of those milestones, the corresponding reward can be allocated.

This makes the reward logic explicit rather than relying entirely on manual calculations.

---

## Verifiers

Not every participant should be allowed to allocate rewards.

Axionvera therefore separates the **agent** from the **verifier**.

A verifier is an authorised party that confirms whether a qualifying action has occurred.

Depending on the business, a verifier could be:

- an internal operations team;
- a sales manager;
- a backend service;
- an application server;
- an approved partner;
- another trusted system.

This creates a clear flow:

```text
Agent performs action
        │
        ▼
Verifier checks action
        │
        ▼
Contract allocates reward
        │
        ▼
Agent claims reward
```

The business determines who is trusted to perform verification.

---

## Agent Rewards

Agents can accumulate rewards across verified activities.

Axionvera tracks:

- the amount currently claimable by an agent;
- the total amount the agent has earned;
- campaign-level reward limits;
- allocated campaign funds;
- claimed rewards.

This makes it possible to separate:

```text
Reward earned
```

from:

```text
Reward claimed
```

An agent can therefore receive allocations over time and claim them according to the application's user experience.

---

## Campaign Accounting

Campaign funds are tracked explicitly.

At a high level:

```text
Funded Amount
      │
      ├── Allocated Rewards
      │
      └── Unused Funds
```

Businesses can determine how much funding remains available for new reward allocations.

After the appropriate campaign state is reached, unused funds can also be withdrawn.

This provides a clearer accounting model than simply sending rewards from an uncontrolled operational wallet.

---

## Axionvera Technology

The product experience is supported by several technical layers.

```text
Business / Agent Applications
            │
            ▼
     Axionvera Interfaces
            │
            ▼
       Axionvera SDK
            │
            ▼
   Campaign Smart Contract
            │
            ▼
      Stellar / Soroban
```

These layers are intentionally separated.

The application handles the user experience.

The SDK handles integration.

The smart contract handles campaign state, accounting, permissions, and rewards.

Stellar handles settlement.

---

## Axionvera SDK

Axionvera includes a TypeScript SDK designed to make the underlying Stellar infrastructure easier to use from applications.

The SDK currently supports:

- typed Campaign contract interfaces;
- live Soroban reads;
- live Soroban writes;
- transaction preparation;
- transaction simulation;
- wallet signing;
- signed transaction submission;
- contract-specific error handling;
- typed Campaign events;
- live RPC event retrieval;
- cursor and ledger-based event queries;
- campaign helper utilities;
- React hooks;
- wallet and application integration utilities;
- test and mock infrastructure.

The SDK exists to support the Axionvera product and make future integrations easier.

It also means applications do not need to interact directly with raw Soroban values for every operation.

---

## Current Campaign Contract Coverage

The current Campaign integration covers the complete public contract interface.

### Reads

```text
get_campaign
get_activation_rule
is_verifier
claimable_reward
agent_total_earned
available_unused_funds
is_initialized
protocol_admin
next_campaign_id
```

### Writes

```text
initialize
create_campaign
fund_campaign
add_activation_rule
add_verifier
remove_verifier
pause_campaign
resume_campaign
close_campaign
withdraw_unused_funds
verify_and_allocate_reward
claim_reward
```

That gives the current Campaign system:

- **9 read operations**
- **12 write operations**
- **21 public contract methods**

---

## Campaign Events

Axionvera also emits and consumes Campaign lifecycle events.

Current event coverage includes:

```text
campaign initialized
campaign created
campaign funded
activation rule added
verifier added
verifier removed
reward allocated
reward claimed
campaign paused
campaign resumed
campaign closed
unused funds withdrawn
```

Events make it possible for applications to build:

- activity feeds;
- campaign histories;
- agent dashboards;
- business reporting;
- notifications;
- analytics;
- indexing systems;
- audit trails.

---

## Testnet Validation

The Campaign system has been exercised against Stellar testnet through an end-to-end lifecycle.

The verified flow included:

1. contract initialization;
2. campaign creation;
3. campaign funding;
4. activation-rule creation;
5. verifier addition;
6. reward verification and allocation;
7. agent reward claiming;
8. campaign pause;
9. campaign resume;
10. campaign close;
11. unused-fund withdrawal;
12. post-transaction state reads;
13. live RPC event retrieval;
14. typed Campaign event decoding.

The objective is to validate Axionvera against the network itself rather than relying only on mocked contract interactions.

---

## Current Development Focus

Axionvera is currently focused on turning the underlying Campaign infrastructure into a complete product experience.

Current priorities include:

### Business experience

- campaign creation;
- campaign funding;
- activation-rule management;
- verifier management;
- campaign monitoring;
- campaign lifecycle controls;
- reward and fund reporting.

### Agent experience

- campaign discovery;
- earned reward visibility;
- claimable reward visibility;
- reward claiming;
- reward history.

### Verification

- simple verifier workflows;
- secure reward allocation;
- clear links between verified activities and resulting rewards.

### Infrastructure

- stronger transaction lifecycle handling;
- improved wallet experience;
- richer event indexing;
- additional integration tooling;
- production readiness.

---

## Product Direction

The longer-term product is intended to make campaign creation feel much simpler than the underlying blockchain architecture.

A business should eventually be able to configure something like:

```text
Campaign
─────────────────────────────

Name:
Merchant Expansion Campaign

Reward asset:
USDC

Campaign budget:
10,000 USDC

Start:
1 October

End:
31 December

Per-agent cap:
500 USDC

Reward rules:
✓ Merchant onboarded       5 USDC
✓ Merchant activated      10 USDC
✓ 100 transactions        25 USDC

Verifiers:
✓ Operations API
✓ Regional Manager
```

The contract and SDK handle the technical mechanics underneath.

The business interacts with the campaign.

---

## Why Axionvera Exists

The idea behind Axionvera is straightforward:

> Businesses should be able to reward people for measurable contributions without building an entire reward infrastructure from scratch.

Today, many agent-based reward systems depend heavily on internal operations.

Axionvera is exploring a model where:

- the campaign rules are explicit;
- the budget is visible;
- verification is permissioned;
- rewards are accounted for programmatically;
- agents can see what they have earned;
- settlement can happen through Stellar.

The aim is not to put unnecessary blockchain complexity in front of businesses.

The aim is to use blockchain infrastructure where it can improve the reward system underneath.

---

## What Makes Axionvera Different?

Axionvera is not intended to be only a generic token distribution tool.

The product is centred around the relationship between:

```text
Business
   │
   ▼
Campaign
   │
   ▼
Agent Activity
   │
   ▼
Verification
   │
   ▼
Reward
```

That creates several important product concepts:

### Campaign-based

Rewards belong to defined programmes with their own budgets, rules, timelines, and administrators.

### Agent-based

Reward history and limits can be tracked per agent.

### Verification-based

Completing an action does not automatically mean a reward is valid. An authorised verifier confirms the activity.

### Rule-based

Businesses define what is rewarded and how much it is worth.

### Programmable

Campaign accounting and reward allocation are enforced through Soroban contracts.

### Integratable

The Axionvera SDK provides application-facing APIs for integrating campaigns into business products.

---

## Roadmap

### Phase 1 — Campaign Infrastructure

- Campaign Soroban contract
- Typed Core SDK
- Live reads and writes
- Wallet signing
- Transaction submission
- Contract errors
- Campaign events
- React hooks
- Testnet validation

### Phase 2 — Product Experience

- Business campaign dashboard
- Agent dashboard
- Verifier interface
- Campaign analytics
- Reward history
- Wallet onboarding
- Improved claim experience

### Phase 3 — Integrations

- Business APIs
- Webhooks and event delivery
- Backend verification integrations
- Payment and fintech integrations
- External application SDK adoption

### Phase 4 — Production Growth

- Mainnet deployment
- Production campaign pilots
- Business onboarding
- Agent network pilots
- Usage analytics
- Security reviews
- Expanded financial integrations

---

## Origins

Axionvera began with a strong open-source focus.

Early development emphasised:

- contributor-friendly repositories;
- reusable architecture;
- testing;
- documentation;
- clear issues;
- maintainable code;
- transparent engineering.

That foundation helped shape the way Axionvera is built today.

The project has since moved into a more focused product-development phase, with its core infrastructure, contracts, SDK, integrations, and product direction being developed directly around the Axionvera vision.

Open development remains part of the project's history and engineering culture.

The focus now is building and validating the product.

---

## Engineering Principles

### Product first

Technical infrastructure should support a real business workflow rather than exist only for its own sake.

### Simple user experience

Businesses and agents should not need to understand Soroban internals to use Axionvera.

### Clear accounting

Campaign funding, allocations, claims, and unused balances should be explicit.

### Controlled verification

Only authorised parties should be able to approve reward-triggering actions.

### Reusable infrastructure

The same underlying campaign architecture should be capable of supporting many business use cases.

### Test what matters

Contract behaviour, transaction flows, errors, events, and integration boundaries should have strong regression protection.

### Validate on Stellar

Where practical, important workflows should be exercised against Stellar testnet in addition to local tests.

---

## Vision

Axionvera's long-term vision is to become a reward infrastructure platform for businesses operating agent-driven growth models.

A company should be able to say:

> We want to reward these people for these actions.

Axionvera should handle the rest:

```text
Campaign Creation
       ↓
Funding
       ↓
Rules
       ↓
Verification
       ↓
Reward Allocation
       ↓
Agent Claim
       ↓
Settlement
```

The underlying technology can be sophisticated.

The product experience should not be.

---

<div align="center">

## Reward the people who help your business grow.

Create campaigns.  
Verify meaningful activity.  
Reward agents transparently.

<br />

**Axionvera — programmable agent rewards, powered by Stellar.**

</div>
