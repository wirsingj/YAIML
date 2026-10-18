---
yaiml: 0.2
kind: architecture
title: YAIML Architecture
purpose: Preserve YAIML's durable conceptual model, artifact responsibilities, and tooling boundaries.
belongs-here: conceptual architecture, artifact responsibilities, role boundaries, deferred approaches.
not-here: current priorities, command procedures, complete file inventory.
durability: durable; update when roles, artifact responsibilities, or deferred tooling boundaries change.
budget: About 800 words; preserve necessary design constraints if exceeded.
read-with: SoTY; YAIML Maintainer Guide.
agent-guidance: Verify repository shape before claiming artifacts. Surface conflicts. Preserve human direction.
---

# YAIML Architecture

## System Model

YAIML is shared project context plus reusable methods for managing and using it. The minimum interaction is one pasted init prompt. It runs bootstrap through existing host tools, establishes target-owned memory and skills, and connects future sessions. Optional named commands select the same methods used during ordinary work. There is no YAIML application runtime, scheduler or workflow engine.

`.yaiml/` is the default home for discovery, memory, skills and reusable resources. Host instructions and public/legal entry points remain in their supported locations. Discovery paths resolve relative to their map; mature layouts are compatibility inputs, not replacement targets. [Adoption And Updates](ADOPTION_AND_UPGRADES.md) owns compatibility.

## Owners And Boundaries

| Owner | Responsibility |
| --- | --- |
| SoT | Current direction, capabilities, risks, priorities, divergence and uncertainty |
| Architecture | Durable responsibilities, invariants, design and relevant rationale |
| Maintainer Guide | Actual project procedures, verification/recovery and current source/adaptation notes |
| Supporting memory | Recurring specialist knowledge or distinct retention |
| `skills/yaiml-*/SKILL.md` | Reusable methods with triggers, inputs, actions and outcomes |
| `YAIML_GUIDE.md` | Shared context, composition, evidence, authority and retention rules |
| `skills/INDEX.md` | Selection by purpose and local reachability |
| Host instructions / native entries | Activation, scope and argument forwarding into canonical methods |
| Init / Bootstrap | Entry seed, source acquisition, adoption and repair |
| Templates / optional prompts | Dormant writing aids / alternative entry points to owning skills |

Facts have one detailed memory owner; methods read current facts rather than embedding copies. Host entries are thin routes, not competing implementations. This repository uses `.agents/skills/` entries pointing to `.yaiml/skills/`; other hosts need their supported mechanisms. [Core Document Family](CORE_DOCUMENT_FAMILY.md) owns role guidance.

## Lifecycle

The seed knows the public reference location and bootstrap path; it assumes no YAIML context or preinstalled skill. Bootstrap resolves a revision, acquires a complete local base and creates useful memory from target evidence. Source-project facts and policies do not transfer. Acquiring a resource does not require loading its whole body into reasoning context or executing it.

The base supplies standard skills, shared rules, optional coordination guidance, dormant starters and applicable notice. These provide ordinary offline use. Specific missing extensions can be retrieved later from the recorded source. Current source revision, local ownership/adaptations and partial-update exceptions live in maintenance guidance, without a log or machine-specific paths.

On meaningful work, load applicable instructions, discovery and concise core, then select relevant methods/support. Reuse current context until stale or insufficient. Headers identify responsibility/lifecycle; `read-with` is a hint, not recursion. No Markdown parser or body schema is required.

Composition carries one task's scope, findings, priorities and evidence through selected skills. Orient once, perform authorized work, verify at relevant checkpoints, then synthesize material understanding. `yaiml-to-do` bounds feasible original priorities; `yaiml-audit` accepts perspectives. Neither task counts nor skill invocations authorize subagents. Read-only and unchanged tasks remain respected.

Growth distinguishes facts from methods: add specialist memory for recurring knowledge and project skills for recurring procedures. Update an existing owner first; avoid empty artifacts and speculative rules. Refresh compares incoming guidance, the applied baseline where available and current adaptations. Preserve local skills, authority and unresolved conflicts; healthy repeat setup is unchanged. [Skills And Project Lifecycle](SKILLS_AND_LIFECYCLE.md) owns the fuller rationale.

## Evidence And Integration

Present files, configured routes and observed fresh-session use are distinct claims. The public prompt cannot retrieve unpublished working-tree resources. Missing access yields explicit partial setup, not fabricated completeness. No background maintenance is implied.

Memory describes its checkout. Routine edits stay passage-scoped; broad reorganization is separately authorized. Before integration compare actual target/common ancestor, preserve independent contributions, resolve semantic conflicts through existing authority and recheck affected evidence. A clean merge is insufficient.

## Deferred And Retired Approaches

YAIMLACP uses existing host subagents after affirmative scoped confirmation; it adds no server, SDK, installation or runner and claims no standard MCP interoperability. Skills can be used by one agent. Host controls govern enforceable limits; documentation cannot enforce them.

`SPEC.md` as normative center, Markdown schemas, JSON-LD systems, conformance fixtures, custom `.yaiml` file formats and provider implementation libraries remain retired or outside this phase. The `.yaiml/` directory is ordinary storage. Preserve the [approved license](../LICENSE.md) and [independence declaration](PROJECT_INDEPENDENCE.md); tooling, licensing and governance changes remain human decisions.
