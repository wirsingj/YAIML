# YAIML

YAIML is an incubating plain-file convention for preserving a software project's current interpreted engineering understanding across disposable coding-agent sessions.

The chat can disappear. The provider can change. The agent can change. The project context remains in the repository.

> Coding agents are temporary. The project's engineering understanding should not be.

## What Problem It Solves

Modern agent-assisted software work includes code, tests, configuration, and a second layer of natural-language engineering direction: product intent, design corrections, audit findings, rejected approaches, risk calls, maintainer procedures, and lessons learned through use.

That second layer often lives in temporary chat. YAIML keeps the useful interpreted state close to the source code so the next Codex, Claude, Cursor, Gemini, local model, or other coding agent does not have to reconstruct the project from scratch.

## Who It Is For

YAIML is for developers using recurring coding-agent sessions on projects where source code alone does not preserve enough meaning.

The README is for humans deciding whether to try YAIML. The document family inside a project is primarily for agent continuity, while staying readable and reviewable by humans.

## Minimum Useful Setup

The smallest useful YAIML setup is three Markdown files plus a tiny discovery file:

```text
SOT.md
ARCHITECTURE.md
MAINTAINER_GUIDE.md
yaiml.yml
```

Use this flow when you want to try the idea in a few minutes:

1. Run the small init prompt once: [prompts/init-yaiml.md](prompts/init-yaiml.md).
2. Review the created or updated `SOT.md`, `ARCHITECTURE.md`, `MAINTAINER_GUIDE.md`, and `yaiml.yml`.
3. Add a short pointer from your repository's agent instruction file, if it has one, telling future agents to read `yaiml.yml` and the core YAIML documents before meaningful work.
4. Let future sessions use those files as project memory. After meaningful work, the agent should update and prune the affected YAIML documents as part of the work, not wait for a separate pasted reminder.

If a repository has no agent instruction file yet, YAIML still works: start future sessions by telling the agent to read `yaiml.yml` first. The goal is not to paste a workflow prompt after every step. The goal is for the repository to carry enough current project understanding that the next agent can rehydrate from the files already there.

In day-to-day use, the human instruction should be ordinary language: "read YAIML and continue through the SoT priorities," "check the SoT before changing this," or "update our SoT after this work." YAIML should make those small instructions meaningful because the repository already contains the context.

## Full Initialization

Use [prompts/initialize-yaiml.md](prompts/initialize-yaiml.md) when the repository needs a deeper first pass: richer evidence discipline, self-unfolding supporting documents, safety boundaries, and more complete starter shapes.

The full initializer is intentionally self-contained so it can work in another repository without assuming the agent has this repository open. It should still create ordinary project-local Markdown files, not a package dependency, runtime, build step, hosted service, schema system, or required CLI.

## Core Documents

**SoT** means **State Of The**. It is the current engineering-state document: what the project means now, what is verified, what humans intend, what is risky, what is uncertain, what diverges, and what the next agent must not casually distort.

For unfamiliar repositories, use `SOT.md` by default. Project-specific names such as `SoTC.md`, `SoTT.md`, or this repository's `docs/SoTY.md` are supported when they add useful project character, but a new adopter should not have to invent one before beginning.

**Architecture** preserves durable system shape: components, boundaries, invariants, intended architecture, current architecture, known violations, danger zones, and retired approaches.

**Maintainer Guide** preserves practical operating knowledge: setup, commands, tests, diagnostics, important files, danger files, release or recovery procedures, and failure playbooks.

Supporting documents are added only when recurring specialist knowledge no longer fits naturally in the core three. A useful test: if a new document cannot immediately hold several concrete recurring pieces of project knowledge, it probably should not exist yet.

## Agent Instructions

`AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and similar files primarily tell an agent how to behave while working in a repository.

YAIML primarily preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.

An instruction file may point agents to YAIML, but YAIML should not duplicate every behavioral rule. See [Agent Integration](docs/AGENT_INTEGRATION.md).

## Context Loading

Self-unfolding does not mean reading every document for every task. YAIML uses a bounded loading model:

- Discovery layer: `yaiml.yml` and repository agent instructions.
- Core layer: concise SoT, Architecture, and Maintainer Guide.
- Task-relevant layer: supporting documents selected because the current task touches their domain.
- Deep-reference layer: historical decisions, audits, release notes, or specialized material loaded only when needed.

See [Context Loading](docs/CONTEXT_LOADING.md). The hydrate prompt follows this model: [prompts/hydrate-agent-session.md](prompts/hydrate-agent-session.md).

## Evidence Discipline

YAIML should not silently blend different kinds of truth.

- **Verified**: supported by named files, tests, commands, runtime behavior, or documents.
- **Declared**: stated as intent, policy, direction, or decision by a human or authoritative project document.
- **Observed**: seen in behavior but not fully traced.
- **Inferred**: plausible from available evidence but not verified.
- **Disputed**: sources disagree.
- **Unknown**: not currently established.
- **Obsolete**: previously relevant but no longer current.

Do not label every sentence. Use labels where a claim could steer future work. See [Ambiguity And Evidence](docs/AMBIGUITY_AND_EVIDENCE.md).

## What YAIML Is Not

YAIML is not:

- a YAML format;
- a schema-validation system;
- an RFC or conformance regime;
- a package;
- a runtime framework;
- a hosted memory service;
- a database;
- an agent SDK;
- a required CLI;
- a provider integration layer;
- a replacement for source code, tests, Git history, issues, or agent instruction files.

Future tools may help initialize, discover, audit, prune, or assemble context. They should serve the plain-file convention rather than redefine YAIML as software infrastructure.

## Positioning

YAIML does not claim to have invented persistent Markdown context for coding agents.

Its contribution is the combination of current interpreted whole-project understanding, separation of human direction from implementation evidence, explicit uncertainty and disagreement, synthesis instead of chronological logging, pruning and obsolescence, distinct document ownership, and continuity across disposable agents and providers.

Agent instruction files tell an agent how to work. Feature specs define desired behavior for a bounded change. Changelogs describe what changed. Backlogs describe work that may happen. Architecture docs describe system shape. YAIML connects these concerns by preserving the project's current interpreted engineering state and pointing agents toward the authoritative artifacts behind it.

## Examples And Evaluation

[Canopy Dispatch](examples/canopy-dispatch/) is a robust fictional example. It is useful as an example, not proof.

YAIML needs real-project evidence. Use [Evaluation And Case Studies](docs/EVALUATION.md) to run lightweight cold-start comparisons and record limitations without fabricating adoption claims or universal metrics.

## Prompt Library

These prompts are fallback and maintenance workflows, not required commands to paste after every change. In a healthy YAIML repository, the core documents and agent instructions already guide routine hydration, update, and pruning.

- Initialize YAIML in a repository: [prompts/init-yaiml.md](prompts/init-yaiml.md)
- Do a deeper initialization pass: [prompts/initialize-yaiml.md](prompts/initialize-yaiml.md)
- Rehydrate a session when the agent needs explicit help: [prompts/hydrate-agent-session.md](prompts/hydrate-agent-session.md)
- Repair stale memory after meaningful work: [prompts/update-project-memory.md](prompts/update-project-memory.md)
- Audit memory against reality: [prompts/audit-against-reality.md](prompts/audit-against-reality.md)
- Prune an overgrown SoT: [prompts/prune-sot.md](prompts/prune-sot.md)
- Realign a project around a corrected center: [prompts/major-project-realignment.md](prompts/major-project-realignment.md)

## Maturity And License

YAIML is currently in an incubation and review phase. The repository is public for visibility and feedback, but reuse is intentionally restricted during this phase.

No open-source license is currently granted. See [LICENSE.md](LICENSE.md). The maintainer intends to choose an open license before broad public adoption, but no license or release date has been selected.

The current restriction is temporary project protection, not YAIML's intended permanent adoption model.

## Where To Read More

- [Concepts](docs/CONCEPTS.md)
- [Core Document Family](docs/CORE_DOCUMENT_FAMILY.md)
- [Stable Headers](docs/STABLE_HEADERS.md)
- [Context Loading](docs/CONTEXT_LOADING.md)
- [Agent Integration](docs/AGENT_INTEGRATION.md)
- [Evaluation And Case Studies](docs/EVALUATION.md)
- [Roadmap](ROADMAP.md)
