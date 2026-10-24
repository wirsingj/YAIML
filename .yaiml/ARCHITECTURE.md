---
yaiml-revision: "0.33.73aaa0d992e327de"
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

Include any [pending corrections](changes.md).

## System Model

One pasted networked init runs bootstrap through host tools; its self-contained offline peer embeds minimal memory/record rules without retrieval or skill acquisition. Both establish project memory and connect supported future sessions. Optional commands select ordinary-work methods. YAIML adds no runtime or background process.

This repository develops and publishes YAIML while using it to manage its own development. Its core memory describes this project; adopters receive methods and establish their own context. Repository maintenance and adopter behavior require separate evidence.

`.yaiml/` is the default home for discovery, memory, skills and reusable resources. Host instructions and public/legal entry points remain in their supported locations. Discovery paths resolve relative to their map; mature layouts are compatibility inputs, not replacement targets. [Adoption And Updates](ADOPTION_AND_UPGRADES.md) owns compatibility.

## Owners And Boundaries

| Owner | Responsibility |
| --- | --- |
| SoT | Current direction, capabilities, risks, priorities, divergence and uncertainty |
| Architecture | Durable responsibilities, invariants, design and relevant rationale |
| Maintainer Guide | Procedures, verification/recovery and current source/adaptation notes |
| changes.md | Retained iteration audit: intent, parents, affected paths and scoped verification |
| Supporting memory | Recurring specialist knowledge or distinct retention |
| `skills/yaiml-*/SKILL.md` | Reusable methods with triggers, inputs, actions and outcomes |
| `YAIML_GUIDE.md` / `CHANGE_RECORDS.md` | Shared loop / retained records and ownership-based consolidation |
| `skills/INDEX.md` | Selection by purpose and local reachability |
| Host instructions / native entries | Activation, scope and argument forwarding into canonical methods |
| Init / Bootstrap | Entry seed, source acquisition, adoption and repair |
| Templates / optional prompts | Dormant writing aids / alternative entry points to owning skills |

Facts have one detailed memory owner; methods read current facts rather than embedding copies. Host entries are thin routes, not competing implementations. This repository uses `.agents/skills/` entries pointing to `.yaiml/skills/`; other hosts need their supported mechanisms. [Core Document Family](CORE_DOCUMENT_FAMILY.md) owns role guidance.

## Lifecycle

The seed names the official repository and bootstrap path without assuming YAIML context. Init/refresh defaults to reviewed release ref `v0.5.1`, resolved once to an exact commit throughout acquisition. Prompt stamps track documents; the release ref pins the source. Alternative sources/refs require explicit user requests; floating `main` is for explicit testing only. Unavailable pins never trigger fallback. Bootstrap grounds memory in target evidence, excluding source-project facts and policies; acquisition need not load every body or execute each method.

The offline base supplies methods, shared/revision rules, release identity, coordination guidance, starters and notice. Bootstrap governs further acquisition; maintenance guidance records applied sources/adaptations, and the audit retains changes without private paths.

The guide owns context, work, verification and maintenance. Reuse context; select specialized methods when needed. Routine completion loads revision steps; migration/integration detail is conditional. `read-with` is a relevance hint.

Composition carries one task's scope, findings, priorities and evidence through selected skills. Orient once, perform authorized work, verify at relevant checkpoints, then synthesize material understanding. `yaiml-to-do` bounds feasible original priorities; `yaiml-audit` accepts perspectives. Neither task counts nor skill invocations authorize subagents. Read-only and unchanged tasks remain respected.

Growth distinguishes facts from methods: add specialist memory for recurring knowledge and project skills for recurring procedures. Update an existing owner first; avoid empty artifacts and speculative rules. Refresh compares incoming guidance, the applied baseline where available and current adaptations. Preserve local skills, authority and unresolved conflicts; healthy repeat setup is unchanged. [Skills And Project Lifecycle](SKILLS_AND_LIFECYCLE.md) owns the fuller rationale.

## Evidence And Integration

Present files, configured routes and observed fresh-session use are distinct claims. The public prompt cannot retrieve unpublished working-tree resources. Missing access yields explicit partial setup, not fabricated completeness. No background maintenance is implied.

[Revision lineage](VERSIONING.md) separates product, discovery and local versions. Changed managed Markdown is stamped; all affected paths enter the audit. [Change Records](CHANGE_RECORDS.md) composes snapshots with pending corrections. Sole ownership permits ordinary consolidation; overlap or uncertainty defers it. Navigation is repaired immediately; incorporated records remain history. No mode switch or global worker detector is supplied. Semantic-merge tooling, gatekeepers and CI validators are external projects consuming stable YAIML formats and integration points; this repository builds none. A clean merge still requires authority/evidence review.

## Deferred And Retired Approaches

YAIMLACP uses host subagents after affirmative scoped confirmation, without added infrastructure or claimed MCP interoperability. Skills can be used by one agent. Host controls govern enforceable limits; documentation cannot enforce them.

`SPEC.md` as normative center, schemas for free-form memory bodies, JSON-LD systems, conformance fixtures, custom `.yaiml` file formats and provider implementation libraries remain retired or outside this phase. The small record frontmatter/body contract is owned by Change Records for external consumers; it adds no tooling. The `.yaiml/` directory is ordinary storage. Preserve the [approved license](../LICENSE.md) and [independence declaration](PROJECT_INDEPENDENCE.md); tooling, licensing and governance changes remain human decisions.
