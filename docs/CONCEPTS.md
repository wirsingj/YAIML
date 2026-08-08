---
yaiml: 0.2
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

YAIML is a lightweight plain-file convention and reusable template docset for AI Project Engineering practice. It should grow more like Markdown, Keep a Changelog, Conventional Commits, or EditorConfig than like a runtime framework: easy to adopt, easy to inspect, and useful without installing a dependency. It may become broadly adopted later, but this repository should not imply that broad adoption or consensus already exists.

It exists because repository-aware AI chats and coding agents have made natural-language engineering direction a first-class part of software development. A person or team may spend months steering agents through product intent, bugs, design corrections, audits, playtest feedback, security findings, implementation risks, and priorities. The raw conversation is temporary working memory. A repo using YAIML preserves the useful engineering state that should survive.

YAIML is a guiding document set for project management, project memory, project definition, and AI-session continuity. It gives durable homes to the parts of a repository that are too important to leave in vanished chat but too interpretive to live only in source code.

YAIML is an idea and documentation framework, not professional advice. It can help preserve a project's own legal, security, compliance, privacy, licensing, or IP constraints, but it does not create those constraints or recommend professional action.

## AI Project Engineering

In AI Project Engineering, the developer works at two layers:

- technical artifacts: code, tests, configuration, scripts, docs, assets;
- engineering direction: goals, constraints, corrections, risk calls, acceptance judgments, and lessons learned through human, chat, and agent collaboration.

A repo using YAIML stores the distilled second layer in the repository so a later chat, agent, or contributor can continue the same project instead of re-discovering or distorting it.

## Repository Memory, Not Chat Memory

Chat history is useful during a session, but it is a poor long-term source of project truth:

- it is provider-specific;
- it may be inaccessible to another agent, chat, or contributor;
- it is too large to reread continuously;
- it mixes obsolete experiments with current direction;
- it often records raw discussion rather than synthesized engineering state.

YAIML documents are smaller, local, editable, versioned with the repo, and designed to be read by the next AI chat, agent, or contributor.

They should be ordinary Markdown documents by default. A custom `.yaiml` extension would make the idea feel more branded, but less usable: editors, previews, search tools, diffs, and agents already understand `.md`. YAIML's strength is the shape of the memory, not a new file format.

`yaiml.yml` exists only as a tiny discovery file so humans, chats, agents, and possible future tools can find the memory family. If YAIML ever validates anything, validation should stay around that small discovery file, not the human-authored Markdown memory.

They should usually be committed with the source code. YAIML is shared project memory, not private scratch space by default. A project may choose a private-memory policy, but initialization should not hide YAIML files in `.gitignore` without explicit human direction.

YAIML's portability is independent of the project's business or licensing model. A project may be private, public, paid, free, open-source, or unreleased; the YAIML family should still travel with the repository across machines, contributors, and AI chat provider instances.

Because YAIML travels with the repository, it must be safe for the repository's intended audience. It must not become a dumping ground for secrets, private chat transcripts, raw logs, private screenshots, or fragile legal claims. Do not store raw tokens, passwords, private keys, credentials, customer personal data, or other sensitive values in YAIML. For security and privacy topics, preserve sanitized risk shape, evidence location, owner, decision, and next step.

In company, client, or regulated repositories, "safe for the repository's intended audience" means permitted by the governing retention, privacy, access-control, owner, and review rules. YAIML documents can record those constraints; they do not override them.

Legal, licensing, copyright, trademark, ownership, patent, contract, and IP statements need extra caution. Agents should preserve human-approved statements and uncertainty, not invent legal conclusions or rights claims.

The same caution applies to security, compliance, privacy, and incident-response notes. YAIML documents can record reviewed decisions, risk shape, evidence, owners, and questions. They should not manufacture advice or imply that agent-written text is a professional assessment.

## Relationship To Agent Instructions

Agent instruction files such as `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and similar files primarily tell an agent how to behave while working in a repository.

YAIML primarily preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.

An instruction file can direct an agent to discover and read YAIML. YAIML should not duplicate every behavioral rule from the instruction file.

## Positioning

YAIML does not claim to have invented persistent Markdown context for AI chats or coding agents.

Its differentiator is the combination of:

- current interpreted whole-project understanding;
- separation of human direction from implementation evidence;
- explicit uncertainty and disagreement;
- synthesis instead of chronological logging;
- pruning and obsolescence;
- distinct ownership across SoT, Architecture, Maintainer Guide, and supporting domains;
- continuity across disposable chats, agents, contributors, and providers.

Feature specifications define desired behavior for a bounded change. Changelogs describe what changed. Backlogs describe work that may happen. Architecture documents describe system shape. YAIML connects these concerns by preserving the project's current interpreted engineering state and directing agents toward the authoritative artifacts behind it.

## Standard Shape, Local Fit

YAIML should be recognizable without requiring identical documents everywhere.

Durable expectations:

- SoT is the central current-state artifact.
- Architecture preserves durable system understanding.
- Maintainer Guide preserves operational knowledge.
- The core document family can self-unfold into supporting documents when the project needs durable homes for preferences, definitions, rules, risks, doctrine, legal constraints, domain concepts, or operating knowledge.
- Every YAIML document starts with a stable header.
- Human intent and implementation evidence stay distinct.
- Uncertainty and conflicts stay visible.
- Stale SoT detail is pruned.

Project-sensitive choices:

- filenames may vary;
- headings may vary;
- documents should usually stay as `.md` files;
- projects may add or omit supporting documents;
- supporting document types are not closed; projects can invent the ones they need;
- local vocabulary may vary;
- the body is free-form Markdown;
- no parser-driven compliance is required for the Markdown memory.

A document is healthy because it performs its engineering role, not because it matches a schema exactly.

Self-unfolding does not mean creating every possible document. It means splitting out a document when a topic repeatedly shapes work, carries risk, defines vocabulary, preserves preferences, or needs a different pruning rule than the core three.

## Human-Governed, Agent-Maintained

Agents are expected to create, update, audit, and prune YAIML documents. Humans remain authoritative about intended meaning and product direction when they are the right authority for that project. In shared or governed projects, approved decisions, current maintainers, owners, and documented repository rules outweigh stale notes, stray comments, and agent inference. The repository remains authoritative about current implementation reality.

YAIML is allowed to be multi-agent and multi-contributor. That makes the evidence rules more important, not less important: when two chats, agents, or humans disagree, preserve the conflict, source, and uncertainty instead of smoothing it into a false single story.

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
Will this help the next AI chat, coding agent, or contributor make better decisions?
```

If not, Git history is the archive.
