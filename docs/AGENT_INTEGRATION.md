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

YAIML and agent instruction files have different jobs.

`AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and similar files primarily tell an agent how to behave while working in a repository: coding style, tool rules, review expectations, safety limits, branch policy, and local workflow preferences.

YAIML primarily preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.

An instruction file can point agents toward YAIML. YAIML should not become a duplicate of every instruction file.

In multi-agent or multi-contributor projects, YAIML is shared project memory. It should help the next AI chat or contributor understand the same project state without requiring access to earlier private conversations.

## Initialization Behavior

YAIML initialization should wire project memory into the repository's agent-instruction surface.

If the repository already has instruction files such as `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, `.cursorrules`, `.windsurfrules`, `.cursor/rules/*`, or `.windsurf/rules/*`, add or preserve a short YAIML pointer in each relevant file. This lets tools that switch between providers or modes still converge on the same project memory.

If no agent instruction file exists, create a small provider-neutral `AGENTS.md` by default. Do not create a stack of provider-specific files just for YAIML unless the human asks or the repository already uses those surfaces.

Provider-specific files should stay thin. They can point to `yaiml.yml`, the core YAIML documents, and local behavior rules. They should not duplicate the full SoT, Architecture, Maintainer Guide, or supporting memory.

## Minimal Instruction Snippet

```md
Before meaningful work:

1. Read `yaiml.yml` if present.
2. Read the stable header of each declared YAIML document before its body.
3. Read the core YAIML documents: `SOT.md`, `ARCHITECTURE.md`, and `MAINTAINER_GUIDE.md`, or the paths declared in `yaiml.yml`.
4. Load supporting YAIML documents only when the current task touches their domain.
5. Verify task-relevant claims against repository reality.
6. Never treat inference as verified reality.
7. After meaningful work, update only affected YAIML documents and prune stale current-state information.
```

## Existing Instruction File Example

```md
# Instructions For Agents

Use YAIML as project memory, not as a replacement for these instructions.

Start by reading `yaiml.yml`. Then read the core YAIML documents it declares:

- SoT for current project state, direction, risk, uncertainty, and priorities.
- Architecture for durable system shape and intended boundaries.
- Maintainer Guide for commands, diagnostics, and failure playbooks.

For the current task, inspect only relevant supporting YAIML documents. Do not load unrelated domains just because they exist.

When intent and implementation disagree, surface the divergence. Do not rewrite human intent to match accidental code, and do not describe planned behavior as already implemented.

After material changes, update only the affected YAIML documents. Remove resolved active risks and replace stale verification summaries instead of appending a work diary.

If another agent or contributor left conflicting project-memory updates, preserve the disagreement and evidence until a human or repository fact resolves it.
```

## Boundary

Put behavior rules in agent instructions:

- how to run tools;
- how to format responses;
- how to handle tests;
- how to manage branches;
- what commands require care;
- how the human wants the agent to collaborate.

Put project understanding in YAIML:

- current product or system meaning;
- verified current capabilities;
- declared human direction;
- architecture boundaries;
- commands and diagnostics that are current project memory;
- active risks and known divergence;
- open questions and uncertainty;
- durable lessons that should guide future work.

If both places need a fact, prefer a short instruction-file pointer to the YAIML document rather than duplicating the body.

For shared teams, keep local tool preferences in the instruction file when they affect agent behavior, but keep project meaning in YAIML so different chats, agents, and contributors can converge on the same interpreted state.
