# CognoKratos

**Build agents. Share the knowledge.**

Practical agentic AI for engineers. Working code to learn from, foundations to build on, and a path to blockchain as financial infrastructure. An open-source initiative by [BelaZayka](https://www.belazayka.com).

![CognoKratos gold emblem. Build agents. Share the knowledge. An initiative by BelaZayka.](images/header.png)

_Built to be understood. Designed to be extended. Shared to move us forward._

---

## Build with what exists

Go beyond the demo. Inspect the architecture, run the evaluations, and follow the decisions from prompt to tool call.

### [`simple-agent-template`](https://github.com/cognokratos/simple-agent-template) — the foundation

**Your next agent starts here.** A working reference for building tool-using agents. Start with a customer-support example, understand the trust boundaries, then adapt it to your domain.

- Keycloak authentication & Rust gateway
- MCP tools, input & output guardrails
- OpenTelemetry traces & MLflow evaluations

`Rust` `NeMo` `MCP` `PostgreSQL` · [Read the extension guide](https://github.com/cognokratos/simple-agent-template/blob/main/docs/EXTENDING.md)

> Read-only by default. Optional human-approved changes.

### [`etf-research-agent`](https://github.com/cognokratos/etf-research-agent) — the applied example

**Research with a reasoning trail.** See the template applied to ETF research: a deterministic Rust engine scores funds, an agent explains the evidence, and a human approves recorded decisions.

- Versioned scoring rules & investor profiles
- Signed human approvals for state changes
- Append-only decision history

`Rust` `Decision support` `Human oversight` · [Walk through the example](https://github.com/cognokratos/etf-research-agent/blob/main/docs/DEMO.md)

> Uses a dated data snapshot. No live market feed or trade execution.

One foundation, different domains: the ETF research agent builds on the shared template. Each repository documents its setup, limitations and licensing notes.

---

## Learn by building

For engineers who want to understand how an agent works, where it can fail, and what keeps it accountable.

1. **Inspect the boundaries.** Follow authentication, tool access and human approvals. See where authority lives and what the model is allowed to do. → [Read the architecture](https://github.com/cognokratos/simple-agent-template/blob/main/docs/ARCHITECTURE.md)
2. **Measure the behaviour.** Run evaluations, inspect traces and test failure cases. Build confidence from evidence you can reproduce. → [Explore evaluation](https://github.com/cognokratos/simple-agent-template/blob/main/docs/EVALUATION.md)
3. **Make it your own.** Replace the example domain with your data, tools and rules. Keep the foundations, and understand what needs to change. → [Start extending](https://github.com/cognokratos/simple-agent-template/blob/main/docs/EXTENDING.md)

---

## The next layer: agents that act, infrastructure to transact

An agent can call a tool. Giving it financial authority is a different engineering problem.

We are exploring blockchain as the financial infrastructure beneath agentic systems:

| Layer          | Question                | Direction                                           |
| -------------- | ----------------------- | --------------------------------------------------- |
| **Identity**   | Know who is acting.     | Agent accounts and attributable actions.            |
| **Authority**  | Define what is allowed. | Budgets, spending policies and approval thresholds. |
| **Settlement** | Make value traceable.   | Payments and receipts with an auditable history.    |

Human-defined policy. Machine-executed workflows. This is a research direction: the current projects focus on agent foundations and decision support, and onchain payments are future work.

---

## On the horizon

The longer-term CognoKratos ideas, kept in view as the foundations take shape. Some are already started in the open. Scope and order may change; none are released products.

| Project                                                         | Focus                                          | Status  |
| --------------------------------------------------------------- | ---------------------------------------------- | ------- |
| [Σοφός Agent](https://github.com/cognokratos/sophos-agent)      | Agent orchestration for business workflows.    | Started |
| [Αρκτος Wallet](https://github.com/cognokratos/arktos-wallet)   | Secure custody and controlled signing.         | Started |
| [Ταύρος Revenue](https://github.com/cognokratos/tauros-revenue) | Contracts, invoices and payment workflows.     | Started |
| Αρχνος Analytics                                                | Blockchain data pipelines and analytics.       | Planned |
| Λύκος Vault                                                     | Smart-contract controls for trusted execution. | Planned |
| Νέος Node                                                       | Controlled EVM deployment infrastructure.      | Planned |
| Εργος Platform                                                  | Bring agents and onchain workflows together.   | Planned |

---

## Built in the open. Backed by BelaZayka.

CognoKratos is an open-source initiative by BelaZayka GmbH, an independent AI consultancy based in the Zürich region of Switzerland.

This is where we share practical engineering and explore what comes next. Explore the code, open an issue or contribute. If your team needs help applying it, [BelaZayka](https://www.belazayka.com) brings the architecture and implementation experience.

[cognokratos.com](https://www.cognokratos.com) · [belazayka.com](https://www.belazayka.com)

<sub>_Cognitio / Kratos_ — the power of knowledge. Shared. Project code is subject to each repository's licensing terms.</sub>
