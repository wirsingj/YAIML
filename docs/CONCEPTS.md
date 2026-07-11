---
yaiml: 0.1
kind: concept-guide
title: Concepts
purpose: Explain YAIML's conceptual frame and vocabulary for AI Project Engineering.
belongs-here: core philosophy, project-memory concepts, strong-bones/soft-definitions framing, human-agent authority model.
not-here: current project priorities, command procedures, complete template inventory.
durability: durable; update when YAIML's conceptual frame changes materially.
read-with: SoTY; Core Document Family; Ambiguity And Evidence.
update-when: YAIML's meaning, audience, or core conceptual vocabulary changes.
agent-guidance: Preserve the lightweight convention-first frame. Do not turn concepts into schema or conformance language.
---

# Concepts

YAIML is an incubating convention and framework of ideas for AI Project Engineering practice. It may become a broadly reusable standard later, but this repository should not imply that broad adoption or consensus already exists.

It exists because repository-aware coding agents have made natural-language engineering direction a first-class part of software development. A developer may spend months steering agents through product intent, bugs, design corrections, audits, playtest feedback, security findings, implementation risks, and priorities. The raw conversation is temporary working memory. YAIML preserves the useful engineering state that should survive.

YAIML is a guiding document set for project management, project memory, project definition, and agent continuity. It gives durable homes to the parts of a project that are too important to leave in vanished chat but too interpretive to live only in source code.

YAIML is an idea and documentation framework, not professional advice. It can help preserve a project's own legal, security, compliance, privacy, licensing, or IP constraints, but it does not create those constraints or recommend professional action.

## AI Project Engineering

In AI Project Engineering, the developer works at two layers:

- technical artifacts: code, tests, configuration, scripts, docs, assets;
- engineering direction: goals, constraints, corrections, risk calls, acceptance judgments, and lessons learned through agent collaboration.

YAIML stores the distilled second layer in the repository so a later agent can continue the same project instead of re-discovering or distorting it.

## Repository Memory, Not Chat Memory

Chat history is useful during a session, but it is a poor long-term source of project truth:

- it is provider-specific;
- it may be inaccessible to another agent;
- it is too large to reread continuously;
- it mixes obsolete experiments with current direction;
- it often records raw discussion rather than synthesized engineering state.

YAIML documents are smaller, local, editable, versioned with the repo, and designed to be read by the next agent.

They should be ordinary Markdown documents by default. A custom `.yaiml` extension would make the idea feel more branded, but less usable: editors, previews, search tools, diffs, and agents already understand `.md`. YAIML's strength is the shape of the memory, not a new file format.

They should usually be committed with the source code. YAIML is project memory, not private scratch space by default. A project may choose a private-memory policy, but initialization should not hide YAIML files in `.gitignore` without explicit human direction.

Because YAIML travels with the repository, it must not become a dumping ground for secrets or fragile legal claims. Do not store raw tokens, passwords, private keys, credentials, customer personal data, or other sensitive values in YAIML. For security and privacy topics, preserve sanitized risk shape, evidence location, owner, decision, and next step.

Legal, licensing, copyright, trademark, ownership, patent, contract, and IP statements need extra caution. Agents should preserve human-approved statements and uncertainty, not invent legal conclusions or rights claims.

The same caution applies to security, compliance, privacy, and incident-response notes. YAIML can record reviewed decisions, risk shape, evidence, owners, and questions. It should not manufacture advice or imply that agent-written text is a professional assessment.

## Relationship To Agent Instructions

Agent instruction files such as `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and similar files primarily tell an agent how to behave while working in a repository.

YAIML primarily preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.

An instruction file can direct an agent to discover and read YAIML. YAIML should not duplicate every behavioral rule from the instruction file.

## Positioning

YAIML does not claim to have invented persistent Markdown context for coding agents.

Its differentiator is the combination of:

- current interpreted whole-project understanding;
- separation of human direction from implementation evidence;
- explicit uncertainty and disagreement;
- synthesis instead of chronological logging;
- pruning and obsolescence;
- distinct ownership across SoT, Architecture, Maintainer Guide, and supporting domains;
- continuity across disposable agents and providers.

Feature specifications define desired behavior for a bounded change. Changelogs describe what changed. Backlogs describe work that may happen. Architecture documents describe system shape. YAIML connects these concerns by preserving the project's current interpreted engineering state and directing agents toward the authoritative artifacts behind it.

## Strong Bones, Soft Definitions

YAIML should be recognizable without requiring identical documents everywhere.

Strong bones:

- SoT is the central current-state artifact.
- Architecture preserves durable system understanding.
- Maintainer Guide preserves operational knowledge.
- The core document family can self-unfold into supporting documents when the project needs durable homes for preferences, definitions, rules, risks, doctrine, legal constraints, domain concepts, or operating knowledge.
- Every YAIML document starts with a stable header.
- Human intent and implementation evidence stay distinct.
- Uncertainty and conflicts stay visible.
- Stale SoT detail is pruned.

Soft definitions:

- filenames may vary;
- headings may vary;
- documents should usually stay as `.md` files;
- projects may add or omit supporting documents;
- supporting document types are not closed; projects can invent the ones they need;
- local vocabulary may vary;
- the body is free-form Markdown;
- no parser-driven compliance is required.

A document is healthy because it performs its engineering role, not because it matches a schema exactly.

Self-unfolding does not mean creating every possible document. It means splitting out a document when a topic repeatedly shapes work, carries risk, defines vocabulary, preserves preferences, or needs a different pruning rule than the core three.

## Human-Governed, Agent-Maintained

Agents are expected to create, update, audit, and prune YAIML documents. Humans remain authoritative about intended meaning and product direction. The repository remains authoritative about current implementation reality.

Example:

```text
Declared: The desktop host is not the DM; it is the table owner and a player.
Verified: Two current UI labels still call the host "DM".
Divergence: Product intent and implementation copy disagree.
```

The correct YAIML behavior is to preserve the divergence, not rewrite intent to match the UI or claim the UI has already been fixed.

## Not A Work Log

YAIML is not a transcript of prior agent work. Completed work belongs only when it changes current engineering understanding.

Ask:

```text
Will this help the next coding agent make better decisions?
```

If not, Git history is the archive.
