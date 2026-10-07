# CognoKratos Curriculum

CognoKratos is a living engineering curriculum for trustworthy autonomous agents.

The current projects are **the present state of the curriculum**, not the permanent definition of it. New engineering problems will appear as autonomous systems gain more authority. The community should be able to extend, refine, or replace parts of this map as our collective understanding improves.

## Graduate outcome

After working through the curriculum, an engineer should be able to design, implement, and critically evaluate autonomous agent systems that exercise real capabilities — including economic and cryptographic capabilities — while preserving explicit authority boundaries, deterministic governance, recoverability, auditability, and meaningful human control.

The core transformation is:

> **From building agents to engineering trust around autonomous actors.**

## Competency map

A CognoKratos graduate should be able to reason about and implement the following areas.

| Competency | Graduate capability |
| --- | --- |
| Agent systems thinking | Treat the LLM as one probabilistic component inside a larger deterministic system. |
| Threat modelling | Identify actors, assets, trust boundaries, attack surfaces, privilege escalation paths, and failure modes. |
| Identity | Distinguish users, agents, services, and organizations and reason about authentication between them. |
| Authority & authorization | Model who may perform which operation, under what conditions, and why. |
| Capability engineering | Expose narrow operations rather than broad credentials or infrastructure access. |
| Runtime durability | Reason about runs, threads, checkpoints, persistence, crashes, retries, and side effects. |
| Deterministic governance | Keep rules and policy in software that can be specified, tested, and verified. |
| Evidence & auditability | Preserve enough evidence to explain and reconstruct consequential actions. |
| Human authority | Place approval and override boundaries where the model cannot bypass or manufacture them. |
| Observability & evaluation | Inspect traces, evaluate behaviour, and distinguish model quality from system correctness. |
| Secrets & cryptography | Keep sensitive material outside model context and expose constrained cryptographic capabilities. |
| Blockchain literacy | Understand when signatures, smart contracts, decentralized state, and settlement change the trust model. |
| Economic agency | Design autonomous participation in financial workflows involving intent, approval, idempotency, reconciliation, and settlement. |
| Sovereignty & decentralization | Recognize where centralized trust is necessary, where it is merely convenient, and where verification can replace it. |
| Compositional design | Combine identity, capabilities, policy, runtime, cryptography, audit, and settlement into one coherent trust architecture. |

## Current curriculum

### Part I — Production Agent Engineering

**Reference project:** [`simple-agent-template`](https://github.com/cognokratos/simple-agent-template)

**Question:** How is a production agent engineered around an untrusted probabilistic component?

**Primary competencies:**

- agent loops and tool calling;
- MCP as a capability boundary;
- grounding and authoritative state;
- guardrails and deterministic controls;
- evaluation;
- observability;
- authentication and trust boundaries;
- controlled mutation and human approval.

**Core lesson:**

> **Intelligence does not imply authority.**

The model may reason and request actions. Identity, authorization, mutation, and audit remain outside the model.

### Part II — Durable Agent Runtime Engineering

**Reference project:** [`sophos-agent`](https://github.com/cognokratos/sophos-agent)

**Question:** Once an agent can act, how does it become durable software that survives time, state, crashes, and restarts?

**Primary competencies:**

- resource and process ownership;
- runtime state vs product state;
- durability boundaries;
- checkpoints and resume semantics;
- streaming vs persistence;
- memory types;
- replay and side effects;
- idempotency;
- local-first ownership.

**Core lesson:**

> **Recoverable execution is not the same thing as exactly-once execution.**

### Part III — Governed Decision Engineering

**Reference project:** [`etf-research-agent`](https://github.com/cognokratos/etf-research-agent)

**Question:** How do we place deterministic policy, evidence, and human authority around probabilistic reasoning?

**Primary competencies:**

- policy as code/data;
- uncertainty and missing data;
- evidence contracts;
- domain modelling before agent design;
- recommendation vs authority;
- human consent and override;
- policy-versioned audit;
- system-level evaluation.

**Core lesson:**

> **The model can reason about a decision without owning the decision.**

### Part IV — Cryptographic Capability Engineering

**Reference project:** [`arktos-wallet`](https://github.com/cognokratos/arktos-wallet)

**Question:** How can autonomous software request cryptographic capability without becoming the custodian of cryptographic authority?

**Primary competencies:**

- custody models;
- key hierarchy;
- secret lifetimes;
- deterministic derivation;
- encryption boundaries;
- identity bound to capability;
- least-capability tool design;
- recovery.

**Core lesson:**

> **Give agents capabilities, never secrets.**

Arktos currently derives public addresses only. It deliberately does not sign or broadcast transactions. That boundary is part of the curriculum, not a defect to hide.

### Part V — Agentic Financial Workflow Engineering

**Reference project:** [`tauros-revenue`](https://github.com/cognokratos/tauros-revenue)

**Question:** How can agents perform financial work while humans retain financial authority?

**Primary competencies:**

- humans and agents as distinct actors;
- ownership and domain authorization;
- financial intent;
- immutable revisions;
- state machines;
- idempotency and retries;
- exact-payload approval;
- concurrency;
- reviewed AI capability surfaces;
- audit and supervision.

**Core lesson:**

> **AI capability is not financial authority.**

### Part VI — Connecting the Architectures

**Reference:** The CognoKratos Book

**Question:** How do the previous layers combine into a trustworthy autonomous system?

**Primary competencies:**

- capability vs permission vs authority;
- runtime state vs domain state vs audit history;
- approval boundaries;
- idempotency, replay, concurrency, and recovery;
- technology choices following trust boundaries;
- composition of the five architectures.

**Core lesson:**

> **Trust comes from the composition of explicit boundaries, not from the model alone.**

## Current coverage and gaps

The following table is intentionally public-facing. A gap is an invitation to research and contribute, not an admission that the current curriculum has failed.

| Competency | Current coverage | State |
| --- | --- | --- |
| Probabilistic model boundaries | Parts I, III, V | Strong |
| Threat modelling | Parts I, II, IV | Strong but fragmented |
| Application identity & authentication | Parts I, IV, V | Strong |
| Capability engineering | Parts I, IV, V | Very strong |
| Runtime durability & recovery | Parts II, V | Strong |
| Idempotency & concurrency | Parts II, V, VI | Strong |
| Deterministic governance | Parts III, V | Very strong |
| Evidence & provenance | Parts III, V | Strong |
| Human authority | Parts I, III, V | Very strong |
| Observability & evaluation | Parts I, III | Strong but not universal |
| Secret and key isolation | Part IV | Strong |
| Cryptographic authority | Part IV | Partial — signing deliberately absent |
| Economic intent/workflows | Part V | Strong |
| Audit & supervision | Parts III, V | Partial — still expanding |
| Settlement | Emerging in Tauros roadmap | Open frontier |
| Blockchain execution | — | Open frontier |
| Smart-contract authority | — | Open frontier |
| On-chain evidence and analytics | — | Open frontier |
| Portable agent identity/delegation | — | Open frontier |
| Multi-agent economic coordination | — | Open frontier |
| Full economic-agent composition | Part VI design work | Conceptual today |

## Cross-cutting CognoKratos method

Every curriculum track should eventually answer the same trust questions:

1. **Actors** — who participates?
2. **Assets** — what are we protecting?
3. **Capabilities** — what can each actor cause?
4. **Authority** — who is allowed to decide?
5. **Trust boundaries** — which component is trusted for what?
6. **Failure modes** — what happens on crash, retry, replay, concurrency, or partial execution?
7. **Attacker actions** — how could a malicious user, model input, tool result, service, or operator abuse the system?
8. **Revocation** — how is authority removed or constrained over time?
9. **Evidence** — what remains afterwards to reconstruct what happened?
10. **Limitations** — what is not solved by this architecture?

This common frame should make projects comparable without forcing them onto one technology stack.

## Research frontier

The following directions are candidates for future tracks. Their exact scope and order are intentionally open to community input.

### Secure signing and delegated cryptographic authority

**Open question:** How can an agent sign or authorize transactions without receiving unrestricted private-key control?

Potential topics:

- HSMs and hardware-backed keys;
- transaction simulation;
- scoped signing policies;
- spend limits;
- revocation;
- multi-party or threshold authorization;
- MPC;
- human co-signing;
- signed capability tokens.

This may become an Arktos extension or a separate track.

### Settlement and reconciliation

**Open question:** How does an approved economic intent become a safely executed and reconciled transfer of value?

Potential topics:

- stablecoins and payment rails;
- transaction construction;
- submission vs confirmation vs finality;
- retries and replacement;
- reconciliation;
- network fees;
- duplicate settlement prevention;
- partial failure.

Tauros already points toward this through settlement events and reconciliation.

### Αρχνος Analytics — On-chain evidence and analytics

Potential curriculum role:

- blockchain data pipelines;
- provenance;
- on-chain evidence;
- financial observation;
- reconciliation against decentralized state;
- analytics over Bitcoin and EVM systems.

### Λύκος Vault — Smart-contract authority

Potential curriculum role:

- programmable authorization;
- escrow;
- verifiable agreements;
- smart-contract trust boundaries;
- adversarial contract interaction;
- constraints enforced by decentralized execution.

### Νέος Node — Sovereign blockchain infrastructure

Potential curriculum role:

- node trust;
- RPC security boundaries;
- controlled deployment;
- self-hosting and sovereignty;
- chain configuration;
- contract deployment infrastructure;
- operational ownership.

### Έργος Platform — Composition

Potential curriculum role:

- combine agent reasoning, financial intent, cryptographic authority, and on-chain execution;
- generate or orchestrate infrastructure from explicit requirements;
- study where automation itself requires new authority boundaries.

### Portable agent identity and delegated authority

**Open question:** How does an autonomous agent prove who it is and what authority was delegated to it across organizational boundaries?

Potential topics:

- workload identities;
- verifiable credentials;
- decentralized identifiers;
- attestations;
- capability delegation;
- expiry and revocation;
- agent-to-agent verification.

### Multi-agent economic coordination

**Open question:** What happens when autonomous agents transact with other autonomous agents rather than only with human-operated systems?

Potential topics:

- protocol discovery;
- negotiation;
- escrow;
- reputation;
- adversarial counterparties;
- payment and settlement;
- machine-to-machine markets;
- decentralized coordination.

## Project maturity model

A new idea does not immediately become a curriculum track.

A suggested path is:

**Research question → discussion/RFC → experiment → reference implementation → learning track → curriculum integration**

An official curriculum track should aim to provide:

- a concrete engineering question;
- runnable code;
- explicit actors, assets, capabilities, and trust boundaries;
- reproducible verification or tests;
- documented failure modes and limitations;
- learning material;
- exercises, labs, or adversarial experiments;
- a clear relationship to existing graduate competencies;
- enough independence that learners can inspect the problem rather than merely use an opaque framework.

## The book and repositories

Learning material should live as close as possible to the code it describes. The book can then assemble pinned, reviewed versions of that material and add orientation and cross-project synthesis.

This creates a knowledge pipeline:

**repository implementation → learning material beside the code → review and contribution → pinned curriculum edition → book synthesis**

The book should describe the current state of knowledge rather than freeze the first architecture forever.

## Versioning the curriculum

The curriculum should evolve without pretending that earlier designs never existed.

When an architecture materially changes, CognoKratos should preserve:

- what the previous design assumed;
- what failure or new requirement motivated the change;
- what changed in the trust model;
- whether the new architecture supersedes or merely complements the old one.

That history is educational.

## Community ownership

The long-term objective is not merely to accept pull requests. It is to let practitioners contribute engineering experience back into the curriculum.

High-value contributions include:

- demonstrating a broken assumption;
- adding an adversarial case;
- correcting an architectural claim;
- improving a threat model;
- contributing a new lab;
- comparing an alternative design;
- proposing a missing competency;
- building a new reference implementation;
- developing an entirely new curriculum track.

The current five projects are **Version 1**, not the finish line.
