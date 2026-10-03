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

YAIML is a project-memory initiative centered on a documentation convention. This repository supplies guidance, prompts, templates, examples, and living project memory. Adopters keep ordinary Markdown files; no YAIML runtime is required in their application or build.

`yaiml.yml` maps document roles to paths. It is a discovery index, not a schema for memory bodies. Discovery compatibility belongs in [Adoption And Updates](ADOPTION_AND_UPGRADES.md).

## Core Responsibilities

- **SoT:** current engineering state, direction, capabilities, risks, priorities, divergence, and unresolved questions.
- **Architecture:** durable boundaries, responsibilities, invariants, intended design, and relevant retired approaches.
- **Maintainer Guide:** current procedures, focused checks, diagnostics, and failure recovery.
- **Supporting documents:** recurring specialist knowledge that needs its own responsibility or retention rule.

[Core Document Family](CORE_DOCUMENT_FAMILY.md) owns the adopter-facing role guidance. Each fact should have one detailed home; other documents can summarize and link when their readers need it.

## Repository Surfaces

| Surface | Responsibility |
| --- | --- |
| README | Definition, one adoption path, limits, and navigation |
| Root policies and ROADMAP | Contributions, licensing, sensitive reporting, AI disclosure, future direction |
| AGENTS.md | Instructions for contributors’ agents working on YAIML itself |
| docs/SoTY.md, this file, Maintainer Guide | YAIML’s own current state, architecture, and procedures |
| Other docs/ guides | Reference explanations by topic |
| templates/ | Document starters and portable operating guidance; sources for embedded init text |
| prompts/init-yaiml.md | Self-contained seed: setup, pointer, operating guide, templates, coordination, and copied-material notice |
| Other prompts/ | Optional standalone entry points to six workflows also carried by init's saved operating guide |
| examples/ | Minimal and larger fictional document families, plus a short demo; no application code |
| docs/case-studies/ and COLD_START_REVIEW.md | Evidence notes with scope and limitations |

Init retains reusable procedures and dormant starters locally. Saved instructions support ordinary work and explicit requests, context reuse, and maintenance of material changes, including confirmed conversational direction. Project-specific memory unfolds only for useful knowledge; reference-project facts, policies, case studies, and inventories do not transfer.

## Reading And Maintenance Boundaries

The normal loading sequence is discovery, three concise core documents, then task-relevant support. At startup and on context loading or refresh, consider coordination using available context; consult [YAIMLACP](YAIMLACP.md) for a concrete benefit. Persistent instructions carry its user-confirmation gate. History and specialist references load only when needed; `read-with` is a relevance hint, not a recursive import.

Headers communicate role, responsibility, lifecycle, update triggers, and evidence/conflict behavior. Field names, titles, wording, and body sections remain adaptable. No Markdown parser or conformance checker is required.

Init owns the instruction pointer and complete text for adoption/growth without downloads. Humans receive a readable opening; agents are the primary operational readers. Compress payloads while preserving obligations, conditions, exceptions, authority, context routes, headers, and syntax. Agents reconcile local instructions, operating guidance, dormant templates, and YAIMLACP; adopters own adaptations. Embedded copies match source guides/templates. No automatic upstream update or competing example policy is implied.

Persistent repository instructions carry reading and maintenance into later sessions. Initialization connects applicable existing tool routes and the active agent's supported mechanism to one shared memory family, preserving instruction scope. A discovery file alone cannot activate an agent. Configured instructions and observed loading are different evidence. No background process maintains memory between sessions. Memory follows its checkout through ordinary branch review. Routine edits reconcile affected passages; broad compression is separately scoped. Semantic integration follows existing decision authority, with no required coordinator or CI service.

## Deferred And Retired Approaches

YAIMLACP is a serverless handoff convention using native host subagents, not standard MCP. It adds no server, SDK, installation, or runner. Skills supply methods; the lead owns delegation, evidence review, and memory integration. Describe the option and obtain affirmative user confirmation before first use or changed scope/cost. Existing host controls govern access and enforceable limits; documentation alone cannot enforce them. Basic adoption remains no-install.

`SPEC.md` as the normative center, Markdown schemas, JSON-LD metadata systems, conformance fixtures, RFC-style requirements, and custom `.yaiml` memory files are retired for this phase. Do not revive them without an explicit human phase change. Memory-format validation stays limited to discovery; coordination messages require no parser or schema.

Preserve the MIT License and the maintainer’s [independence declaration](PROJECT_INDEPENDENCE.md). Tooling, licensing, release labeling, and governance changes remain human decisions.
