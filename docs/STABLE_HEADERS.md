---
yaiml: 0.2
kind: stable-header-guide
title: Stable Headers
purpose: Explain the stable header convention used to orient AI chats and coding agents before document bodies.
belongs-here: header purpose, required meaning, recommended shape, minimum healthy header, compatibility guidance.
not-here: parser requirements, schema design, exhaustive metadata fields, current project priorities.
durability: durable; update when header responsibilities or compatibility posture changes.
read-with: Core Document Family; Ambiguity And Evidence; Pruning And Lifecycle.
update-when: stable header meaning, recommended shape, or agent guidance expectations change.
agent-guidance: Keep headers short and semantic. Do not convert this guide into a rigid field schema.
---

# Stable Headers

Every YAIML document begins with a small stable header.

The header is an operating guide for future AI chats and coding agents. It is not primarily machine metadata, not a rigid YAML schema, and not a promise that every project uses byte-for-byte identical fields.

The body beneath the header remains free-form Markdown suited to the project.

## Required Meaning

A stable header should answer:

- document identity;
- purpose and responsibility;
- what belongs in the document;
- what does not belong in the document;
- how durable or volatile the contents are;
- related YAIML documents to consult;
- when and why the document should be updated;
- reader instructions for evidence, uncertainty, conflicts, pruning, and human direction.

These are semantic responsibilities. Projects may phrase them differently.

Enterprise projects may also include concise owner, reviewer, or higher-authority-source notes when those help agents route material changes through normal review controls. Keep those notes short; do not turn the stable header into a governance form.

## Recommended Shape

Use a compact YAML-like block for readability:

```md
---
yaiml: 0.2
role: sot
title: SOT
purpose: Current engineering state and direction for the project.
belongs-here: goals, current capabilities, active risks, priorities, divergence, recent lessons.
not-here: durable architecture, command reference, full history.
durability: volatile; synthesize and prune aggressively.
read-with: Architecture; Maintainer Guide.
update-when: direction, verified reality, risks, priorities, or useful engineering lessons change.
agent-guidance: Verify implementation claims. Preserve human intent. Mark uncertainty. Surface conflicts. Prune stale detail.
---
```

This is a recommended header shape, not a serialization protocol.

## Minimum Healthy Header

If a project wants fewer fields, the header should still make these clear:

```text
This is SoT.
It owns current engineering state, risks, priorities, divergence, and recent lessons.
It does not own architecture, commands, or full history.
It changes often and should be pruned aggressively.
Read it with Architecture and Maintainer Guide.
Update it when work changes current understanding.
Verify implementation claims and preserve human intent.
```

Markdown prose is acceptable if it reliably orients the agent.

## Header Discipline

Keep headers short. If the header becomes a policy document, move the policy into the body or a supporting guide.

Do not add ceremony unless it improves agent behavior.

Do not use the header to encode a project-management database, issue tracker, or exhaustive file inventory.

## Compatibility

Future tools may read these headers, but current YAIML does not require a parser. A compatible tool should tolerate equivalent wording, missing optional fields, and project-specific vocabulary as long as the semantic responsibilities are clear.
