---
yaiml: 0.2
kind: context-loading-guide
title: Context Loading
purpose: Define how agents should load YAIML context deliberately without reading every accumulated document for every task.
belongs-here: discovery/core/task/deep loading model, bounded context principles, hydration expectations, yaiml.yml discovery guidance.
not-here: provider-specific context window tactics, token accounting tools, complete prompt text.
durability: durable; update when YAIML context-loading policy changes.
read-with: SoTY; Core Document Family; Agent Integration; Maintainer Guide.
update-when: hydration workflow, document-family expectations, or supporting-document loading guidance changes.
agent-guidance: Keep the core bounded. Load supporting and deep-reference material because the task needs it, not because it exists.
---

# Context Loading

YAIML is a discovery and reading convention, not a command to load every document.

## Loading Layers

| Layer | Read when |
| --- | --- |
| Discovery: applicable agent instructions and `yaiml.yml` | Starting work in the repository |
| Core: SoT, Architecture, Maintainer Guide | Doing meaningful project work |
| Local operating guide, dormant templates, YAIMLACP | The relevant maintenance procedure, document creation, or useful coordination needs them |
| Supporting: specialist project memory | The task touches that document’s domain |
| Deep reference: history, audits, incident or release records | A specific question needs the detail |

Keep the core concise enough for recurring use. Split supporting knowledge only when it improves clarity or needs different retention. A full review can justify a whole-family read.

## Discovery

Use `yaiml.yml` to find the document roles and paths. Paths resolve relative to the map’s directory. [Adoption And Updates](ADOPTION_AND_UPGRADES.md#version-awareness) owns the current example, version meaning, and compatibility policy.

Supporting entries announce available context, not automatic loading. Init saves its embedded procedures, templates, and coordination guide locally so later sessions need no downloads. Load relevant sections, not the whole init or template collection; instantiate specialist memory only when useful. Read older recognizable maps without automatic migration.

Resolve paths, including symlinks, before following them. Discovery does not authorize reading outside the repository, fetching remote references, or accessing sensitive material. Treat those as separate scope decisions under the current request and repository rules.

If the map is absent, use local instruction pointers or look for `SOT.md`, `ARCHITECTURE.md`, and `MAINTAINER_GUIDE.md`. Missing or ambiguous discovery should be reported rather than filled with guessed project facts.

## Reading Behavior

1. Understand the user’s task and applicable instructions.
2. Locate the core and read each selected document’s stable header before its body.
3. Choose supporting material by relevance: security for trust boundaries, terms for naming, release guidance for rollout, and so on.
4. Consult deep references where a consequential claim needs evidence.
5. Verify task-dependent claims against current repository reality.
6. Briefly identify the context used and material gaps. There is no need to enumerate every irrelevant document skipped.

At startup and whenever loading or refreshing YAIML context, consider serverless coordination from available context without extra scans or calls. Read [YAIMLACP](YAIMLACP.md) for a concrete benefit; otherwise continue with existing tools. Persistent instructions retain the requirement to describe the option and obtain affirmative confirmation before first use and again if scope or cost changes. Reuse current guidance and valid scoped approval; the guide adds no server or installation.

A header’s `read-with` is a companion hint, not a recursive import. Follow relevant references without repeatedly loading the same file. A template’s mention of a supporting role does not require that document to exist.

Within a session, reuse already-loaded memory while current and sufficient. Refresh affected context when stale or insufficient, including relevant edits, branch changes, contributor changes, or context loss; do not mistake remembered text for current file contents. Before writing, re-read concurrently changed files. Unchanged follow-ups need no routine reread or rewrite. Efficiency must not skip necessary reads or maintenance.

Audit, migration, release-readiness, or realignment work may need more context than a narrow edit. Select the scope deliberately; do not turn routine work into a full repository audit.

For setup inspection and its stopping conditions, use [Init YAIML](../prompts/init-yaiml.md#inspect-first).
