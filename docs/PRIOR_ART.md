---
yaiml: 0.2
kind: comparison-guide
title: Prior Art
purpose: Locate YAIML among existing agent-instruction, project-memory, and documentation conventions, and state what it does not claim to originate.
belongs-here: comparable conventions, what each already solves, YAIML's actual difference, when to use another convention instead.
not-here: adoption steps, feature roadmaps, marketing claims, competitor criticism.
durability: durable; update when a compared convention changes materially or a new comparable convention gains real adoption.
read-with: Concepts; Core Document Family; Ambiguity And Evidence.
update-when: a listed convention changes its model, or YAIML's distinguishing claim changes.
agent-guidance: Describe other projects accurately and without disparagement. Do not claim adoption, benchmarks, or superiority that evidence does not support.
---

# Prior Art

YAIML did not invent keeping project context in Markdown. Several conventions already do, some with far more adoption. This document states what they solve, what YAIML adds, and when to use one of them instead.

Descriptions reflect the maintainer's reading at the time of writing and may lag those projects. Correct them rather than preserving a stale summary.

## Agent Instruction Files

`AGENTS.md`, `CLAUDE.md`, `.github/copilot-instructions.md`, Cursor rule files, and Kiro steering files tell an agent how to behave in a repository: commands, style, boundaries, review rules.

These are the incumbent, and YAIML depends on one of them. The init prompt writes its pointer into whichever file the active agent actually loads; without that step YAIML never enters context. They are instructions, not state — none carries a record of what the project currently *is*, what was decided, or what remains unverified.

**Use them alone when** the repository is small enough that an agent can rebuild current understanding by reading the code.

## Structured Memory Sets

Cline and Roo **Memory Bank** is the closest existing convention: a fixed Markdown set (`projectbrief`, `productContext`, `activeContext`, `systemPatterns`, `techContext`, `progress`) plus an "update memory bank" trigger phrase.

The overlap is substantial and should be acknowledged plainly. `activeContext` + `progress` cover roughly what YAIML's SoT covers; `systemPatterns` + `techContext` cover roughly what Architecture covers. The trigger-phrase mechanism is the same idea as YAIML's "update project memory."

YAIML differs in three ways: roles are defined by exclusion as well as content, so every document declares what it does *not* own; retention is explicit, so documents declare durability and a working size budget rather than growing indefinitely; and claims carry provenance. Memory Bank records that something works. YAIML asks whether that was verified, declared, observed, or inferred — and under what conditions.

**Use Memory Bank instead when** your team already runs Cline or Roo and wants a convention the tool understands natively.

## Decision Records

**ADR** (Nygard) and **MADR** keep one immutable file per architectural decision, with a status field and the context that produced it.

ADRs are a history of decisions. YAIML's SoT is a synthesis of current state, and it explicitly discards what no longer matters. These are complementary, not competing: a project with ADRs already has the decision trail YAIML tells you not to reconstruct, and YAIML should link to them rather than restate them.

**Use ADRs instead when** the durable question is *why was this chosen* rather than *what is true now*.

## Architecture And Documentation Frameworks

**arc42** supplies a twelve-section architecture template. **C4** supplies a diagram hierarchy. **Diátaxis** classifies documentation by reader need (tutorial, how-to, reference, explanation).

All three are aimed at human readers and are considerably more thorough than YAIML's single Architecture document. None addresses staleness, agent loading order, or evidence status.

**Use them instead when** the audience is human and the goal is comprehensive documentation rather than context an agent reloads every session.

## Specification-Driven Development

**GitHub Spec Kit** and similar spec-first workflows drive work forward: specification, then plan, then tasks, then implementation.

They describe intended future change. YAIML describes present reality, including where implementation has diverged from intent. A project can run both; the spec says where it is going, memory says where it actually is.

**Use a spec workflow instead when** the problem is coordinating what to build next, not recovering what already exists.

## What YAIML Claims

One thing, stated narrowly: **project memory should distinguish what was verified from what was declared, observed, or inferred, and should record the scope under which that was established.**

The role separation, the Markdown format, the discovery file, and the trigger phrases are all conventional. The evidence vocabulary in [Ambiguity And Evidence](AMBIGUITY_AND_EVIDENCE.md) is the part with no direct equivalent in the conventions above, and it is the reason to prefer YAIML over a simpler alternative.

If that distinction does not matter for a given project, one of the conventions above is likely a better fit, and adopting YAIML will cost more than it returns.

## What YAIML Does Not Claim

No adoption beyond the maintainer's own repositories. No measured productivity effect. No benchmark against any convention named here. No compatibility guarantee with any tool that reads these files.

See [Evaluation](EVALUATION.md) for the evidence that would be needed to say more, and [SoTY](SoTY.md) for current status.
