# Init YAIML

You are an AI coding assistant adding the smallest useful YAIML project-memory loop to a new or existing software repository.

This prompt must stand on its own. Do not assume the human has explained YAIML elsewhere.

Do not change application code during this init unless the human explicitly asks.

Before editing, inspect the current worktree state. Treat existing uncommitted changes as intentional work in progress. Do not reset, discard, rename, delete, or overwrite existing work to make room for YAIML.

## Goal

Create a plain Markdown project-memory loop that preserves the repository's current interpreted engineering understanding across future disposable AI chats, coding-agent sessions, and contributor handoffs.

YAIML means YAIML. It is a documentation standard and reusable template docset, not a package, runtime, schema, parser target, hosted memory service, database, storage layer, orchestration framework, SDK, autonomous coding agent, or required CLI. It is ordinary version-controlled project memory.

Assume the repository may later be touched by multiple humans, multiple AI chats, and multiple agents. Preserve conflicts, uncertainty, and evidence instead of flattening disagreement into false certainty.

Assume the YAIML family should travel with this repository across machines, contributors, and AI chat provider instances. The project may be private, public, paid, free, open-source, or unreleased; that is separate from YAIML. Write YAIML as repository-safe project memory for the repository's intended audience: sanitized evidence, no secrets, no private chat transcripts, no raw sensitive logs, no private screenshots, and no invented legal, security, privacy, or ownership conclusions.

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
7. Add a short YAIML maintenance note to `MAINTAINER_GUIDE.md`: phrases such as "update YAIML", "updated YAIML", "check new YAIML", or "run a YAIML update" mean compare the local YAIML setup against a human-provided or workspace-local YAIML reference, refresh compatible prompts/templates/guidance, and preserve project-specific memory.
8. Do not record machine-specific YAIML reference paths or local workspace URIs in versioned files. A local YAIML reference path belongs in the human prompt, agent/workspace configuration, environment, or ignored local notes, not committed project memory.
9. If an existing agent instruction file was found, add or preserve a short pointer telling future AI chats and agents to read `yaiml.yml` and the core YAIML documents before meaningful work, update affected YAIML documents after meaningful work, and treat "update YAIML" / "check new YAIML" as a convention-refresh request that needs a human-provided or workspace-local reference rather than a project-memory rewrite. Do not create a provider-specific instruction file solely for YAIML unless the human asks.
10. Populate only verified facts, declared human intent, clearly marked inference, known uncertainty, and visible divergence.
11. When recording commands, list only commands found in project files or actually run. If you run checks, record the exact command and a sanitized outcome inside the YAIML documents, not only in the final chat response. Do not copy raw output that contains secrets, personal data, machine-specific paths, private URLs, or confidential details.
12. Do not create supporting documents unless a domain already has several concrete recurring pieces of project knowledge that would bloat the core three.
13. Keep the first pass concise. Leave clear next steps, but do not turn init into a giant audit.
14. Do not add YAIML files to `.gitignore` by default. YAIML is meant to live with the project; keep the contents safe enough to move with the repository across machines, contributors, and AI chat providers by sanitizing sensitive evidence.
15. Do not store secrets, credentials, tokens, private keys, passwords, customer personal data, private chat transcripts, or sensitive raw values in YAIML.
16. Do not invent legal, IP, licensing, security, privacy, or compliance conclusions.

## Stable Header Shape

Use this shape or equivalent plain prose:

```md
---
yaiml: 0.2
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
yaiml: "0.2"

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

Keep `yaiml.yml` portable. Do not add machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs to versioned YAIML files. If "update YAIML" needs a local reference, the human or workspace should provide it at run time.

## Core Document Jobs

`SOT.md` preserves current engineering state: project identity, verified capabilities, declared human direction, active risks, testing state, known divergence, useful lessons, immediate priorities, and open questions.

`ARCHITECTURE.md` preserves durable system shape: components, boundaries, data flow, invariants, current architecture, intended architecture, known violations, danger zones, and retired approaches.

`MAINTAINER_GUIDE.md` preserves operating knowledge: setup, verified commands, environment-dependent commands, focused checks, important files, danger files, diagnostics, failure playbooks, and unverified procedures.

It should also include a short YAIML maintenance note so future AI chats and agents understand that "update YAIML", "updated YAIML", or "check new YAIML" means to refresh convention scaffolding from a human-provided or workspace-local YAIML reference while preserving project-specific memory. Do not hardcode machine-specific reference paths in the note.

## Output

Report:

- files created or changed;
- pre-existing files preserved;
- exact agent-instruction paths found, or none found;
- agent-instruction paths updated with a YAIML pointer, or why none were updated;
- confirmation that no machine-specific YAIML reference path was committed;
- evidence inspected;
- verified facts recorded;
- declared intent recorded;
- inference, uncertainty, or divergence recorded;
- commands run and whether they passed;
- recommended next steps.
