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

If no agent instruction file exists, the init prompt creates a small provider-neutral `AGENTS.md`. Do not create extra provider-specific files solely for YAIML unless requested.

If a tool does not read repository instructions, ask the session to read `yaiml.yml` explicitly.

Repeated initialization should update an existing pointer instead of appending another copy. Preserve nested instruction scope and re-read files changed by another contributor before writing.

## Suggested Pointer

Adapt paths through the discovery map:

```md
## YAIML Project Memory

Before meaningful work, read yaiml.yml and its core documents:
SoT for current state, Architecture for system boundaries, and
Maintainer Guide for procedures. Read each selected document’s
stable header before its body. Load supporting material only
when task-relevant, and verify consequential claims.

After material work, update affected memory and prune stale state.
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
