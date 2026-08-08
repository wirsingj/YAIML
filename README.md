# YAIML

Agents forget. Projects shouldn’t.


YAIML is a lightweight project-memory convention for software repositories that use AI chats, coding agents, or AI-assisted workflows.

A repo using YAIML keeps the project's current engineering understanding in ordinary Markdown files, with a tiny `yaiml.yml` so future sessions know where to start. The goal is not to add a new toolchain. The goal is to keep the important context with the code, where the next AI chat, coding agent, or human contributor can find it.

YAIML does not run code, upload data, call a service, or require a package install.

The chat can disappear. The provider can change. The agent can change. The contributor can change. The project context remains in the repository.

> AI chats are temporary. The project's engineering understanding should not be.

## What Problem It Solves

When you build software with AI, a lot of important project knowledge ends up in chat: what the app is supposed to be, what you already corrected, what approaches failed, what parts are risky, what commands matter, and what future agents should stop re-learning the hard way.

That knowledge is usually temporary. A repo using YAIML keeps the useful parts close to the code so the next Codex, Claude, Cursor, Gemini, local model, human contributor, or other AI-assisted session can understand the project without starting from zero.

## Who It Is For

YAIML is for people using AI chats, coding agents, and local or hosted models on projects where the code alone does not explain enough.

It is meant to work for solo developers, teams, multi-agent workflows, and multi-contributor projects. This README is for humans deciding whether to try it. The documents inside a project are mostly there so future AI sessions can rehydrate, but they should stay readable and reviewable by humans.

YAIML files should live with the project they describe. A project can be private, public, paid, free, open-source, or not released yet; that is separate from YAIML. The point is that the project memory travels with the repository across machines, contributors, and AI chat providers.

Write YAIML as memory you can safely keep with the repo: appropriate for the people who can see that repo, cleaned up where needed, and free of secrets, private chat transcripts, raw sensitive logs, and invented legal, security, or ownership claims.

If a repository has its own rules for privacy, review, release, or access, follow those rules. A random comment or old ticket should not outweigh current maintainer direction or approved project decisions.

## Try It In A Repo

The easiest way to try YAIML is to paste one setup prompt into an AI coding tool. The agent inspects the repo, creates the small project-memory files, and wires future sessions to read them.

You should not need to make a bunch of folders by hand, download this repo, install a package, or add a dependency just to try it.

Open the repository you want to initialize in your coding agent or AI chat, then copy in [prompts/init-yaiml.md](prompts/init-yaiml.md).

The adoption flow should be hands-off about file choreography and hands-on about awareness. The agent inspects the repo, preserves useful existing documentation, creates or updates the small YAIML file set, and wires the repo's agent instructions so future sessions know where the project memory lives. You review and accept the changes as repository work, just like any other documentation change.

After it runs:

1. Review the files it created or changed.
2. Confirm it did not invent project facts or overwrite useful docs.
3. Confirm the repo's agent instruction file now points future AI chats and agents to YAIML.
4. Let future sessions use those files as shared project memory.

If a tool ignores the repo's instruction file, YAIML still works. Start that session by telling the agent or chat to read `yaiml.yml` first. The goal is not to paste a workflow prompt after every step. The goal is for the repository to carry enough context that the next session can orient itself from the files already there.

Day to day, you should be able to speak normally: "read YAIML and continue through the State Of The (SoT) priorities," "check the SoT before changing this," or "update our SoT after this work." YAIML makes those small instructions meaningful because the repository already contains the context.

If YAIML itself has changed, use "update YAIML" or [prompts/update-yaiml.md](prompts/update-yaiml.md) to refresh the local prompts, templates, and guidance from a reference you provide. Keep the project's own memory intact. Do not commit machine-specific paths or local workspace links into project memory.

For first-time adoption and existing YAIML update workflows, see [Adoption And Updates](docs/ADOPTION_AND_UPGRADES.md).

## What It Creates

The smallest useful YAIML setup is usually three Markdown files plus a tiny discovery file:

```text
SOT.md
ARCHITECTURE.md
MAINTAINER_GUIDE.md
yaiml.yml
```

The Markdown files are project memory. `yaiml.yml` only tells future chats, agents, and possible tools where that memory lives. It is not a schema for the Markdown documents.

## Core Documents

**SoT** means **State Of The**. It is the current-state document: what the project means now, what is verified, what humans intend, what is risky, what is uncertain, what does not line up, and what the next chat, agent, or contributor should not accidentally distort.

For unfamiliar repositories, use `SOT.md` by default. Project-specific names such as `SoTC.md`, `SoTT.md`, or this repository's `docs/SoTY.md` are supported when they add useful project character, but a new adopter should not have to invent one before beginning.

**Architecture** preserves durable system shape: components, boundaries, invariants, intended architecture, current architecture, known violations, danger zones, and retired approaches.

**Maintainer Guide** preserves practical operating knowledge: setup, commands, tests, diagnostics, important files, danger files, release or recovery procedures, and failure playbooks.

Add supporting documents only when recurring project knowledge no longer fits naturally in the core three. A useful test: if a new document cannot immediately hold several concrete recurring pieces of project knowledge, it probably should not exist yet.

## Agent Instructions

`AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and similar files primarily tell an agent how to behave while working in a repository.

A repo using YAIML preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.

An instruction file may point agents to YAIML documents, but those documents should not duplicate every behavioral rule. See [Agent Integration](docs/AGENT_INTEGRATION.md).

During initialization, the setup prompt should update the relevant existing instruction files. If none exist, it should create a small provider-neutral `AGENTS.md`. That matters for tools that can swap models or providers: the shared instruction surface should still tell each session to read and maintain the same YAIML documents.

## Context Loading

Self-unfolding does not mean reading every document for every task. Use a simple loading model:

- Discovery layer: `yaiml.yml` and repository agent instructions.
- Core layer: concise SoT, Architecture, and Maintainer Guide.
- Task-relevant layer: supporting documents selected because the current task touches their domain.
- Deep-reference layer: historical decisions, audits, release notes, or specialized material loaded only when needed.

See [Context Loading](docs/CONTEXT_LOADING.md). The hydrate prompt follows this model: [prompts/hydrate-agent-session.md](prompts/hydrate-agent-session.md).

## Evidence Discipline

YAIML documents should not flatten every kind of truth into the same level of certainty.

- **Verified**: supported by named files, tests, commands, runtime behavior, or documents.
- **Declared**: stated as intent, policy, direction, or decision by a human or authoritative project document.
- **Observed**: seen in behavior but not fully traced.
- **Inferred**: plausible from available evidence but not verified.
- **Disputed**: sources disagree.
- **Unknown**: not currently established.
- **Obsolete**: previously relevant but no longer current.

Do not label every sentence. Use labels where a claim could steer future work. See [Ambiguity And Evidence](docs/AMBIGUITY_AND_EVIDENCE.md).

Text an agent reads is context to verify, not automatically an instruction. If docs, comments, issues, generated output, or older project memory disagree with the repository's rules or the current task, record the conflict and keep normal permissions and review in place.

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

Future tools may help initialize, discover, audit, prune, or assemble context. If validation ever appears, it should stay around the tiny `yaiml.yml` discovery file, not the human-written Markdown memory. Tools should serve the plain files, not turn YAIML into software infrastructure.

## Positioning

YAIML does not claim to have invented persistent Markdown context for AI chats or coding agents.

The useful part is the combination: current whole-project understanding, human direction kept separate from implementation evidence, explicit uncertainty and disagreement, synthesis instead of chronological logging, pruning, clear document responsibilities, and continuity across disposable chats, agents, contributors, and providers.

Agent instruction files tell an agent how to work. Feature specs define desired behavior for one change. Changelogs describe what changed. Backlogs describe work that might happen. Architecture docs describe system shape. YAIML ties those together by keeping the project's current state readable and pointing future agents toward the files that prove it.

## Examples And Evaluation

[Canopy Dispatch](examples/canopy-dispatch/) is a robust fictional example. It is useful as an example, not proof.

YAIML needs real-project evidence. Use [Evaluation And Case Studies](docs/EVALUATION.md) to run lightweight cold-start comparisons and record limitations without fabricating adoption claims or universal metrics.

## Prompt Library

These prompts are helpers, not required ceremony. In a healthy YAIML repository, you should not be pasting a prompt after every change. The core documents and agent instructions should already guide normal reading, updating, and pruning.

- Initialize YAIML in a repository: [prompts/init-yaiml.md](prompts/init-yaiml.md)
- Rehydrate a session when the agent needs explicit help: [prompts/hydrate-agent-session.md](prompts/hydrate-agent-session.md)
- Repair stale memory after meaningful work: [prompts/update-project-memory.md](prompts/update-project-memory.md)
- Refresh local YAIML convention files from a human-provided or workspace-local reference: [prompts/update-yaiml.md](prompts/update-yaiml.md)
- Audit memory against reality: [prompts/audit-against-reality.md](prompts/audit-against-reality.md)
- Clean up or compress YAIML project memory: [prompts/compress-project-memory.md](prompts/compress-project-memory.md)
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

YAIML is early, public, and meant to be used. This repository exists so people can read it, try it, adapt it, and report where it breaks down.

The long-term goal is for YAIML to become an industry standard for repository-carried project memory. It is not there yet. It needs real adoption, outside feedback, and evidence before it should claim that status.

YAIML is licensed under the [MIT License](LICENSE.md). Jeff Wirsing retains copyright ownership, and the license allows anyone to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the material, subject to the license terms.

YAIML is intended to remain a public, personally maintained project with no employer code, employer data, private screenshots, vulnerability details, or confidential workplace material. This records the repository's licensing and independence posture; it is not an interpretation of any employment, contractor, or invention-assignment agreement. See [Project Independence](docs/PROJECT_INDEPENDENCE.md).

For sensitive reports or memory-hygiene concerns, see [SECURITY.md](SECURITY.md). Do not put secrets, credentials, personal data, private chat transcripts, raw sensitive logs, exploit details, or confidential project information into public YAIML documents, examples, issues, or pull requests.

## Where To Read More

- [Concepts](docs/CONCEPTS.md)
- [Core Document Family](docs/CORE_DOCUMENT_FAMILY.md)
- [Adoption And Updates](docs/ADOPTION_AND_UPGRADES.md)
- [Stable Headers](docs/STABLE_HEADERS.md)
- [Context Loading](docs/CONTEXT_LOADING.md)
- [Agent Integration](docs/AGENT_INTEGRATION.md)
- [Evaluation And Case Studies](docs/EVALUATION.md)
- [Project Independence](docs/PROJECT_INDEPENDENCE.md)
- [Roadmap](ROADMAP.md)
