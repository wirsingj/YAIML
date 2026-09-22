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

Inspect existing repository instruction routes, including root and nested AGENTS.md, CLAUDE.md, GEMINI.md, tool rule directories, and project-specific equivalents. Include hidden configuration when relevant; exclude examples, templates, generated files, and vendor copies. Preserve actual filenames and casing; do not create case-only duplicates. Names alone do not establish automatic loading.

Connect each applicable existing route, including tools other than the agent running initialization. Reuse working include chains and shared instruction owners; add or update a section only where needed. Preserve unrelated instructions, metadata, activation conditions, and nested scope. Routes for the same project share memory; preserve separately scoped subproject memory and avoid provider-specific families.

Where supported, keep the complete maintenance guidance in one existing shared instruction location and have other entry points explicitly tell agents to read and follow it. Verify that route; a bare link may not cause loading. Otherwise, keep equivalent concise guidance in each applicable entry point. Avoid circular references and repeated insertion.

Use available configuration or current official documentation to establish each mechanism's behavior. If the active agent has no supported instruction file, create the smallest one needed, using AGENTS.md when supported. Do not create a catalog of unused tool files. Report uncertain or unsupported routes without guessing syntax or broadening their scope.

Check syntax, activation scope, and discovery paths, including from subdirectories. For each route, report connected, already connected, or incomplete, its pointer location, tracking status or explicit private-instruction policy, and the basis for expecting it to load. Identify new files awaiting an authorized commit.

Distinguish configured instructions from observed fresh-session loading. If persistence is unsupported or requires a user-controlled setting, disclose the unfinished step; repeated reminders do not complete integration. Ordinary work should then read and maintain affected memory without mentioning YAIML.

## Suggested Pointer

[Init YAIML's Connect Future Sessions section](../prompts/init-yaiml.md#connect-future-sessions) owns the complete copyable pointer. Adapt it to local paths and policies instead of maintaining a second generic version here. Repeated setup updates the existing pointer rather than appending another.

The pointer carries routine reading, evidence distinctions, verification scope, synthesis, retention, and privacy rules into later sessions. Those sessions may never see the init conversation. The local Maintainer Guide supplies project-specific maintenance details. [Context Loading](CONTEXT_LOADING.md) owns reading behavior; [Adoption And Updates](ADOPTION_AND_UPGRADES.md) owns convention refresh and discovery compatibility.

## Keeping Responsibilities Clear

Tool permissions, response style, branch rules, and collaboration behavior belong in agent instructions. Project procedures and the rationale for lasting preferences can live in linked memory. Neither the discovery map nor memory grants new permissions.
