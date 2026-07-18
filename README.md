# YAIML

YAIML is a small set of Markdown files and prompts that help a software project remember what it is while AI chats, coding agents, and contributors come and go.

The chat can disappear. The provider can change. The agent can change. The contributor can change. The project context remains in the repository.

> AI chats are temporary. The project's engineering understanding should not be.

## What Problem It Solves

When you build software with AI, a lot of important project knowledge ends up in chat: what the app is supposed to be, what you already corrected, what approaches failed, what parts are risky, what commands matter, and what future agents should stop re-learning the hard way.

That knowledge is usually temporary. YAIML keeps the useful parts close to the code so the next Codex, Claude, Cursor, Gemini, local model, human contributor, or other AI-assisted session can pick up the project without starting from zero.

## Who It Is For

YAIML is for people using AI chats, coding agents, and local or hosted models on projects where the code alone does not explain enough.

It is meant to work for solo developers, teams, multi-agent workflows, and multi-contributor projects. This README is for humans deciding whether to try it. The documents inside a project are mostly there so future AI sessions can rehydrate, but they should stay readable and reviewable by humans.

YAIML files should live with the project they describe. A project can be private, public, paid, free, open-source, or not released yet; that is separate from YAIML. The point is that the project memory travels with the repository across machines, contributors, and AI chat providers.

Write YAIML as memory you can safely keep with the repo: appropriate for the people who can see that repo, cleaned up where needed, and free of secrets, private chat transcripts, raw sensitive logs, and invented legal, security, or ownership claims.

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
3. If your repository already has an agent instruction file, verify that it now points future AI chats and agents to `yaiml.yml` and the core YAIML documents before meaningful work.
4. Let future sessions use those files as shared project memory. After meaningful work, the agent should update and prune the affected YAIML documents as part of the work, not wait for a separate pasted reminder.

If a repository has no agent instruction file yet, YAIML still works: start future sessions by telling the agent or chat to read `yaiml.yml` first. The goal is not to paste a workflow prompt after every step. The goal is for the repository to carry enough current project understanding that the next session can rehydrate from the files already there.

In day-to-day use, the human instruction should be ordinary language: "read YAIML and continue through the SoT priorities," "check the SoT before changing this," or "update our SoT after this work." YAIML should make those small instructions meaningful because the repository already contains the context.

If YAIML itself has changed, use "update YAIML" or [prompts/update-yaiml.md](prompts/update-yaiml.md) to refresh local YAIML prompts, templates, and guidance from a reference the human or workspace provides. Keep the project's own memory intact. Do not commit machine-specific reference paths or local workspace URIs into project memory.

For the full first-time adoption and existing YAIML update workflows, see [Adoption And Updates](docs/ADOPTION_AND_UPGRADES.md).

## Full Initialization

Use [prompts/initialize-yaiml.md](prompts/initialize-yaiml.md) when the repository needs a deeper first pass: more evidence guidance, supporting documents where they are actually useful, safety boundaries, and fuller starter shapes.

The full initializer includes enough context to work in another repository without this repo open beside it. It should still create ordinary Markdown files in that project, not a package dependency, runtime, build step, hosted service, schema system, or required CLI.

## Core Documents

**SoT** means **State Of The**. It is the current engineering-state document: what the project means now, what is verified, what humans intend, what is risky, what is uncertain, what diverges, and what the next chat, agent, or contributor must not casually distort.

For unfamiliar repositories, use `SOT.md` by default. Project-specific names such as `SoTC.md`, `SoTT.md`, or this repository's `docs/SoTY.md` are supported when they add useful project character, but a new adopter should not have to invent one before beginning.

**Architecture** preserves durable system shape: components, boundaries, invariants, intended architecture, current architecture, known violations, danger zones, and retired approaches.

**Maintainer Guide** preserves practical operating knowledge: setup, commands, tests, diagnostics, important files, danger files, release or recovery procedures, and failure playbooks.

Add supporting documents only when recurring project knowledge no longer fits naturally in the core three. A useful test: if a new document cannot immediately hold several concrete recurring pieces of project knowledge, it probably should not exist yet.

## Agent Instructions

`AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and similar files primarily tell an agent how to behave while working in a repository.

YAIML preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.

An instruction file may point agents to YAIML, but YAIML should not duplicate every behavioral rule. See [Agent Integration](docs/AGENT_INTEGRATION.md).

## Context Loading

Self-unfolding does not mean reading every document for every task. YAIML uses a simple loading model:

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
- durable storage;
- an orchestration framework;
- a background service;
- a replacement for source code, tests, Git history, issues, or agent instruction files.

Future tools may help initialize, discover, audit, prune, or assemble context. They should serve the plain-file convention rather than redefine YAIML as software infrastructure.

## Positioning

YAIML does not claim to have invented persistent Markdown context for AI chats or coding agents.

The useful part is the combination: current whole-project understanding, human direction kept separate from implementation evidence, explicit uncertainty and disagreement, synthesis instead of chronological logging, pruning, clear document responsibilities, and continuity across disposable chats, agents, contributors, and providers.

Agent instruction files tell an agent how to work. Feature specs define desired behavior for one change. Changelogs describe what changed. Backlogs describe work that might happen. Architecture docs describe system shape. YAIML ties those together by keeping the project's current state readable and pointing future agents toward the files that prove it.

## Examples And Evaluation

[Canopy Dispatch](examples/canopy-dispatch/) is a robust fictional example. It is useful as an example, not proof.

YAIML needs real-project evidence. Use [Evaluation And Case Studies](docs/EVALUATION.md) to run lightweight cold-start comparisons and record limitations without fabricating adoption claims or universal metrics.

## Prompt Library

These prompts are fallback and maintenance helpers, not required commands to paste after every change. In a healthy YAIML repository, the core documents and agent instructions already guide routine reading, updating, and pruning.

- Initialize YAIML in a repository: [prompts/init-yaiml.md](prompts/init-yaiml.md)
- Do a deeper initialization pass: [prompts/initialize-yaiml.md](prompts/initialize-yaiml.md)
- Rehydrate a session when the agent needs explicit help: [prompts/hydrate-agent-session.md](prompts/hydrate-agent-session.md)
- Repair stale memory after meaningful work: [prompts/update-project-memory.md](prompts/update-project-memory.md)
- Refresh local YAIML convention files from a human-provided or workspace-local reference: [prompts/update-yaiml.md](prompts/update-yaiml.md)
- Audit memory against reality: [prompts/audit-against-reality.md](prompts/audit-against-reality.md)
- Prune an overgrown SoT: [prompts/prune-sot.md](prompts/prune-sot.md)
- Realign a project around a corrected center: [prompts/major-project-realignment.md](prompts/major-project-realignment.md)

Practical prompts:

```text
I want this repository to adopt YAIML. Read the YAIML reference, inspect the repository, create the right YAIML files for this project, preserve existing useful documentation, and do not invent project facts.
```

```text
I have a new version of the YAIML reference at [path]. Review this repository's current YAIML files, compare them with the newer reference, preserve repository-specific truth, migrate relevant structural or terminology changes, update internal references, and summarize the upgrade.
```

```text
Read my request, read the repository's YAIML documents, inspect the relevant implementation, execute the work, update the YAIML documents where project truth changed, verify the result, and report what was done.
```

## Maturity And License

YAIML is currently in an incubation and review phase. The repository is public for visibility and feedback, and its intended audience is broad, but reuse is intentionally restricted during this phase.

No open-source license is currently granted. See [LICENSE.md](LICENSE.md). The maintainer intends to choose an open license before broad public reuse, but no license or release date has been selected.

The current restriction is temporary project protection, not YAIML's intended permanent adoption model.

For sensitive reports or memory-hygiene concerns, see [SECURITY.md](SECURITY.md). Do not put secrets, credentials, personal data, private chat transcripts, raw sensitive logs, exploit details, or confidential project information into public YAIML documents, examples, issues, or pull requests.

## Where To Read More

- [Concepts](docs/CONCEPTS.md)
- [Core Document Family](docs/CORE_DOCUMENT_FAMILY.md)
- [Adoption And Updates](docs/ADOPTION_AND_UPGRADES.md)
- [Stable Headers](docs/STABLE_HEADERS.md)
- [Context Loading](docs/CONTEXT_LOADING.md)
- [Agent Integration](docs/AGENT_INTEGRATION.md)
- [Evaluation And Case Studies](docs/EVALUATION.md)
- [Roadmap](ROADMAP.md)
