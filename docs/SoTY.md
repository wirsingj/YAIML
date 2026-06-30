---
yaiml: 0.1
kind: sot
title: SoTY
purpose: Preserve YAIML's current meaning, direction, risks, and immediate priorities.
belongs-here: current project identity, purpose, artifact set, strengths, weaknesses, risks, priorities, divergence, useful lessons.
not-here: complete history, permanent architecture, command reference.
durability: volatile; synthesize and prune aggressively.
read-with: YAIML Architecture; YAIML Maintainer Guide.
update-when: project concept, core artifacts, active risks, or priorities change materially.
agent-guidance: Verify repository shape. Preserve human direction. Mark uncertainty. Surface conflicts. Prune stale rewrite history.
---

# SoTY

## North Star

YAIML preserves the current interpreted understanding of a software project across disposable coding-agent sessions.

The practical goal is simple: a developer can copy a small document family and paste prompts into a coding agent so future sessions inherit current engineering state, architecture, and practical operating knowledge.

## Current Concept

Declared: YAIML is a lightweight project-context system for AI Project Engineering. It is not primarily a schema, formal specification, YAML dialect, parser target, contract system, or compliance framework.

Verified: This repository is currently plain Markdown and YAML guidance, templates, prompts, one robust fictional example, a cold-start review note, and YAIML's own project-memory documents. It does not include a CLI, SDK, parser, package manifest, validator, web app, provider adapter, or license file.

## Current Artifact Set

- `README.md`: public entry point, quick start, concept summary, and current/future boundary.
- `yaiml.yml`: discovers this repository's YAIML document family.
- `docs/SoTY.md`: current engineering state for YAIML.
- `docs/ARCHITECTURE.md`: durable conceptual architecture and artifact responsibilities.
- `docs/MAINTAINER_GUIDE.md`: current maintenance procedures and review checks.
- `docs/CONCEPTS.md`, `docs/CORE_DOCUMENT_FAMILY.md`, `docs/STABLE_HEADERS.md`, `docs/AMBIGUITY_AND_EVIDENCE.md`, `docs/PRUNING_AND_LIFECYCLE.md`: supporting guidance.
- `templates/core/`: starter SoT, Architecture, and Maintainer Guide.
- `templates/optional/`: optional supporting document starters.
- `prompts/`: provider-neutral workflows for initialization, hydration, updating, auditing, pruning, and realignment.
- `examples/canopy-dispatch/`: robust fictional example with SoTD, architecture, maintainer, and release/trust memory.

## Initial Audience

Developers using Codex, Claude, Gemini, Cursor, local models, or future coding agents on projects where source code alone does not preserve enough meaning.

## Decided

- The first release is convention-first and no-install.
- The core engineering frame is AI Project Engineering.
- SoT is the central artifact. SoT means State Of The.
- A real project should usually expand SoT with a final project letter, as this repository does with `SoTY`.
- The default family is SoT, Architecture, and Maintainer Guide.
- Every YAIML document starts with a short stable header.
- Human intent and implementation evidence must remain separate.
- Ambiguity must be visible when it can affect future work.
- Pruning is part of the method, especially for SoT.
- Tooling is deferred.

## Meaningful Accomplishments

- The repository has been realigned away from formal schema/conformance framing and toward a usable AI Project Engineering framework.
- The core document family has been clarified as SoT, with project-specific filenames such as `SoTY.md`, `SoTT.md`, or `SoTC.md`.
- Stable headers now replace the earlier heavier document-contract framing.
- The README explains the problem, the immediate workflow, and the current/future boundary.
- Core templates and the fictional example use SoT, Architecture, and Maintainer Guide consistently.

## Current Strengths

- A developer can use YAIML today with only Markdown files and prompts.
- The central SoT role is distinct from Architecture and Maintainer Guide.
- Authority and evidence guidance clearly separates human intent from implementation reality.
- Pruning guidance directly addresses append-only state bloat.
- The repository dogfoods its own framework.

## Current Weaknesses

- The framework has one robust fictional example, but it still needs adoption trials on real repositories.
- The SoT naming decision is recent and may need validation with first-time readers.
- The manifest is useful for discovery, but it is not yet proven whether it should be required for all adopters.
- The prompt pack has not yet been exercised enough to know which instructions agents routinely miss.

## Active Risks

- YAIML could drift back toward formal-standard habits if future changes recreate schemas, conformance fixtures, contract-system framing, or normative spec language too early.
- Templates could become generic documentation rather than agent-maintained project memory.
- The stable header could bloat into a field schema instead of staying a readable agent orientation.
- The prompt pack needs real use on varied repositories before its wording can be considered stable.
- SoT could be misread as a status report unless examples keep showing it as an engineering-state synthesis.

## Immediate Priorities

1. Use the templates and prompts on real projects.
2. Keep the fictional example detailed enough to teach the pattern without implying it is a source-project copy.
3. Refine pruning behavior from actual overgrown SoT documents.
4. Preserve YAIML's own dogfood documents after material changes.
5. Decide licensing only with explicit human approval.

## Known Divergence

Resolved in current repository shape: the previous version centered on `SPEC.md`, schemas, conformance fixtures, and formal standard language. That material was removed during the foundational realignment. The current refinement also reframed document headers as stable agent guidance and centered AI Project Engineering plus SoT.

## Rejected Framings

- YAIML is not primarily a YAML format.
- YAIML is not a parser or validation target first.
- YAIML is not a generic memory database.
- YAIML is not a replacement for source code, tests, Git history, issues, or `AGENTS.md`.
- YAIML is not a finished software platform.

## Future Possibilities

Possible later tooling includes repository initialization, document discovery, freshness checks, document health reviews, pruning assistance, context assembly, IDE integration, and coding-agent adapters. These should serve the framework after the Markdown workflow proves itself.

## Open Questions

- What license should govern the repository and templates?
- How strongly should YAIML enforce project-specific SoT filenames such as `SoTY.md`, `SoTT.md`, or `SoTC.md`?
- Is `yaiml.yml` essential for the no-tooling phase, or should it be recommended but optional?
- How strict should future tooling be without damaging the interpretive value of YAIML?
- Which optional document roles are common enough to deserve first-class templates?
- What is the smallest useful project initializer, if tooling becomes appropriate?
