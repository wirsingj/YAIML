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

YAIML did not invent keeping project context in Markdown. The approaches below overlap with it and can supply the documentation YAIML points to. Choose by the knowledge and workflow your project needs.

The linked primary descriptions were checked on 2026-09-22. These are scoped comparisons of documented purposes, not tested rankings, exclusive feature claims, or compatibility guarantees.

## Agent Instruction Files

[AGENTS.md](https://agents.md/) provides repository context and instructions for coding agents, including project overviews, commands, and working rules. Other tools have their own instruction mechanisms; check the active tool's support.

Instruction files can contain current state, decisions, and uncertainty too. YAIML's choice is to give evolving project knowledge distinct document roles and a maintenance loop, with a pointer in the agent's instructions. An explicit reading request can also load YAIML; routine use depends on a working persistent instruction route.

**Use existing instructions alone when** they already keep the necessary context concise and current. Additional files need to earn their maintenance cost.

## Structured Memory Sets

[Cline Memory Bank](https://docs.cline.bot/best-practices/memory-bank) documents a Markdown family covering project purpose, active context, architecture, technical context, and progress, connected through persistent rules and update requests. Its documentation also describes use with other AI tools.

The overlap is substantial. YAIML groups knowledge into three core roles, adds supporting roles as needed, and emphasizes evidence scope, explicit uncertainty, selective reading, and replacing stale state. This describes YAIML's emphasis; it does not establish that another memory workflow cannot provide the same discipline.

**Keep an existing memory workflow when** it serves the team well. Avoid parallel memory sets describing the same project.

## Decision Records

[Nygard's architecture decision records](https://cognitect.com/blog/2011/11/15/documenting-architecture-decisions) preserve a decision, its context, status, and consequences, retaining superseded decisions. [MADR](https://adr.github.io/madr/) offers a Markdown template for recording decisions and their rationale.

YAIML summarizes the current consequences of decisions and links to those records. Its pruning guidance respects their separate retention rules.

**Use ADRs instead when** the durable question is *why was this chosen* rather than *what is true now*.

## Architecture And Documentation Frameworks

[arc42](https://arc42.org/overview/) supplies a tailorable architecture template. [C4](https://c4model.com/) organizes architecture diagrams by levels of abstraction. [Diátaxis](https://diataxis.fr/) organizes documentation around tutorials, how-to guides, reference, and explanation.

Existing material using these approaches can remain the detailed source. YAIML can point to it and summarize what a recurring session needs; adopting YAIML does not require replacing it.

**Use these approaches when** the main need is architecture communication or organizing documentation for its readers.

## Specification-Driven Development

[GitHub Spec Kit](https://github.com/github/spec-kit) provides structured workflows for specifying, planning, implementing, and checking work. Its current documentation also covers bug fixing and idea assessment.

Such workflows can record decisions and verification too. YAIML's focus is the maintained project-wide understanding used across tasks; it can link to feature specifications and their outcomes.

**Use a spec workflow instead when** the problem is coordinating what to build next, not recovering what already exists.

## What YAIML Claims

YAIML combines current-state synthesis, distinct responsibilities, evidence and uncertainty, selective loading, and pruning into a portable maintenance convention.

The [evidence vocabulary](AMBIGUITY_AND_EVIDENCE.md) makes the difference between intent, inspected implementation, and uncertainty explicit. This is a design choice, not a claim to have invented evidence-aware documentation.

Whether this combination improves a particular team's work enough to justify its cost remains a question to test.

## What YAIML Does Not Claim

No documented independent adoption or measured productivity effect. No benchmark against any convention named here. No compatibility guarantee with any tool that reads these files.

See [Evaluation](EVALUATION.md) for the evidence that would be needed to say more, and [SoTY](SoTY.md) for current status.
