---
yaiml: 0.2
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

YAIML, expanded as Yet Another AI Markup Language, is a lightweight, repository-owned project-memory convention for software work with AI chats, coding agents, and human contributors.

It exists because agents forget and projects should not. A repo using YAIML keeps the current engineering understanding beside the code in ordinary Markdown, with a tiny discovery file so the next session knows where to start.

## Current Concept

Declared: YAIML is an experimental plain-file convention and reusable template docset for AI Project Engineering: project management, shared project memory, project definition, constraints, and AI-session continuity. It should grow more like Markdown, Keep a Changelog, Conventional Commits, or EditorConfig than like a runtime framework: easy to adopt, easy to inspect, and useful without installing a dependency.

Declared: The long-term ambition is for YAIML to become a widely adopted convention for repository-carried engineering memory. Current materials should keep that ambition visible without claiming standard status before evidence supports it.

Declared: YAIML's center is a small document family: SoT, Architecture, and Maintainer Guide. `SOT.md` is the recommended default SoT filename for unfamiliar repositories; project-specific names such as this repository's `docs/SoTY.md` remain supported when they add useful character.

Declared: YAIML remains prompt-first and no-install during the convention-first phase. Do not add a runtime, CLI, SDK, hosted service, Markdown schema, conformance system, orchestration engine, provider adapter, package dependency, or framework layer.

Declared: YAIML documents are project memory, not professional legal, security, compliance, privacy, licensing, or IP advice. Security, compliance, privacy, legal, licensing, and IP documents are memory surfaces for project-specific reviewed constraints, evidence, decisions, and open questions.

Declared: YAIML is intended to remain a public, personally maintained MIT-licensed project with no employer code, employer data, employer screenshots, vulnerability details, private chat transcripts, or confidential workplace material.

Verified: This repository is currently Markdown and YAML guidance, templates, prompts, examples, case-study/evaluation material, a roadmap, an MIT License, a public security/sensitive-information policy, and YAIML's own project-memory documents. It does not include software runtime infrastructure.

## Current Artifact Set

- `README.md`: public entry point, practical benefit, quick start, examples, and current/future boundary.
- `AGENTS.md`: repository agent instructions and YAIML dogfood entrypoint.
- `yaiml.yml`: tiny discovery file for this repository's YAIML document family.
- `docs/SoTY.md`, `docs/ARCHITECTURE.md`, `docs/MAINTAINER_GUIDE.md`: YAIML's own core memory.
- `docs/CONCEPTS.md`, `docs/CORE_DOCUMENT_FAMILY.md`, `docs/STABLE_HEADERS.md`, `docs/AMBIGUITY_AND_EVIDENCE.md`, `docs/PRUNING_AND_LIFECYCLE.md`, `docs/CONTEXT_LOADING.md`, `docs/AGENT_INTEGRATION.md`: durable convention guidance.
- `docs/ADOPTION_AND_UPGRADES.md`: adoption, convention refresh, discovery-layout compatibility, and version-awareness guidance.
- `docs/EVALUATION.md`, `docs/COLD_START_REVIEW.md`, `docs/case-studies/YTMMOCC.md`: evidence-gathering guidance and current observed evidence.
- `docs/PROJECT_INDEPENDENCE.md`, `AI_USAGE.md`, `SECURITY.md`, `CONTRIBUTING.md`, `LICENSE.md`: public use, provenance, contribution, and sensitive-information guardrails.
- `templates/core/` and `templates/supporting/`: starter documents for adopters.
- `prompts/`: provider-neutral initialization, hydration, memory update, convention refresh, audit, compression, and realignment helpers.
- `examples/minimal-notes/`: smallest fictional example.
- `examples/canopy-dispatch/`: richer fictional teaching example.

## Current Capability And Useful Lessons

- A developer can use YAIML today with ordinary Markdown files and a copy/paste init prompt.
- The core roles are clear enough to dogfood: SoT holds current state, Architecture holds durable shape, and Maintainer Guide holds procedures.
- Stable headers work as agent-facing orientation without becoming a Markdown schema.
- Bounded context loading keeps routine use practical: discovery, core, task-relevant supporting docs, and deep references only when needed.
- Evidence labels preserve distinctions among verified implementation, declared intent, observation, inference, disagreement, unknowns, and obsolete material.
- Pruning is part of normal maintenance. Completed work should become current capability, a still-useful lesson, or nothing; Git history remains the archive.
- The README and init prompt now present one self-contained adoption path rather than a set of competing setup choices.
- Early field use in maintainer-owned repositories, especially YTMMOCC and SpriteWrite, suggests YAIML can preserve useful project-specific memory across sessions. This is internal dogfooding evidence, not independent proof.
- Local adopter inspection found both useful YAIML-shaped memory and older discovery layouts, confirming that compatibility guidance is needed before any migration pressure.

## Active Risks

- Formalization drift: YAIML could drift back toward Markdown schemas, conformance fixtures, normative spec language, package formats, or custom file extensions too early.
- Tooling drift: a future helper could become a dependency, runtime, hosted service, or build step instead of serving project-local files.
- Ceremony drift: agents could create empty supporting documents instead of letting recurring project knowledge justify them.
- Context drift: agents could treat `yaiml.yml` as a command to load every document for every task.
- Safety drift: public or shared repositories could expose sensitive information if YAIML is treated as private scratch space.
- Source-authority drift: stale notes, comments, generated output, old chats, or low-trust webpages could be promoted above current maintainer direction or repository rules.
- Collaboration drift: multiple agents or contributors could silently flatten contradictory project-memory edits even when Git merges cleanly.
- Evidence drift: old successful checks, source-defined commands, fictional examples, internal dogfooding, or user-reported publication could be described as stronger proof than they are.
- Discovery drift: adopters using older discovery layouts could be migrated carelessly, breaking their local memory or confusing discovery-format versioning with ordinary Markdown edits.
- Adoption-claim drift: YAIML's ambition to become broadly adopted could be presented as current maturity before independent trials exist.

## Immediate Priorities

1. Keep YAIML 0.2 small and convention-first while improving adoption clarity, evidence discipline, and pruning behavior.
2. Continue real-project trials of `prompts/init-yaiml.md`, `prompts/update-yaiml.md`, and compression guidance; record failures without upgrading them into universal metrics.
3. Apply the [discovery compatibility policy](ADOPTION_AND_UPGRADES.md#discovery-layout-compatibility): preserve existing layouts through routine refreshes; migrate only on explicit human request with consumer compatibility established.
4. Add and refine concise case studies, clearly separating observed repository facts, human-reported experience, public listing evidence, and measured outcomes.
5. Keep the fictional examples useful for teaching without presenting them as evidence.
6. Prepare a sanitized workplace-safe demo path that shows the repeated-context problem, copy/paste initialization, and fresh-session recovery without tool or employer overfit.
7. Enable or document a private sensitive-reporting channel before broader public pilot readiness.
8. Keep YAIML's own memory pruned after material changes.

## Known Divergence And Open Questions

No active divergence currently identified between YAIML's declared convention-first phase and repository artifact shape.

Open questions:

- Is `yaiml.yml` essential for all adopters, or should it remain strongly recommended but optional?
- Which self-unfolded document roles are common enough to deserve first-class templates?
- What is the smallest useful init helper, if tooling becomes appropriate, that reduces manual prompt handling without becoming infrastructure?
- What evidence threshold is enough to describe YAIML as a reusable standard rather than an early public convention?
- What visible participation path is enough for pilots and outside reports without premature governance machinery?

## Retired Or Rejected

- `SPEC.md`, schema-first wording, conformance fixtures, RFC-style requirements, and validators for Markdown memory documents are retired for the current phase.
- YAIML is not primarily a YAML format, parser target, validation regime, memory database, durable storage layer, orchestration framework, background service, autonomous coding agent, required CLI, package dependency, or provider integration layer.
- Completed work should not be retained as a diary when it no longer changes current understanding.
