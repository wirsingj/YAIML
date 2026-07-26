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

YAIML should preserve useful project understanding without turning every task into a whole-repository document reading exercise.

Self-unfolding means the document family can grow when the project needs it. It does not mean every accumulated document belongs in every prompt.

## Loading Layers

### Discovery Layer

Read first:

- `yaiml.yml`, if present;
- repository agent instructions such as `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, or contribution instructions.

Use this layer to find the YAIML family and understand how the repository expects agents to behave.

### Core Layer

Read for meaningful work:

- SoT;
- Architecture;
- Maintainer Guide.

These documents should stay concise enough to be practical recurring context. If they become too large for routine loading, prune them or split recurring specialist knowledge into a supporting document.

### Task-Relevant Layer

Read supporting documents when the current task touches their domain.

Examples:

- Read Security Memory for authentication, authorization, secret handling, public exposure, or trust-boundary work.
- Read Legal Or Compliance Memory for license, compliance, contract, policy, or rights-sensitive work.
- Read Product Doctrine for product tradeoffs, audience assumptions, or rejected product directions.
- Read Terms And Glossary when naming, vocabulary, concepts, or domain distinctions shape the task.
- Read Release or Operations material when deployment, rollout, rollback, incident response, or support behavior is in scope.

Do not load unrelated domains just because they exist.

### Deep-Reference Layer

Load only when needed:

- historical decisions;
- audit notes;
- release records;
- old incident reports;
- migration notes;
- specialized domain material;
- long example transcripts or research notes.

Deep references should not be required by default stable headers unless the project truly needs them for routine work.

## Principles

- Prefer a bounded core.
- Keep SoT synthesized and current, not chronological.
- Split recurring specialist knowledge only when it improves clarity.
- Do not create empty documents preemptively.
- Do not load unrelated supporting domains.
- Prune stale information rather than endlessly accumulating it.
- Make `yaiml.yml` useful for discovery without turning project memory into a schema-controlled format.
- Allow a full hydration pass when the task genuinely requires whole-project review.

## `yaiml.yml`

`yaiml.yml` should help agents discover the document family and current YAIML discovery version. It should not become a database, storage layer, local-reference cache, or schema for the Markdown memory documents.

A small useful shape is:

```yaml
yaiml:
  version: "0.2.0"
  core:
    state: SOT.md
    architecture: ARCHITECTURE.md
    maintainer_guide: MAINTAINER_GUIDE.md
  supporting:
    security: docs/SECURITY_MEMORY.md
```

Supporting entries should describe available context, not require automatic loading.

Future validation, if any, should stay limited to this small discovery shape. The project memory itself remains ordinary Markdown with stable roles, evidence discipline, and human-readable judgment.

## Hydration Behavior

A good hydration pass should:

1. Read discovery files.
2. Read stable headers before bodies.
3. Read the core layer.
4. Inspect the user's task.
5. Select task-relevant supporting documents.
6. Verify claims against repository reality where the task depends on them.
7. State what was loaded, what was skipped, and why.

If the human asks for a full review, audit, migration, release readiness check, or major realignment, a whole-family read may be appropriate. Treat that as an explicit deep pass, not the default for every change.
