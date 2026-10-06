# CognoKratos

**Build agents. Share the knowledge.**

Runnable reference architectures for engineering increasingly consequential agentic systems: from production agent foundations, through runtime durability and governed decisions, to cryptographic capabilities and financial workflows. The open-source engineering and education initiative of [BelaZayka](https://belazayka.com).

![CognoKratos gold emblem. Build agents. Share the knowledge. An initiative by BelaZayka.](images/header.png)

_Built to be understood. Designed to be extended. Shared to move us forward._

Written for experienced software engineers: working code, reproducible experiments and explicit trade-offs instead of demos. Across the portfolio, the model is treated as a probabilistic component. Where authority matters, it is enforced outside the model.

---

## Start with the book

**[The CognoKratos Book — Engineering Agentic Systems](https://book.cognokratos.com/)** is the structured learning companion to the five projects below. Parts I–V are built from the learning paths, concepts, labs, walkthroughs and challenges that live beside each project's code; Part VI compares the five architectures. Every imported chapter names its repository and pinned revision, so you can read a lesson and then run the exact code it describes.

- **New to the series?** Read [What this book teaches](https://book.cognokratos.com/orientation/what-this-book-teaches.html), then follow the [recommended reading order](https://book.cognokratos.com/orientation/learning-routes.html#the-recommended-full-reading-order), starting with Part I.
- **Have a specific question?** Pick an [independent route](https://book.cognokratos.com/orientation/learning-routes.html#independent-routes) into the part that answers it.
- **Before you adapt anything,** read [Limitations and maturity](https://book.cognokratos.com/appendices/limitations-and-maturity.html).

**[Read the book →](https://book.cognokratos.com/)**

---

## Five engineering problems. Five runnable projects.

Each project is a working system with its own learning path, grounded in the code and explicit about what is implemented and what is planned. Each is also one part of the book.

### Production Agent Engineering · [`simple-agent-template`](https://github.com/cognokratos/simple-agent-template)

**How is a production agent engineered around an untrusted probabilistic component?**

Identity and trust boundaries through Keycloak and a Rust authentication gateway, MCP as a capability boundary, guardrails, opt-in signed human approvals, OpenTelemetry tracing and MLflow evaluation, and how to extend the reference architecture to your own domain. A learning path, concept pages, ten labs, a request walkthrough and challenges, all grounded in a customer-support example that is read-only by default.

`Rust` `Python` `NeMo Agent Toolkit` `MCP` `Keycloak` `PostgreSQL` · **Start:** [Learning path](https://github.com/cognokratos/simple-agent-template/blob/main/docs/LEARNING-PATH.md) · [Book, Part I](https://book.cognokratos.com/part-1/introduction.html)

### Durable Agent Runtime Engineering · [`Σοφός Agent`](https://github.com/cognokratos/sophos-agent)

**Once you have an agent, how do you make it durable software that survives time, state, crashes and restarts?**

A small, local-first agent used to study runtime ownership: conversations vs threads vs runs vs checkpoints, SQLite checkpointing, durability boundaries, streaming vs persistence, kinds of memory, crash and resume semantics, and why checkpointing does not make side effects exactly-once.

`TypeScript` `SvelteKit` `LangGraph.js` `SQLite` `MCP` `Ollama` · **Start:** [Runtime learning path](https://github.com/cognokratos/sophos-agent/blob/main/docs/RUNTIME-LEARNING-PATH.md) · [Book, Part II](https://book.cognokratos.com/part-2/introduction.html)

> A single-agent system; it does not implement multi-agent orchestration. Approvals, guardrails and tracing are on its roadmap.

### Governed Decision Engineering · [`etf-research-agent`](https://github.com/cognokratos/etf-research-agent)

**How do you put deterministic policy, evidence and human authority around probabilistic reasoning?**

The model does not make the authoritative decision. A versioned Rust rules engine evaluates each fund against an investor profile; the model explains and proposes; a human confirms or overrides through a signed approval; every change lands in an append-only history recording the policy versions in force. Policy as data, uncertainty and missing data, evidence contracts, decision authority, policy-versioned audit and system-level evaluation. It builds on the `simple-agent-template` architecture rather than re-teaching it.

`Rust` `Python` `NeMo Agent Toolkit` `MCP` `PostgreSQL` · **Start:** [Applied learning path](https://github.com/cognokratos/etf-research-agent/blob/main/docs/APPLIED-LEARNING-PATH.md) · [Book, Part III](https://book.cognokratos.com/part-3/introduction.html)

> Decision support on a dated data snapshot. No market feed, brokerage or trade execution.

### Cryptographic Capability Engineering · [`Άρκτος Wallet`](https://github.com/cognokratos/arktos-wallet)

**How can probabilistic software request cryptographic capabilities without becoming the custodian of cryptographic authority?**

**Give agents capabilities, never secrets.** A self-hosted MCP service through which agents create HD wallets and derive Bitcoin Taproot and Ethereum addresses (BIP39, BIP32, BIP86, BIP44). Key hierarchies and HKDF separation, encrypted secret storage, secret lifetimes and zeroization boundaries, least-capability tool design, out-of-band identity, operator custody and recovery.

`Rust` `Axum` `SQLCipher` `MCP` · **Start:** [Cryptographic capability learning path](https://github.com/cognokratos/arktos-wallet/blob/main/docs/CRYPTOGRAPHIC-CAPABILITY-LEARNING-PATH.md) · [Book, Part IV](https://book.cognokratos.com/part-4/introduction.html)

> Agents receive public capabilities only. No tool signs or broadcasts transactions, signs messages, or exports keys, seeds or recovery phrases, so agents have no authority to move value. The model never holds secret material, but whoever operates the instance holds the encryption keys: self-hosted by the wallet owner, there is no third-party custodian; operated for someone else, the operator has custody.

### Agentic Financial Workflow Engineering · [`Ταύρος Revenue`](https://github.com/cognokratos/tauros-revenue)

**How can agents do operational financial work while humans keep the authority?**

Declarative domain modelling with Ash: resources, actions and policies that are enforced identically for the LiveView UI, the JSON:API and AI tools over MCP. Humans and agents are distinct actors, and the domain, not the prompt, decides what an agent with a valid API key may do. Capability vs authority, non-human identity, financial intent, state machines, idempotency, exact-payload approval, concurrency and auditability. An agent can propose an invoice; only a human approver can decide it.

`Elixir` `Phoenix` `Ash` `AshAI` `MCP` `PostgreSQL` · **Start:** [Learning path](https://github.com/cognokratos/tauros-revenue/blob/main/docs/LEARNING-PATH.md) · [Book, Part V](https://book.cognokratos.com/part-5/introduction.html)

> Implemented on `main`, with a 16-lesson course and exercises: humans and agents with API keys, customer ownership, payment destinations, immutable invoice revisions, a state machine, idempotency, exact-payload human approval, an application-level audit record and eight reviewed MCP tools through AshAI. Database-enforced audit, payments and reconciliation are on the [roadmap](https://github.com/cognokratos/tauros-revenue/blob/main/docs/ROADMAP.md).

---

## Choose where to start

| If you want to…                                                   | Start with                                                                                                                                               |
| ----------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Follow the whole arc, from a bounded agent to financial authority | [Recommended reading order](https://book.cognokratos.com/orientation/learning-routes.html#the-recommended-full-reading-order) · the book                 |
| Follow one request across every trust boundary                    | [Follow one request](https://github.com/cognokratos/simple-agent-template/blob/main/docs/tutorials/REQUEST-WALKTHROUGH.md) · `simple-agent-template`     |
| Adapt a production agent architecture to your domain              | [Extending the template](https://github.com/cognokratos/simple-agent-template/blob/main/docs/EXTENDING.md) · `simple-agent-template`                     |
| See what survives when the process dies mid-run                   | [Run lifecycle walkthrough](https://github.com/cognokratos/sophos-agent/blob/main/docs/runtime/RUN-LIFECYCLE-WALKTHROUGH.md) · `sophos-agent`            |
| Trace one consequential decision from policy to audit             | [Follow one decision](https://github.com/cognokratos/etf-research-agent/blob/main/docs/applied/DECISION-WALKTHROUGH.md) · `etf-research-agent`           |
| See where a secret exists, for how long, and who sees it          | [Secret lifecycle walkthrough](https://github.com/cognokratos/arktos-wallet/blob/main/docs/capability/SECRET-LIFECYCLE-WALKTHROUGH.md) · `arktos-wallet` |
| Understand why an agent's capability is not authority             | [AI capability is not authority](https://github.com/cognokratos/tauros-revenue/blob/main/docs/AI-AUTHORITY.md) · `tauros-revenue`                        |
| Compare how the five projects answer the same questions           | [Part VI: Connecting the architectures](https://book.cognokratos.com/part-6/introduction.html) · the book                                                |

---

## How the projects fit together

```text
                        Production Agent Engineering
                           simple-agent-template
                  how a production agent is built and bounded
                                     │
              ┌──────────────────────┴──────────────────────┐
              ▼                                             ▼
   Durable Runtime Engineering                 Governed Decision Engineering
          sophos-agent                               etf-research-agent
   how the agent survives time                 how its decisions are governed


   Agentic Financial Workflow Engineering      Cryptographic Capability Engineering
          tauros-revenue        ─ ─ planned ─ ─ ▶         arktos-wallet
   who may intend a payment, and why            who may exercise a key, and how
```

The projects are complementary, not a mandatory curriculum. `simple-agent-template` teaches the general production-agent architecture and is the natural foundation. Sophos goes deep on runtime durability and ownership; ETF Research on governing consequential decisions. Arktos isolates cryptographic capability boundaries, and Tauros explores business and financial domain authority. Sophos, ETF Research and Arktos link back to the lessons they depend on instead of re-teaching them, so you can start wherever your question is.

Different engineering questions justify different tools. Rust is used for several low-level security and protocol boundaries: gateways, MCP servers, deterministic rules and key handling. Python carries the agent framework in the NeMo projects, TypeScript and LangGraph.js keep the Sophos runtime small enough to read end to end, and Elixir with Ash expresses business authority declaratively at the domain layer, enforced the same way for every interface.

---

## From model reasoning to financial authority

An agent can call a tool. Letting increasingly autonomous software take part in a financial workflow is a different engineering problem: authority has to be separated, and each part held by the component that can be trusted with it.

```text
Model reasoning           interprets, explains, proposes          the agent projects
      ↓
Agent capability          bounded tools, never credentials        simple-agent-template · arktos-wallet · tauros-revenue
      ↓
Governed intent           deterministic policy and domain rules   etf-research-agent · tauros-revenue
      ↓
Human authority           signed or exact-payload approval,       simple-agent-template · etf-research-agent · tauros-revenue
                          verified at mutation
      ↓
Cryptographic authority   keys held outside the model             arktos-wallet (no signing yet)
      ↓
Settlement                value moves and is reconciled           research direction
```

The question behind the whole initiative: **how can increasingly autonomous software participate in consequential financial workflows without giving probabilistic models uncontrolled authority?**

> **Tauros knows financial intent. Arktos knows cryptographic authority.**

Today they are deliberately separate. Tauros stores public wallet addresses only and never holds a key; Arktos derives addresses but does not sign or broadcast. An optional Tauros-to-Arktos adapter is on the Tauros roadmap. Signing, payments and onchain settlement remain future work.

---

## Research directions

Ideas beyond the five current projects. All are exploratory and none has been started; they are not part of the book, and scope and order may change.

| Idea             | Direction                                      |
| ---------------- | ---------------------------------------------- |
| Αρχνος Analytics | Blockchain data pipelines and analytics.       |
| Λύκος Vault      | Smart-contract controls for trusted execution. |
| Νέος Node        | Controlled EVM deployment infrastructure.      |
| Έργος Platform   | Bring agents and onchain workflows together.   |

---

## Built in the open. Backed by BelaZayka.

CognoKratos is the open-source engineering and education initiative of BelaZayka GmbH, an independent AI engineering and consulting company based in the Zürich region of Switzerland. It is where we share practical engineering in agentic AI and financial systems, and work out in the open what comes next.

The projects are reference architectures for learning, not products, and the book teaches them as such: they are not audited, certified or production-ready, and none of them executes trades, moves money or signs transactions. Explore the code, open an issue or contribute. Each repository documents its own setup, limitations and licensing. If your team needs help applying these architectures, [BelaZayka](https://belazayka.com) brings the design and implementation experience.

[book.cognokratos.com](https://book.cognokratos.com/) · [cognokratos.com](https://cognokratos.com) · [belazayka.com](https://belazayka.com)

<sub>_Cognitio / Kratos_ — the power of knowledge. Shared. Original code and documentation in each repository are MIT licensed; third-party material keeps its own terms, and logos and brand images are not covered. This profile text is MIT licensed; the header image is a brand asset.</sub>
