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

The practical goal is simple: a developer keeps a small, visible, versioned guiding document family inside a project so future AI sessions inherit the project's state, past, risks, constraints, dependencies, definitions, preferences, rules, and operating shape.

YAIML should feel like an observation platform for a project: high enough to see what the project is, where it has been, what matters now, what is risky, and what the next agent must not casually distort.

## Current Concept

Declared: YAIML is an incubating plain-file convention and framework of ideas for AI Project Engineering: project management, project memory, project definition, constraints, and agent continuity. It is not primarily a schema, formal specification, YAML dialect, parser target, contract system, package dependency, runtime, database, hosted memory service, agent SDK, required CLI, or compliance framework.

Declared: YAIML is an idea and documentation framework, not professional legal, security, compliance, privacy, licensing, or IP advice. Security, compliance, privacy, legal, licensing, and IP documents are memory surfaces for project-specific reviewed constraints, evidence, decisions, and open questions, not recommendations supplied by YAIML itself.

Declared: YAIML's value is the convention it expresses, not the documents as standalone artifacts. The documents, templates, prompts, examples, and future helpers exist only to preserve project understanding across coding-agent sessions.

Verified: This repository is currently plain Markdown and YAML guidance, templates, prompts, one robust fictional example, an evaluation guide, a cold-start review note, a restrictive incubation-phase all-rights-reserved notice, a public security/sensitive-information policy, and YAIML's own project-memory documents. It does not include a CLI, SDK, parser, package manifest, validator, web app, database, hosted service, or provider adapter.

## Current Artifact Set

- `README.md`: public entry point, quick start, concept summary, and current/future boundary.
- `LICENSE.md`: restrictive incubation-phase rights notice; public visibility does not grant open-source reuse.
- `SECURITY.md`: public guidance for sensitive reports and memory-hygiene risks.
- `CONTRIBUTING.md`: contribution guardrails for preserving the concept.
- `ROADMAP.md`: convention-first priorities and deferred-tooling boundary.
- `yaiml.yml`: discovers this repository's YAIML document family.
- `docs/SoTY.md`: current engineering state for YAIML.
- `docs/ARCHITECTURE.md`: durable conceptual architecture and artifact responsibilities.
- `docs/MAINTAINER_GUIDE.md`: current maintenance procedures and review checks.
- `docs/CONCEPTS.md`, `docs/CORE_DOCUMENT_FAMILY.md`, `docs/STABLE_HEADERS.md`, `docs/AMBIGUITY_AND_EVIDENCE.md`, `docs/PRUNING_AND_LIFECYCLE.md`: supporting guidance.
- `docs/AGENT_INTEGRATION.md`: boundary and snippets for connecting YAIML to agent instruction files.
- `docs/CONTEXT_LOADING.md`: bounded discovery/core/task/deep context-loading model.
- `docs/EVALUATION.md`: real-project case-study template and cold-start comparison method.
- `docs/COLD_START_REVIEW.md`: latest first-time-agent usability review.
- `templates/core/`: starter SoT, Architecture, and Maintainer Guide.
- `templates/supporting/`: supporting document starters for self-unfolded roles such as domain, legal/compliance, preferences, product doctrine, risk review, security memory, and terms/glossary.
- `prompts/`: provider-neutral workflows for initialization, hydration, updating, auditing, pruning, and realignment.
- `prompts/init-yaiml.md`: smallest useful one-time adoption prompt.
- `examples/canopy-dispatch/`: robust fictional example with SoTD, architecture, maintainer, and release/trust memory.

## Initial Audience

Developers using Codex, Claude, Gemini, Cursor, local models, or future coding agents on projects where source code alone does not preserve enough meaning.

## Decided

- The first release is convention-first and no-install.
- Protect the philosophy before expanding the framework.
- The core engineering frame is AI Project Engineering.
- SoT is the central artifact. SoT means State Of The.
- `SOT.md` is the recommended default SoT filename for unfamiliar repositories; project-specific names such as this repository's `SoTY.md` remain supported when they add useful project character.
- The default family is SoT, Architecture, and Maintainer Guide.
- YAIML now has two initialization paths: `init-yaiml.md` for quick adoption and `initialize-yaiml.md` for deeper initialization.
- YAIML distinguishes agent instruction files from project memory: instruction files tell agents how to behave; YAIML preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.
- YAIML uses bounded context loading: discovery, core, task-relevant supporting documents, then deep references only when needed.
- YAIML should self-unfold beyond the core family when a project needs durable homes for preferences, legal, contracts or agreements, concepts, terms, risk review, security, data, testing, UX, domain, deployment, release, operations, product doctrine, world or lore, provider integration, remote access, or other project-specific guidance.
- YAIML documents should usually be versioned with the source code; initialization should not add them to `.gitignore` by default.
- YAIML documents should be ordinary visible Markdown by default, not a custom `.yaiml` extension, hidden folder, cache, or tool-state format.
- YAIML documents must not store raw secrets, credentials, tokens, private keys, passwords, customer personal data, or sensitive raw values.
- AI-generated legal, licensing, ownership, copyright, trademark, patent, contract, or IP statements require caution. Preserve human-approved statements and uncertainty; do not invent rights claims.
- Every YAIML document starts with a short stable header.
- Human intent and implementation evidence must remain separate.
- Ambiguity must be visible when it can affect future work.
- Pruning is part of the method, especially for SoT.
- Tooling is deferred.
- A future startup helper may improve on the one-time init flow, but YAIML should remain plain project-local files, not a package-manager dependency, runtime library, hosted platform, or build step.
- Every proposed addition should answer: does this improve a new coding agent's ability to reconstruct the project's current engineering understanding?
- The repository may be public for visibility, but it is not open source yet. The maintainer intends to choose an open license before broad public adoption, but no license or date has been selected.

## Meaningful Accomplishments

- The repository has been realigned away from schema/conformance/spec framing and toward a convention-first AI Project Engineering framework.
- The core document family is centered on SoT, with project-specific Markdown filenames such as `SoTY.md`, `SoTT.md`, or `SoTC.md`.
- Stable headers now act as agent-facing orientation instead of rigid document contracts.
- The README, guides, templates, prompts, and fictional example now teach YAIML as a self-unfolding project-memory and project-definition document family.
- `prompts/init-yaiml.md` provides the small adoption path; `prompts/initialize-yaiml.md` remains the full self-contained initialization prompt for deeper repository setup.
- Live init trials clarified that command results should be recorded inside generated YAIML documents, not only in final chat output.
- `docs/AGENT_INTEGRATION.md` clarifies the boundary between agent behavior instructions and YAIML project memory.
- `docs/CONTEXT_LOADING.md` prevents self-unfolding from becoming read-everything-by-default context loading.
- `docs/EVALUATION.md` adds a real-project evidence path without inventing adoption or performance proof.
- `templates/optional/` has been renamed to `templates/supporting/` to avoid implying supporting documents are decorative extras.
- Supporting guidance now protects the plain-file boundary: visible Markdown, versioned by default, no `.yaiml` extension, no hidden tool-state folder, no package dependency.
- Supporting guidance now protects memory hygiene: no secrets or sensitive raw values, and no agent-invented legal/IP/security/compliance conclusions.
- Declared supporting YAIML guides now have stable headers, matching the repository's own stable-header rule.
- A public security/sensitive-information policy now tells contributors not to place secrets, personal data, exploit details, or confidential project information into public YAIML materials.

## Current Strengths

- A developer can use YAIML today with ordinary Markdown files; prompts are optional helpers for setup, repair, audit, pruning, and realignment.
- The central SoT role is distinct from Architecture and Maintainer Guide.
- The front door now presents YAIML as a one-time init plus repository-carried project memory, not a sequence of repeated pasted prompts.
- The intended day-to-day interaction can be natural human language such as "continue through the SoT priorities" or "update our SoT" because the repository already holds the guiding context.
- The self-unfolding document model can adapt to project domains without requiring every project to use every document.
- The context-loading model keeps the core family bounded and makes supporting documents task-relevant rather than automatically loaded.
- Authority and evidence guidance clearly separates human intent from implementation reality.
- Pruning guidance directly addresses append-only state bloat.
- The no-dependency/no-custom-format boundary is visible in the README, Architecture, Roadmap, and initialization prompt.
- The repository now has a lightweight method for collecting real-project case studies and cold-start comparison evidence.
- The repository dogfoods its own framework.

## Current Weaknesses

- The framework has one robust fictional example, but it still needs adoption trials on real repositories.
- The SoT naming posture now favors `SOT.md` as the boring default while preserving project-specific names; this still needs validation with first-time readers.
- The manifest is useful for discovery, but it is not yet proven whether it should be required for all adopters.
- The prompt pack has not yet been exercised enough to know which instructions agents routinely miss; the minimum and full initialization prompts both need real-world validation.
- The context-loading guide is conceptually clear but untested under real context-window pressure.
- The case-study and cold-start evaluation method is only a proposed evidence path until used on real repositories.
- The future startup-helper shape is intentionally undefined; it needs to become better than copy-paste without becoming a package dependency or platform.
- The supporting template set must be kept useful without implying every possible memory domain deserves a starter file.
- The README still needs pressure toward human adoption clarity rather than internal framework explanation.
- The prompt library can easily read like a required operating checklist; it should remain framed as fallback and maintenance help for cases where the repository's own YAIML guidance is not enough.

## Active Risks

- Formalization drift: future changes could recreate schemas, conformance fixtures, normative spec language, package formats, or custom file extensions too early.
- Tooling drift: a future startup helper could become a dependency, runtime, hosted platform, or build step instead of serving project-local Markdown files.
- Ceremony drift: self-unfolding documents could become empty files if agents create every possible supporting role instead of only what the project needs.
- Context drift: agents could treat `yaiml.yml` as a command to load every document on every task, making YAIML too heavy for routine work.
- Safety drift: public or shared repositories could expose sensitive information if agents treat YAIML as private scratch space instead of sanitized project memory.
- Reporting drift: public issues or examples could include sensitive security details if the top-level security policy is missed or ignored.
- Advice drift: legal, security, compliance, privacy, licensing, or IP memory could be mistaken for professional recommendations if templates do not keep their memory-only role clear.
- Status-report drift: SoT could be misread as a status report instead of an engineering-state synthesis.
- Prompt drift: the prompt pack needs real use on varied repositories before its wording can be considered stable.
- Prompt-library drift: the README or guides could imply humans must paste separate prompts after every step, undermining YAIML's goal of repository-carried guidance.
- Terminology drift: YAIML could accumulate too many named concepts and become harder to explain than the problem it solves.
- Evidence drift: the fictional example could be mistaken for proof if real case studies are not gathered and labeled honestly.

## Immediate Priorities

1. Trial `init-yaiml.md` and `initialize-yaiml.md` on unrelated real repositories and record where agents misunderstand the concept.
2. Apply the cold-start evaluation method to real projects without overclaiming results.
3. Test whether agents choose useful self-unfolded supporting documents without creating empty ceremony, using the "several concrete recurring pieces of knowledge" heuristic.
4. Test whether the context-loading model keeps routine tasks bounded while still surfacing task-relevant supporting memory.
5. Test whether agents keep YAIML versioned by default while sanitizing secrets, sensitive data, and legal/IP/security/compliance claims.
6. Explore a better startup helper shape while preserving the plain-file, no-dependency boundary.
7. Keep the fictional example detailed enough to teach the pattern without implying it is proof.
8. Refine pruning behavior from actual overgrown SoT documents.
9. Prepare open-license and public-release readiness criteria for human decision.
10. Preserve YAIML's own dogfood documents after material changes.

## Known Divergence

No active divergence currently identified in the repository's declared concept versus current artifact shape.

Resolved: an earlier version centered on `SPEC.md`, schemas, conformance fixtures, and formal standard language. That material was removed during the foundational realignment.

Resolved: later refinements clarified stable headers, SoT naming, self-unfolding supporting documents, versioned-by-default memory, ordinary Markdown files, safety/legal/IP hygiene, bounded context loading, init versus full initialization, evaluation evidence paths, prompt-library fallback framing, and the no-dependency startup-helper boundary.

## Rejected Framings

- YAIML is not primarily a YAML format.
- YAIML is not a parser or validation target first.
- YAIML is not a generic memory database.
- YAIML is not a replacement for source code, tests, Git history, issues, or `AGENTS.md`.
- YAIML is not a custom document file extension.
- YAIML is not proof of agent productivity by itself.
- YAIML is not a finished software platform.

## Future Possibilities

Possible later tooling includes repository initialization, document discovery, freshness checks, document health reviews, pruning assistance, context assembly, IDE integration, and coding-agent adapters. These should serve the framework after the Markdown workflow proves itself, and should preserve project-local YAIML files as the source of truth.

## Open Questions

- What eventual public/open-source license, if any, should govern the repository and templates?
- How strongly should YAIML enforce project-specific SoT filenames such as `SoTY.md`, `SoTT.md`, or `SoTC.md`?
- Is `yaiml.yml` essential for the no-tooling phase, or should it be recommended but optional?
- How strict should future tooling be without damaging the interpretive value of YAIML?
- Which self-unfolded document roles are common enough to deserve first-class templates?
- What is the smallest useful startup helper, if tooling becomes appropriate, that improves on copy-paste without becoming a dependency or platform?
- Which open license should be selected before broad public adoption?
- What evidence threshold is enough to describe YAIML as a reusable standard rather than an incubating convention?
