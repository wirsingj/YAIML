# Concepts

YAIML is a lightweight standard for AI Project Engineering practice.

It exists because repository-aware coding agents have made natural-language engineering direction a first-class part of software development. A developer may spend months steering agents through product intent, bugs, design corrections, audits, playtest feedback, security findings, implementation risks, and priorities. The raw conversation is temporary working memory. YAIML preserves the useful engineering state that should survive.

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

## Strong Bones, Soft Definitions

YAIML should be recognizable without requiring identical documents everywhere.

Strong bones:

- SoT is the central current-state artifact.
- Architecture preserves durable system understanding.
- Maintainer Guide preserves operational knowledge.
- Every YAIML document starts with a stable header.
- Human intent and implementation evidence stay distinct.
- Uncertainty and conflicts stay visible.
- Stale SoT detail is pruned.

Soft definitions:

- filenames may vary;
- headings may vary;
- projects may add or omit supporting documents;
- local vocabulary may vary;
- the body is free-form Markdown;
- no parser-driven compliance is required.

A document is healthy because it performs its engineering role, not because it matches a schema exactly.

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
