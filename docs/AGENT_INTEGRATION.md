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

Agent instructions carry behavior; YAIML holds the project knowledge they point to. Instructions can also contain state, but keeping detailed memory in its owning documents avoids duplicating it across tools.

## Initialization

Identify the active agent's supported persistent repository-instruction mechanism from available configuration or current official documentation. Names such as AGENTS.md, CLAUDE.md, and GEMINI.md are examples, not evidence of automatic loading. Create only the minimal supported surface needed, and preserve relevant existing and nested instructions.

Check syntax, activation scope, and discovery paths, including from subdirectories. Report the exact pointer location, whether it is tracked or covered by an explicit private-instruction policy, and the basis for expecting it to load. A newly created file awaiting an authorized commit should be reported as such.

Distinguish configured instructions from observed fresh-session loading. If persistence is unsupported or requires a user-controlled setting, disclose the unfinished step; repeated reminders do not complete integration. Ordinary work should then read and maintain affected memory without mentioning YAIML.

## Suggested Pointer

[Init YAIML's Connect Future Sessions section](../prompts/init-yaiml.md#connect-future-sessions) owns the complete copyable pointer. Adapt it to local paths and policies instead of maintaining a second generic version here. Repeated setup updates the existing pointer rather than appending another.

The pointer carries routine reading, synthesis, retention, and privacy rules. The local Maintainer Guide supplies project-specific maintenance details. [Context Loading](CONTEXT_LOADING.md) owns reading behavior; [Adoption And Updates](ADOPTION_AND_UPGRADES.md) owns convention refresh and discovery compatibility.

## Keeping Responsibilities Clear

Tool permissions, response style, branch rules, and collaboration behavior belong in agent instructions. Project procedures and the rationale for lasting preferences can live in linked memory. Neither the discovery map nor memory grants new permissions.
