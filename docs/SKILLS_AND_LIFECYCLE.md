---
yaiml-revision: "0.54.58ecbd56ad7274ae"
role: lifecycle-guide
title: YAIML Skills And Project Lifecycle
purpose: Explain how one-prompt adoption becomes persistent context and reusable project workflows.
not-here: Project facts, copied skill procedures, host-specific command syntax or a runtime specification.
durability: Durable design; revise when responsibility or lifecycle boundaries change.
read-with: Using YAIML; Bootstrap; Agent Integration.
update-when: Adoption, composition, growth or update ownership changes.
agent-guidance: Preserve the one-prompt ordinary path and distinguish design from measured behavior.
---
# YAIML Skills And Project Lifecycle

[Using YAIML](../reference/YAIML_GUIDE.md) owns the ordinary context/work/verification/maintenance loop. Named skills provide explicit or specialized methods, rather than mandatory extra steps for every task. [VERSIONING.md](../reference/VERSIONING.md) owns revision and audit mechanics; ordinary completion reads its routine section, while migration and integration load their own detail.

Memory files preserve what the project understands; skill files describe recurring ways to use and maintain it. Agents interpret those instructions with their existing tools. One init prompt starts setup; named skills are optional.

## From Seed To Working Project

The agent follows the pasted `yaiml-init` using its existing file/repository tools. It resolves a revision under [Bootstrap's source policy](../reference/BOOTSTRAP.md#resolve-and-acquire), saves the reusable resources, grounds the four core roles in the target project, and connects supported instructions. The prompt is text to act on, not a program or model installation.

Acquisition and context loading are different operations. The base includes the standard methods, shared rules, coordination guidance and dormant starters so normal use survives an unavailable upstream repository. Agents need not read every saved file into context. The catalog selects methods; methods read current project facts and relevant sources. Additional reference docs or skills are acquired when a concrete need appears. A source revision, local adaptations and incomplete resources remain visible.

A ready adoption has useful memory, complete local workflow dependencies, preserved notices and supported persistent routes. A directory full of files alone is insufficient. If reference access, writes or host persistence are missing, report the exact gap and continue feasible work; do not disguise partial setup as the one-prompt success case.

## Everyday And Explicit Use

After setup, “fix this issue” or a confirmed project decision triggers relevant context loading and material memory maintenance through host instructions. YAIML does not launch audits, empty-document creation or backlog implementation merely because a session started.

A particular user can request `yaiml-audit` with perspectives or `yaiml-to-do 10` with a count. Where the host supports slash commands these can appear as `/yaiml-audit` and `/yaiml-to-do 10`; other hosts use their supported invocation or ordinary language. Host syntax changes the entry point, not the method. Project-only skills can use the same `yaiml-` prefix with a specific purpose name.

[yaiml-diagram](../reference/skills/yaiml-diagram/SKILL.md) creates or updates an editable draw.io view from relevant project memory: "Diagram our architecture and flag uncertain connections." Diagrams are requested deliverables, not required memory files or a competing source of truth. They retain source references and evidence distinctions; updating a view preserves unrelated human edits. See the [fictional example](../examples/diagrams/README.md).

Skills own the methods. [Using YAIML](../reference/YAIML_GUIDE.md) owns shared authority, evidence, context and retention rules. Prompts are optional entry points. Host entries are thin discovery routes. Stubs must never carry method content; retain only canonical references, argument pass-through and reference-resolution directions. Project procedures, expected outcomes and decisions remain in the owning memory documents so methods can use current facts instead of hardcoded copies.

## Concurrent Memory

[Change Records](../reference/CHANGE_RECORDS.md) supplies one workflow: each material change has one retained record; normal work consolidates with sole ownership, while known overlap or uncertain ownership defers factual snapshots and the shared receipt. Current context includes pending records; navigation is repaired immediately. Existing coordination establishes ownership; YAIML provides no global worker detector or lock. “Prepare these changes for review” uses the existing Git method to check intent, evidence and pending consolidation, without granting commit or publication authority.

## Combined Work

The user's request supplies the scope and desired sequence. “Audit as X and Y, do ten priorities, then test” carries one task through evidence gathering, priority selection, work, verification and memory synthesis. A perspective selects questions, not a separate persona or automatic subagent. Counts bound feasible original priorities, not worker count or a demand to manufacture ten tasks.

Methods pass results forward: findings with uncertainty, selected items with acceptance criteria, changes with verification evidence, then material memory corrections. The agent reuses context and completes the requested sequence without requiring additional skill invocations. A blocked dependency does not prevent independent authorized work. Audit findings do not silently supersede human priorities. This composition uses existing agent reasoning; YAIML supplies no workflow engine.

## Growing Knowledge And Methods

Use the existing owner first. Recurring domain knowledge can justify a supporting document with a distinct responsibility and retention rule. Recurring work can justify a project-specific skill with a clear trigger, inputs, steps and completion conditions. One-off observations and speculative preferences do not need permanent artifacts. `yaiml-grow` maintains this distinction.

A missing useful upstream resource follows [Bootstrap's acquisition rules](../reference/BOOTSTRAP.md#resolve-and-acquire), including comparison and authorization for changed license terms, before its dependencies and notices enter local discovery. New skills use the established canonical skill home, defaulting to `.yaiml/skills/` only when none exists. A new project skill is project-owned and stays local unless separately contributed. Updating methods may fix demonstrated shortcomings; it does not silently change project goals or permissions. Growth includes retiring obsolete methods after checking callers and useful knowledge.

## Updating And Repairing

Ordinary memory maintenance changes current project facts. Convention refresh changes reusable YAIML guidance. Init rerun and `yaiml-refresh` use the same reconciliation: compare incoming source, applied baseline where available and current local adaptations. Keep custom skills, unknown extensions and local authority. Unavailable baselines limit confidence; overlapping intent conflicts use established review authority.

Apply complete compatible resource changes, repair catalog/host links and retain revision exceptions after partial updates. Do not claim the entire installation updated when some methods remain on an older revision. Healthy repeat runs are unchanged. Reorganization of mature memory requires scoped authority; ordinary refresh preserves locations.

Removal is also selective: disconnect a retired method only after updating callers; removing YAIML's method routes need not erase the project's accumulated memory. No update or removal is scheduled by this convention.

## Evidence Boundary

These files prescribe agent behavior. Mechanical package/link checks establish availability, while separate fresh-session trials establish whether a host actually discovers and follows the guidance. Neither establishes productivity gains or universal compatibility. [Evaluation](evaluation/EVALUATION.md) and [Cold Start Review](evaluation/COLD_START_REVIEW.md) own current evidence and gaps.
