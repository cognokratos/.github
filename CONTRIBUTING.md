# Contributing to CognoKratos

CognoKratos is a living, community-built engineering curriculum for trustworthy autonomous agents.

Contributions are not limited to bug fixes. The highest-value contribution may be a broken assumption, a better threat model, a reproducible failure case, a new experiment, or an entirely new curriculum track.

## Ways to contribute

You can contribute by:

- fixing code, tests, documentation, or examples;
- reproducing and documenting a failure mode;
- improving a threat model or trust-boundary analysis;
- adding adversarial tests or labs;
- comparing an alternative architecture;
- correcting a curriculum claim that is broader than the code supports;
- proposing a missing competency;
- proposing a new experiment or research question;
- building a new reference implementation;
- developing a new learning track;
- improving the book's synthesis of the projects.

## Start with evidence

CognoKratos values claims that can be inspected.

Good contributions usually include one or more of:

- a test;
- runnable code;
- a command and reproducible output;
- a trace;
- a failure case;
- a threat model;
- a benchmark where performance is the claim;
- a protocol or specification reference;
- a precise explanation of the trust assumptions being changed.

A strong contribution does not need to agree with the current design.

## Challenge the architecture

Reference architectures are propositions, not doctrine.

If you believe an existing design is wrong or incomplete, explain:

1. the assumption you are challenging;
2. the scenario in which it fails;
3. the consequence of that failure;
4. evidence or a reproducible experiment;
5. the alternative design you propose;
6. how the alternative changes the trust model and trade-offs.

A demonstrated weakness is a valuable educational contribution.

## Contributing to an existing project

Each repository owns the learning material that describes its code.

When changing a project, try to keep these aligned:

- implementation;
- tests and verification;
- architecture documentation;
- learning material;
- limitations;
- threat/trust model.

If an educational review reveals that the documentation makes a stronger claim than the implementation supports, narrow the claim or strengthen the implementation. Do not paper over the mismatch.

## Common trust questions

When proposing or reviewing architecture, use the shared CognoKratos frame:

- **Actors** — who participates?
- **Assets** — what are we protecting?
- **Capabilities** — what can each actor cause?
- **Authority** — who may decide?
- **Trust boundaries** — what is trusted for what?
- **Failure modes** — what happens on crash, retry, replay, concurrency, or partial execution?
- **Attacker actions** — how could the system be abused?
- **Revocation** — how can authority be removed?
- **Evidence** — what can be reconstructed afterwards?
- **Limitations** — what is deliberately not solved?

You do not have to use the same technology as existing projects. The shared methodology matters more than stack uniformity.

## Proposing a new curriculum track

A new track should begin with a question, not with a technology.

Good examples:

- How can an agent sign a transaction without receiving unrestricted key control?
- How does approved financial intent become safely settled value?
- How can an agent prove delegated authority across organizational boundaries?
- How should two autonomous economic agents negotiate with adversarial counterparties?

Weak starting points look like:

- "We should have a project using framework X."
- "We should add blockchain Y because it is popular."
- "We need a demo of feature Z."

Technology should follow the trust problem.

## Track lifecycle

A proposed track can mature through:

**Research question → discussion/RFC → experiment → reference implementation → learning track → curriculum integration**

Not every useful experiment needs to reach the final stage.

### Research question

Define the engineering problem and why the existing curriculum does not answer it.

### Discussion / RFC

Describe actors, assets, trust boundaries, candidate approaches, major trade-offs, and what would constitute useful evidence.

### Experiment

Build the smallest system capable of testing the important assumption.

### Reference implementation

Turn the experiment into inspectable, reproducible code with tests and explicit limitations.

### Learning track

Add a progression that teaches the judgment behind the architecture, including exercises that break or challenge it.

### Curriculum integration

Connect the track to existing competencies and update the book's synthesis once the material is mature enough.

## Expected qualities of an official track

An official CognoKratos curriculum track should aim to include:

- one clear engineering question;
- runnable code;
- a defined threat/trust model;
- explicit authority boundaries;
- verification or tests for important guarantees;
- known failure modes;
- documented limitations;
- labs, exercises, or adversarial experiments;
- learning objectives;
- a clear relationship to the wider curriculum.

It does not need to be production-ready. It does need to be intellectually honest about what it proves.

## What belongs where

### Project repositories

Use the relevant project repository for:

- implementation bugs;
- project-specific documentation;
- tests;
- labs;
- architecture changes;
- project-specific threat models;
- project-specific learning material.

### Curriculum-level discussions

Use the CognoKratos organization-level contribution flow for:

- missing competencies;
- cross-project architectural questions;
- new track proposals;
- changes to the curriculum map;
- changes to the CognoKratos foundation or mission;
- suggestions that span multiple repositories.

### The book

The book synthesizes reviewed project knowledge and cross-project reasoning.

Where possible, corrections to imported learning material should happen upstream beside the code first, then flow into the book when the project's pinned revision is updated.

Long-term, the book itself should be directly contributable so that orientation and synthesis can evolve with the community as well.

## Contribution standards

### Be explicit about implemented vs proposed

Use clear language for:

- implemented behaviour;
- behaviour verified by a test;
- observed model behaviour;
- design targets;
- roadmap items;
- speculative research directions.

Do not collapse them into one claim.

### Prefer mechanisms over slogans

"The agent cannot approve invoices" is useful only if the architecture can show where and how that is enforced.

"The wallet is secure" is too broad. State the custody model, key hierarchy, attacker assumptions, and known limitations.

### Preserve disagreement

When two designs have legitimate trade-offs, document the disagreement rather than erasing it for the sake of one canonical answer.

### Make failure teachable

If a bug or architectural weakness reveals a useful lesson, consider preserving it as a regression test, case study, or exercise after fixing it.

## Community conduct

Technical criticism is welcome. Personal attacks are not.

Assume that contributors are trying to improve the shared body of knowledge. Challenge claims aggressively; treat people respectfully.

The goal is not consensus at any cost. The goal is better engineering understanding.

## A contribution can change the curriculum

CognoKratos is deliberately unfinished.

The current projects are the first version of the curriculum. A contributor who demonstrates that a missing trust problem deserves its own track should be able to change what CognoKratos teaches.

That is the point of building it in the open.

> **Learn. Build. Challenge. Contribute.**
