---
yaiml-revision: "0.43.65c0797e642cbbde"
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

Host instructions connect sessions to project knowledge. [Bootstrap — Connect Future Sessions](../reference/BOOTSTRAP.md#connect-future-sessions) owns route inspection, supported native entries, argument forwarding, activation checks and the copyable pointer. Reuse that procedure instead of maintaining a competing integration checklist here.

## Keeping Responsibilities Clear

| Owner | Content |
| --- | --- |
| Host/project instructions | Tool permissions, response style, branch/review policy and the shared-guide pointer |
| Shared operating guide | Ordinary context, evidence and maintenance loop |
| Project memory | Current facts, constraints, decisions, procedures and scoped evidence |
| Canonical specialized skills | Additional methods for matching requests |
| Native skill entries | Names/descriptions and routes with unchanged user arguments |

Keep supported root/nested tool entry points, unrelated rules and subproject scope. Multiple tools can share one memory family. A new provider does not require copying project facts or generic rules into another family.

## Suggested Pointer

Use [Bootstrap's pointer](../reference/BOOTSTRAP.md#connect-future-sessions), adapted to actual paths. It explicitly reads/follows the shared guide and preserves the coordination reminder. A bare link is insufficient; repeated init repairs the existing section rather than appending another. Stricter local rules and unique project constraints survive consolidation.

## What Activation Establishes

A pasted init can execute before native skills exist. Supported native registration improves discovery; file-based instructions remain useful when a native menu is unavailable. Native syntax is host-specific.

Distinguish saved resources, connected instructions and observed fresh-session use. Failed persistent writes or required host settings remain explicit gaps. A reminder from the human is assistance, not proof that the saved route worked. [Evaluation](EVALUATION.md#one-prompt-skills-lifecycle) owns realistic startup and ordinary-work checks.
