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

YAIML preserves the current interpreted understanding of a software repository across disposable AI chats, coding-agent sessions, and contributor handoffs.

The practical goal is simple: a person or team keeps a small, visible, versioned guiding document family inside a project so future AI sessions, agents, and contributors inherit the project's state, past, risks, constraints, dependencies, definitions, preferences, rules, and operating shape.

YAIML should feel like an observation platform for a project: high enough to see what the project is, where it has been, what matters now, what is risky, and what the next chat, agent, or contributor must not casually distort.

## Current Concept

Declared: YAIML is a lightweight plain-file convention and reusable template docset for AI Project Engineering: project management, shared project memory, project definition, constraints, and AI-session continuity. It should grow more like Markdown, Keep a Changelog, Conventional Commits, or EditorConfig than like a runtime framework: easy to adopt, easy to inspect, and useful without installing a dependency. It is not primarily a schema, formal specification, YAML dialect, parser target, contract system, package dependency, runtime, database, hosted memory service, agent SDK, required CLI, storage layer, autonomous coding agent, or compliance framework.

Declared: No established expansion for YAIML was found in the repository history inspected during restoration. YAIML remains the canonical name without an expanded form.

Declared: YAIML is an idea and documentation framework, not professional legal, security, compliance, privacy, licensing, or IP advice. Security, compliance, privacy, legal, licensing, and IP documents are memory surfaces for project-specific reviewed constraints, evidence, decisions, and open questions, not recommendations supplied by YAIML itself.

Declared: YAIML's value is the convention it expresses, not the documents as standalone artifacts. The documents, templates, prompts, examples, and future helpers exist only to preserve project understanding across AI chats, coding-agent sessions, and contributor handoffs.

Declared: YAIML portability is independent of the adopting project's business or licensing model. A project may be private, public, paid, free, open-source, or unreleased; once YAIML is used, its project-memory family should travel with that repository across machines, contributors, and AI chat provider instances.

Verified: This repository is currently plain Markdown and YAML guidance, templates, prompts, one robust fictional example, an evaluation guide, a cold-start review note, an MIT License, a public security/sensitive-information policy, and YAIML's own project-memory documents. It does not include a CLI, SDK, parser, package manifest, validator, web app, database, storage layer, orchestration framework, background service, hosted service, or provider adapter.

## Current Artifact Set

- `README.md`: public entry point, quick start, concept summary, and current/future boundary.
- `AGENTS.md`: repository agent instructions that require future AI chats and agents to read YAIML memory and recognize natural-language SoT and YAIML-refresh requests.
- `LICENSE.md`: MIT License; Jeff Wirsing retains copyright ownership while anyone may use the repository materials under the license terms.
- `SECURITY.md`: public guidance for sensitive reports and memory-hygiene risks.
- `CONTRIBUTING.md`: contribution guardrails for preserving the concept.
- `ROADMAP.md`: convention-first priorities and deferred-tooling boundary.
- `yaiml.yml`: tiny discovery file that records the active YAIML discovery version and points to this repository's YAIML document family.
- `docs/SoTY.md`: current engineering state for YAIML.
- `docs/ARCHITECTURE.md`: durable conceptual architecture and artifact responsibilities.
- `docs/MAINTAINER_GUIDE.md`: current maintenance procedures and review checks.
- `docs/CONCEPTS.md`, `docs/CORE_DOCUMENT_FAMILY.md`, `docs/STABLE_HEADERS.md`, `docs/AMBIGUITY_AND_EVIDENCE.md`, `docs/PRUNING_AND_LIFECYCLE.md`: supporting guidance.
- `docs/AGENT_INTEGRATION.md`: boundary and snippets for connecting YAIML to agent instruction files.
- `docs/CONTEXT_LOADING.md`: bounded discovery/core/task/deep context-loading model.
- `docs/EVALUATION.md`: real-project case-study template and cold-start comparison method.
- `docs/COLD_START_REVIEW.md`: latest first-time-agent usability review.
- `docs/ADOPTION_AND_UPGRADES.md`: adoption, upgrade, and version-awareness guidance.
- `templates/core/`: starter SoT, Architecture, and Maintainer Guide.
- `templates/supporting/`: supporting document starters for self-unfolded roles such as domain, legal/compliance, preferences, product doctrine, risk review, security memory, and terms/glossary.
- `prompts/`: provider-neutral workflows for initialization, hydration, project-memory update, YAIML convention refresh, audit, pruning, and realignment.
- `prompts/init-yaiml.md`: smallest useful one-time adoption prompt.
- `prompts/update-yaiml.md`: refresh workflow for adopting repositories that need to compare their local YAIML prompts/templates/guidance with a human-provided or workspace-local YAIML reference while preserving project-specific memory.
- `examples/canopy-dispatch/`: robust fictional example with SoTD, architecture, maintainer, and release/trust memory.

## Initial Audience

People and teams using Codex, Claude, Gemini, Cursor, local models, or future AI chats and coding agents on projects where source code alone does not preserve enough meaning.

Declared: YAIML should be usable by anyone evaluating or adopting the convention, including multi-agent and multi-contributor projects. Current reuse rights are governed by the MIT License in `LICENSE.md`.

## Decided

- The first release is convention-first and no-install.
- Protect the philosophy before expanding the framework.
- The core engineering frame is AI Project Engineering.
- SoT is the central artifact. SoT means State Of The.
- `SOT.md` is the recommended default SoT filename for unfamiliar repositories; project-specific names such as this repository's `SoTY.md` remain supported when they add useful project character.
- The default family is SoT, Architecture, and Maintainer Guide.
- YAIML now has two initialization paths: `init-yaiml.md` for quick adoption and `initialize-yaiml.md` for deeper initialization.
- YAIML revision `0.2` records the current convention-first docset posture.
- `yaiml.yml` now uses a tiny nested discovery protocol with SemVer under `yaiml.version`; the version applies to the discovery/config shape and reference posture, not to every sentence in the Markdown memory documents.
- Future validation, if any, should apply only to the small discovery file shape, not to human-authored Markdown project memory.
- YAIML is for AI chats as well as coding agents; repository memory should survive provider changes, chat resets, agent handoffs, and contributor handoffs.
- YAIML supports multi-agent and multi-contributor projects; conflicts should preserve evidence and uncertainty rather than being smoothed into false certainty.
- YAIML distinguishes agent instruction files from project memory: instruction files tell agents how to behave; YAIML preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.
- YAIML uses bounded context loading: discovery, core, task-relevant supporting documents, then deep references only when needed.
- YAIML should self-unfold beyond the core family when a project needs durable homes for preferences, legal, contracts or agreements, concepts, terms, risk review, security, data, testing, UX, domain, deployment, release, operations, product doctrine, world or lore, provider integration, remote access, or other project-specific guidance.
- YAIML documents should usually be versioned with the source code; initialization should not add them to `.gitignore` by default.
- YAIML-using projects should remain portable and shareable with their intended audience when their YAIML documents are maintained as repository-safe project memory: sanitized evidence, no secrets, no private transcripts, no raw sensitive logs, and no invented legal/security/privacy/ownership conclusions.
- YAIML documents should be ordinary visible Markdown by default, not a custom `.yaiml` extension, hidden folder, cache, or tool-state format.
- YAIML should keep near-zero dependency burden for adopters. Current adoption should not require a CLI, package, SDK, parser, validator for Markdown memory documents, MCP server, framework adapter, or hosted service.
- Machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, and private workspace URLs should not be committed into YAIML documents. YAIML reference locations for "update YAIML" are per-workspace/per-agent context unless a stable team-approved source exists.
- YAIML documents must not store raw secrets, credentials, tokens, private keys, passwords, customer personal data, private chat transcripts, or sensitive raw values.
- AI-generated legal, licensing, ownership, copyright, trademark, patent, contract, or IP statements require caution. Preserve human-approved statements and uncertainty; do not invent rights claims.
- Every YAIML document starts with a short stable header.
- Human intent and implementation evidence must remain separate.
- Ambiguity must be visible when it can affect future work.
- Pruning is part of the method, especially for SoT.
- SoT templates should include a small recent-verified-checks surface when useful, but it must be replaced after newer verification rather than appended forever.
- Tooling is deferred.
- A future init helper may improve on the one-time init flow, but YAIML should remain plain project-local files, not a package-manager dependency, runtime library, hosted platform, or build step.
- Every proposed addition should answer: does this improve a new AI chat, coding agent, or contributor's ability to reconstruct the project's current engineering understanding?
- The repository is public for visibility, review, and use under the MIT License. The intended audience is broad, including anyone working with AI chats or agents on software projects.

## Meaningful Accomplishments

- The repository has been realigned away from schema/conformance/spec framing and toward a convention-first AI Project Engineering framework.
- The core document family is centered on SoT, with project-specific Markdown filenames such as `SoTY.md`, `SoTT.md`, or `SoTC.md`.
- Stable headers now act as agent-facing orientation instead of rigid document contracts.
- The README now uses a more human-facing front door, while guides, templates, prompts, and the fictional example carry the deeper YAIML project-memory doctrine.
- Obsolete legacy-name migration language has been removed because current known adopters are local and already updated; new readers should encounter YAIML directly.
- The discovery-file examples now use the nested `yaiml.version` / `core` / `supporting` shape instead of the older flat marker shape.
- The repository now uses the MIT License, preserving Jeff Wirsing's copyright ownership while allowing public use, copying, modification, distribution, sublicensing, and sale under the license terms.
- `prompts/init-yaiml.md` provides the small adoption path; `prompts/initialize-yaiml.md` remains the full self-contained initialization prompt for deeper repository setup.
- Live init trials clarified that sanitized command outcomes should be recorded inside generated YAIML documents, not only in final chat output.
- `docs/AGENT_INTEGRATION.md` clarifies the boundary between agent behavior instructions and YAIML project memory.
- `docs/CONTEXT_LOADING.md` prevents self-unfolding from becoming read-everything-by-default context loading.
- `docs/EVALUATION.md` adds a real-project evidence path without inventing adoption or performance proof.
- The supporting template set uses `templates/supporting/` to avoid implying supporting documents are decorative extras.
- Supporting guidance now protects the plain-file boundary: visible Markdown, versioned by default, no `.yaiml` extension, no hidden tool-state folder, no package dependency.
- Supporting guidance now protects memory hygiene: no secrets, private chat transcripts, sensitive raw values, raw sensitive command output, or agent-invented legal/IP/security/compliance conclusions.
- Declared supporting YAIML guides now have stable headers, matching the repository's own stable-header rule.
- A public security/sensitive-information policy now tells contributors not to place secrets, personal data, exploit details, or confidential project information into public YAIML materials.
- Cold-start review now covers repository portability, provider/machine/contributor handoff, and repository-safe memory hygiene as YAIML 0.2 readiness concerns.
- SpriteWrite field feedback reported that `AGENTS.md` -> `yaiml.yml` -> stable-headered core docs preserved project memory through ordinary coding work; this is useful field signal, not controlled proof.

## Current Strengths

- A developer can use YAIML today with ordinary Markdown files; prompts are optional helpers for setup, repair, audit, pruning, and realignment.
- The central SoT role is distinct from Architecture and Maintainer Guide.
- The front door now presents YAIML as a one-time init plus repository-carried project memory, not a sequence of repeated pasted prompts.
- The intended day-to-day interaction can be natural human language such as "continue through the SoT priorities" or "update our SoT" because the repository already holds the guiding context.
- The concept now explicitly covers shared AI-chat, multi-agent, and multi-contributor continuity rather than only a single recurring coding-agent relationship.
- The init prompts now update existing agent instruction files with a concise YAIML pointer when such files exist, helping the repository guide future AI chats and agents without repeated prompt choreography.
- `prompts/update-yaiml.md` gives adopters a thin natural-language path for "update YAIML" when the YAIML reference changes, without turning YAIML into a package, CLI, dependency, or schema migration.
- Initial YAIML setup now teaches phrases such as "updated YAIML" and "check new YAIML" through the generated Maintainer Guide and existing agent instruction files when present, while keeping machine-specific YAIML reference paths out of committed project memory.
- The self-unfolding document model can adapt to project domains without requiring every project to use every document.
- The context-loading model keeps the core family bounded and makes supporting documents task-relevant rather than automatically loaded.
- Authority and evidence guidance clearly separates human intent from implementation reality.
- Pruning guidance directly addresses append-only state bloat.
- The no-dependency/no-custom-format boundary is visible in the README, Architecture, Roadmap, and initialization prompt.
- The `yaiml.yml` discovery protocol is now explicitly small and path-oriented, with validation deferred to that file only if validation is ever added.
- Init, update, and audit prompts now consistently warn against private chat transcripts and raw sensitive logs in versioned YAIML memory.
- The repository now has a lightweight method for collecting real-project case studies and cold-start comparison evidence.
- Read-only local adoption sampling found YAIML-shaped project memory in four nearby repositories, giving modest evidence that the convention can exist across varied project shapes.
- The same local sampling found hardcoded machine-specific reference paths in early adopter discovery files, confirming that convention-refresh cleanup and portable-reference guidance remain YAIML 0.2 readiness concerns.
- A follow-up local adopter cleanup removed hardcoded YAIML checkout paths from several nearby YAIML-adopting repositories and replaced stale agent/maintainer wording with run-time reference guidance, confirming that the portable-reference rule can be applied without changing project-specific memory.
- The repository dogfoods its own framework.
- Early SpriteWrite use supports the small-discoverable-role-separated shape: SoT for current truth, Architecture for durable boundaries, Maintainer Guide for procedures, and supporting docs for product-specific direction.

## Current Weaknesses

- The framework has one robust fictional example and a small read-only local adoption sample, but it still needs controlled adoption trials on real repositories.
- The SoT naming posture now favors `SOT.md` as the boring default while preserving project-specific names; this still needs validation with first-time readers.
- The manifest is useful for discovery, but it is not yet proven whether it should be required for all adopters.
- The prompt pack has not yet been exercised enough to know which instructions agents routinely miss; the minimum and full initialization prompts both need broader real-world validation.
- The context-loading guide is conceptually clear but untested under real context-window pressure.
- The case-study and cold-start evaluation method is only a proposed evidence path until used on real repositories.
- The future init-helper shape is intentionally undefined; it needs to reduce manual prompt handling without becoming a package dependency or platform.
- The supporting template set must be kept useful without implying every possible memory domain deserves a starter file.
- The README still needs pressure toward human adoption clarity rather than internal framework explanation.
- The prompt library can easily read like a required operating checklist; it should remain framed as fallback and maintenance help for cases where the repository's own YAIML guidance is not enough.
- Field feedback suggests agents benefit from explicit instruction to update only affected YAIML documents after material changes and prune stale state; guidance should keep that behavior visible without making updates ceremonial.
- The init prompts still need more real-repository trials to confirm they add agent-instruction pointers cleanly without overwriting local guidance.
- The YAIML refresh prompt and init-time maintenance note need real trials across existing YAIML-adopting projects to confirm agents remove committed local reference paths while preserving local memory.
- Adopter cleanup still needs validation outside this local workspace before the guidance can be treated as broadly proven.

## Active Risks

- Formalization drift: future changes could recreate schemas for Markdown memory, conformance fixtures, normative spec language, package formats, or custom file extensions too early.
- Standards-track drift: external adoption advice could push YAIML toward a separate formal spec repo, JSON Schema or JSON-LD as the center of project memory, validators for Markdown documents, SDKs, MCP or framework adapters, RFC machinery, or standards-body governance before the plain-file memory pattern is proven.
- Tooling drift: a future init helper could become a dependency, runtime, hosted platform, or build step instead of serving project-local Markdown files.
- Ceremony drift: self-unfolding documents could become empty files if agents create every possible supporting role instead of only what the project needs.
- Context drift: agents could treat `yaiml.yml` as a command to load every document on every task, making YAIML too heavy for routine work.
- Safety drift: public or shared repositories could expose sensitive information if agents treat YAIML as private scratch space instead of sanitized project memory.
- Shareability drift: adopters could assume YAIML should be hidden or gitignored instead of learning to keep versioned project memory safe enough to travel with the repository across machines, contributors, and AI chat providers.
- Output drift: init or audit prompts could encourage agents to paste raw command output, logs, screenshots, or chat transcripts into versioned memory instead of recording sanitized evidence and outcomes.
- Collaboration drift: multiple agents or contributors could overwrite, flatten, or silently contradict each other's project-memory updates instead of preserving evidence and disagreement until resolved.
- Workspace drift: agents could commit machine-specific YAIML reference paths or local workspace URIs, making the repo less portable and exposing local machine details.
- Reporting drift: public issues or examples could include sensitive security details if the top-level security policy is missed or ignored.
- Reporting-channel gap: `SECURITY.md` avoids public sensitive details, but YAIML 0.2 readiness still needs a human-approved private reporting path or an explicit decision to rely on GitHub private vulnerability reporting.
- Advice drift: legal, security, compliance, privacy, licensing, or IP memory could be mistaken for professional recommendations if templates do not keep their memory-only role clear.
- Status-report drift: SoT could be misread as a status report instead of an engineering-state synthesis.
- Prompt drift: the prompt pack needs real use on varied repositories before its wording can be considered stable.
- Prompt-library drift: the README or guides could imply humans must paste separate prompts after every step, undermining YAIML's goal of repository-carried guidance.
- Integration drift: initialization could fail to connect YAIML to existing agent instruction files, leaving future sessions dependent on the human remembering to say "read YAIML."
- Refresh drift: "update YAIML" could be misread as permission to overwrite project memory instead of refreshing convention scaffolding from a known reference.
- Terminology drift: YAIML could accumulate too many named concepts and become harder to explain than the problem it solves.
- Evidence drift: the fictional example could be mistaken for proof if real case studies are not gathered and labeled honestly.

## Immediate Priorities

1. Continue trialing `init-yaiml.md`, `initialize-yaiml.md`, and `update-yaiml.md` on unrelated real repositories and record where agents misunderstand the concept.
2. Apply the cold-start evaluation method to real projects without overclaiming results.
3. Test whether agents choose useful self-unfolded supporting documents without creating empty ceremony, using the "several concrete recurring pieces of knowledge" heuristic.
4. Test whether the context-loading model keeps routine tasks bounded while still surfacing task-relevant supporting memory.
5. Test whether agents keep YAIML versioned by default while sanitizing secrets, sensitive data, local reference paths, and legal/IP/security/compliance claims.
6. Explore a better init-helper shape while preserving the plain-file, no-dependency boundary.
7. Keep the fictional example detailed enough to teach the pattern without implying it is proof.
8. Refine pruning behavior from actual overgrown SoT documents.
9. Prepare public-release readiness criteria, including contribution expectations, evidence requirements, release labeling, and clear MIT license communication.
10. Decide the YAIML 0.2 sensitive-reporting path.
11. Preserve YAIML's own dogfood documents after material changes.

## Known Divergence

No active divergence currently identified in the repository's declared concept versus current artifact shape.

Resolved: an earlier version centered on `SPEC.md`, schemas, conformance fixtures, and formal standard language. That material was removed during the foundational realignment.

Resolved: later refinements clarified stable headers, SoT naming, self-unfolding supporting documents, versioned-by-default memory, ordinary Markdown files, safety/legal/IP hygiene, bounded context loading, init versus full initialization, evaluation evidence paths, prompt-library fallback framing, and the no-dependency init-helper boundary.

## Rejected Framings

- YAIML is not primarily a YAML format.
- YAIML is not a parser or validation target first.
- YAIML is not a generic memory database.
- YAIML is not durable storage, an orchestration framework, a background service, or an autonomous coding agent.
- YAIML is not a replacement for source code, tests, Git history, issues, or `AGENTS.md`.
- YAIML is not a custom document file extension.
- YAIML is not proof of agent productivity by itself.
- YAIML is not a finished software platform.
- YAIML is not currently a formal standards-body program, validator ecosystem, SDK family, MCP integration, or framework adapter layer.

## Future Possibilities

Possible later tooling includes repository initialization, document discovery, freshness checks, document health reviews, pruning assistance, context assembly, IDE integration, and coding-agent adapters. These should serve the framework after the Markdown workflow proves itself, and should preserve project-local YAIML files as the source of truth.

## Open Questions

- How strongly should YAIML enforce project-specific SoT filenames such as `SoTY.md`, `SoTT.md`, or `SoTC.md`?
- Is `yaiml.yml` essential for the no-tooling phase, or should it be recommended but optional?
- How strict should future tooling be without damaging the interpretive value of YAIML?
- Which self-unfolded document roles are common enough to deserve first-class templates?
- What is the smallest useful init helper, if tooling becomes appropriate, that reduces manual prompt handling without becoming a dependency or platform?
- What evidence threshold is enough to describe YAIML as a reusable standard rather than an early public convention?
