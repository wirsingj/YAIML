# Init YAIML

You are a coding agent adding the smallest useful YAIML project-memory loop to a new or existing software repository.

This prompt must stand on its own. Do not assume the human has explained YAIML elsewhere.

Do not change application code during this init unless the human explicitly asks.

Before editing, inspect the current worktree state. Treat existing uncommitted changes as intentional work in progress. Do not reset, discard, rename, delete, or overwrite existing work to make room for YAIML.

## Goal

Create a plain Markdown project-memory loop that preserves the repository's current interpreted engineering understanding across future disposable coding-agent sessions.

YAIML is not a package, runtime, schema, parser target, hosted memory service, database, SDK, or required CLI. It is ordinary version-controlled project memory.

## Create Or Update

Use predictable filenames by default when they do not conflict with useful existing files:

```text
SOT.md
ARCHITECTURE.md
MAINTAINER_GUIDE.md
yaiml.yml
```

If the repository already has YAIML documents, preserve useful paths and update stale declarations instead of replacing them blindly.

If `ARCHITECTURE.md`, `MAINTAINER_GUIDE.md`, or similar documentation already exists and contains useful project knowledge, do not overwrite it. Either add a concise YAIML stable header and lightly organize the existing content without changing its meaning, or choose a non-conflicting path and point `yaiml.yml` to it. Preserve existing human wording where it matters.

## Minimal Procedure

1. Read existing agent instructions such as `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, contribution docs, or local workspace notes. Record the exact paths found, or say none were found.
2. Check the current git status or equivalent worktree state before editing.
3. Inspect the repository enough to understand current project purpose, structure, commands, tests, risks, existing documentation, and uncertainty.
4. Create or update `yaiml.yml` as a small discovery file pointing to the three core documents.
5. Create or update `SOT.md`, `ARCHITECTURE.md`, and `MAINTAINER_GUIDE.md`, unless those names would overwrite useful existing non-YAIML documents.
6. Put a concise stable header at the top of each YAIML document.
7. Populate only verified facts, declared human intent, clearly marked inference, known uncertainty, and visible divergence.
8. When recording commands, list only commands found in project files or actually run. If you run checks, record the exact command and result inside the YAIML documents, not only in the final chat response.
9. Do not create supporting documents unless a domain already has several concrete recurring pieces of project knowledge that would bloat the core three.
10. Keep the first pass concise. Leave clear next steps, but do not turn init into a giant audit.
11. Do not add YAIML files to `.gitignore` by default.
12. Do not store secrets, credentials, tokens, private keys, passwords, customer personal data, or sensitive raw values in YAIML.
13. Do not invent legal, IP, licensing, security, privacy, or compliance conclusions.

## Stable Header Shape

Use this shape or equivalent plain prose:

```md
---
yaiml: 0.1
role: sot
title: SOT
purpose: Current engineering state and direction for the project.
belongs-here: goals, current capabilities, declared direction, active risks, priorities, divergence, uncertainty, useful recent lessons.
not-here: durable architecture, command reference, complete history.
durability: volatile; synthesize and prune aggressively.
read-with: Architecture; Maintainer Guide.
update-when: direction, verified reality, risks, priorities, or useful engineering lessons change.
agent-guidance: Verify implementation claims. Preserve human intent. Mark uncertainty. Surface conflicts. Prune stale detail.
---
```

Adapt `role`, `title`, `purpose`, and guidance for Architecture and Maintainer Guide.

## Suggested `yaiml.yml`

```yaml
yaiml: "0.1"

project:
  id: my-project
  name: My Project

documents:
  sot:
    path: SOT.md
    title: SOT
  architecture:
    path: ARCHITECTURE.md
    title: Architecture
  maintainer:
    path: MAINTAINER_GUIDE.md
    title: Maintainer Guide
```

## Core Document Jobs

`SOT.md` preserves current engineering state: project identity, verified capabilities, declared human direction, active risks, testing state, known divergence, useful lessons, immediate priorities, and open questions.

`ARCHITECTURE.md` preserves durable system shape: components, boundaries, data flow, invariants, current architecture, intended architecture, known violations, danger zones, and retired approaches.

`MAINTAINER_GUIDE.md` preserves operating knowledge: setup, verified commands, environment-dependent commands, focused checks, important files, danger files, diagnostics, failure playbooks, and unverified procedures.

## Output

Report:

- files created or changed;
- pre-existing files preserved;
- exact agent-instruction paths found, or none found;
- evidence inspected;
- verified facts recorded;
- declared intent recorded;
- inference, uncertainty, or divergence recorded;
- commands run and whether they passed;
- recommended next steps.
