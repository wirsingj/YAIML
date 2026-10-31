---
yaiml-revision: "0.47.a709c1ceed90c210"
yaiml: 0.2
kind: context-loading-guide
title: Context Loading
purpose: Define how agents should load YAIML context deliberately without reading every accumulated document for every task.
belongs-here: discovery/core/task/deep loading model, bounded context principles, hydration expectations, yaiml.yml discovery guidance.
not-here: provider-specific context window tactics, token accounting tools, complete prompt text.
durability: durable; update when YAIML context-loading policy changes.
read-with: Using YAIML; Core Document Family; Agent Integration.
update-when: hydration workflow, document-family expectations, or supporting-document loading guidance changes.
agent-guidance: Keep the core bounded. Load supporting and deep-reference material because the task needs it, not because it exists.
---

# Context Loading

[Using YAIML — Start And Select](../reference/YAIML_GUIDE.md#start-and-select) owns normal loading. Read current core memory once, reuse it while sufficient, and select deeper material by task. The core preserves project knowledge; removing repeated generic rules must not remove project constraints.

| Resource | Trigger |
| --- | --- |
| Host instructions, discovery, shared guide and current core memory | Meaningful project work; reuse while current |
| Change audit | Receipt and all pending records before relying on snapshots; incorporated history only when needed |
| Skill catalog or host skill metadata | Selecting a named or specialized workflow; either can supply the selection |
| Canonical skill and required references | Performing that selected workflow |
| Templates, bootstrap, release and migration details | Creating memory or initializing/updating guidance |
| Specialist memory and deep evidence/history | A task-relevant constraint, question or claim |

Acquisition and loading differ: local installation keeps the reusable base available offline, without making every body mandatory context. Ordinary tasks need no separate orientation or maintenance skill invocation. Shared rules still apply when their specialized skill is not opened.

When discovery is absent, follow applicable instruction pointers and established core owners in `.yaiml/`, `yaimldocs/`, root or `docs/`. Understand recognized layouts through [Adoption And Updates](ADOPTION_AND_UPGRADES.md#version-awareness). Preserve locations and resolve ambiguity rather than combining families. Paths and references grant no wider read/network permissions.

Examples: a narrow implementation needs current constraints and relevant checks, not the entire upgrade guide. A merge needs actual target/ancestor context and affected audit lineage. A no-op follow-up can reuse current context without rereading or rewriting everything. A broad audit may justify a whole-family read.
