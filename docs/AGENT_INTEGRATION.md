---
yaiml: 0.2
kind: agent-integration-guide
title: Agent Integration
purpose: Explain how YAIML relates to repository agent instruction files without becoming one.
belongs-here: integration patterns for AGENTS.md, CLAUDE.md, GEMINI.md, .cursorrules, .windsurfrules, and similar instruction files.
not-here: provider adapters, SDKs, exhaustive tool-specific instructions, project-specific agent rules.
durability: durable; update when YAIML's relationship to agent instruction files changes.
read-with: SoTY; Context Loading; Core Document Family.
update-when: integration guidance, context-loading expectations, or instruction-file boundaries change.
agent-guidance: Keep this provider-neutral. Do not imply official adapters or duplicate every behavioral rule inside YAIML.
---

# Agent Integration

Agent instruction files specify how a session should work. YAIML holds project understanding: state, direction, evidence, architecture, procedures, and uncertainty. Keep the detailed memory in its owning document and use short pointers from instructions.

## Initialization

Add or preserve a YAIML pointer in each relevant existing instruction surface. Possible surfaces include `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, or editor rule files. Respect their existing scope and syntax; these names are examples, not a claim that every tool reads them.

Initialization must connect the agent being used, even when its instruction file does not exist yet. Identify its supported persistent repository-instruction mechanism from available configuration or current official documentation. Create the minimal supported file or rule needed for that agent; use `AGENTS.md` when supported. Do not create files for every possible provider or guess that a familiar filename is automatically loaded.

Check the instruction file's syntax, activation scope, and path to discovery, including work in subdirectories. Report which mechanism is configured and whether loading was actually observed in a fresh session. File existence alone is not proof of automatic loading. If persistent instructions are unavailable or require a user-controlled setting, report that setup gap during initialization; repeated user reminders are not the intended workflow.

After setup, ordinary requests should trigger memory reading and maintenance without mentioning YAIML. Before finishing material work, record changed facts, decisions, evidence, and unresolved issues in affected memory. Respect read-only scope and review rules; leave unchanged memory alone. Convention refresh from a newer external reference remains a separate maintenance action, not a required step for every task.

Carry local budget and pruning rules into the persistent instruction pointer: review affected memory before adding, prune safely, and report unresolved overages. Necessary growth is allowed; never trade away evidence or retention to meet a number. See [word budgets](PRUNING_AND_LIFECYCLE.md#word-budgets).

Repeated initialization should update an existing pointer instead of appending another copy. Preserve nested instruction scope and re-read files changed by another contributor before writing.

## Suggested Pointer

Adapt paths through the discovery map:

```md
## YAIML Project Memory

Before meaningful work, read yaiml.yml and its core documents:
SoT for current state, Architecture for system boundaries, and
Maintainer Guide for procedures. Read each selected document’s
stable header before its body. Load supporting material only
when task-relevant, reuse already-loaded context while current,
and verify consequential claims.

Before finishing material work, update affected memory and prune stale state
without waiting for a separate YAIML request. Respect read-only task scope;
report pending updates when writing is unavailable. Leave unchanged memory alone.
Preserve declared direction, evidence scope, uncertainty, and unresolved
contributor disagreements. Do not append a work diary.

“Update YAIML”, “updated YAIML”, or “check new YAIML” means refresh
convention guidance from a human-provided or workspace-local reference.
Preserve project memory and the existing discovery layout.

“Clean up YAIML”, “compress YAIML”, “compact project memory”,
“prune project memory”, or “prune SoT” means remove stale or repetitive
memory while preserving current truth, direction, evidence, and uncertainty.

See the Maintainer Guide for local YAIML maintenance.
```

Routine refreshes preserve local document names and older recognizable maps. See [discovery compatibility](ADOPTION_AND_UPGRADES.md#discovery-layout-compatibility) before migration.

## Keeping Responsibilities Clear

Tool permissions, response style, branch rules, and collaboration behavior belong in agent instructions. YAIML can record the project procedures those instructions refer to, such as a current test command or release checklist.

Project preferences may live in supporting memory when their rationale matters. Link to them instead of duplicating their full text in every provider’s instruction file. An agent still follows applicable instructions and project review authority; memory does not grant new permissions.
