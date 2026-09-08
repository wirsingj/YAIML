---
yaiml: 0.2
kind: architecture
title: YAIML Architecture
purpose: Preserve YAIML's durable conceptual model, artifact boundaries, and deferred tooling boundaries.
belongs-here: conceptual architecture, artifact responsibilities, role boundaries, deferred approaches.
not-here: current priorities, command procedures, complete file inventory.
durability: durable; update when roles, artifact responsibilities, or deferred tooling boundaries change.
read-with: SoTY; YAIML Maintainer Guide.
agent-guidance: Verify repository shape before claiming artifacts. Surface conflicts. Preserve human direction.
---

# YAIML Architecture

## System Model

YAIML is a documentation convention. This repository supplies reference guidance, prompts, templates, examples, and its own living project memory. Adopters keep ordinary Markdown files in their repositories; no YAIML runtime participates in their application or build.

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
| templates/ | Optional starters, adapted rather than copied as empty forms |
| prompts/init-yaiml.md | Self-contained adoption instructions |
| Other prompts/ | Explicit orientation, audit, update, compression, refresh, and realignment helpers |
| examples/ | Minimal and larger fictional document families, plus a short demo; no application code |
| docs/case-studies/ and COLD_START_REVIEW.md | Evidence notes with scope and limitations |

The reference repository contains more documents than a typical adopter needs because it explains the convention. Initialization should not reproduce this inventory in an adopting project.

## Reading And Maintenance Boundaries

The normal loading sequence is discovery, three concise core documents, then task-relevant supporting material. History and specialist references load only when needed. A `read-with` header is a relevance hint, not a recursive import.

Headers communicate role, responsibility, lifecycle, update triggers, and evidence/conflict behavior. Field names, titles, wording, and body sections remain adaptable. No Markdown parser or conformance checker is required.

The init prompt deliberately repeats the minimum convention because it must work when copied alone. Other guides should link to the topic’s owner instead of repeating full explanations.

The init prompt is the primary adoption interface. It must retain enough context to work independently, with bounded inspection and no installation requirement. External coordinating tools are optional users of the files; none is a dependency or part of the adoption path.

Persistent repository instructions carry the routine reading and maintenance behavior into later sessions. Initialization connects the active agent's supported mechanism; a discovery file alone cannot activate an agent. Configured instructions and observed loading are different evidence. No background process maintains memory between sessions.

## Deferred And Retired Approaches

During the convention-first phase, do not add implementation libraries, CLIs, SDKs, provider adapters, package manifests, services, databases, orchestration, or web applications. A future helper would serve project-local files without becoming an adopter’s runtime or build dependency.

`SPEC.md` as the normative center, Markdown schemas, JSON-LD metadata systems, conformance fixtures, RFC-style requirements, and custom `.yaiml` memory files are retired for this phase. Do not revive them without an explicit human phase change. Any future validation should be limited to the discovery map.

Preserve the MIT License and the maintainer’s [independence declaration](PROJECT_INDEPENDENCE.md). Tooling, licensing, release labeling, and governance changes remain human decisions.
