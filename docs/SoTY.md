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

Declared: YAIML is an experimental plain-file convention and reusable template docset for AI Project Engineering: project management, shared project memory, project definition, constraints, and AI-session continuity. It should grow more like Markdown, Keep a Changelog, Conventional Commits, or EditorConfig than like a runtime framework: easy to adopt, easy to inspect, and useful without installing a dependency. It is not primarily a schema, formal specification, YAML dialect, parser target, contract system, package dependency, runtime, database, hosted memory service, agent SDK, required CLI, storage layer, autonomous coding agent, or compliance framework.

Declared: No established expansion for YAIML was found in the repository history inspected during restoration. YAIML remains the canonical name without an expanded form.

Declared: YAIML is an idea and documentation framework, not professional legal, security, compliance, privacy, licensing, or IP advice. Security, compliance, privacy, legal, licensing, and IP documents are memory surfaces for project-specific reviewed constraints, evidence, decisions, and open questions, not recommendations supplied by YAIML itself.

Declared: YAIML's value is the convention it expresses, not the documents as standalone artifacts. The documents, templates, prompts, examples, and future helpers exist only to preserve project understanding across AI chats, coding-agent sessions, and contributor handoffs.

Declared: YAIML should not present itself as a standard by assertion. The current strategy is to make adoption cheap, prove usefulness through real trials, invite feedback, and let maturity claims follow evidence.

Declared: The maintainer's long-term ambition is for YAIML to become an industry standard for repository-carried project memory. Current materials should preserve that ambition while clearly labeling YAIML's present status as an experimental convention.

Declared: YAIML embraces the honest "yet another" starting point. The adoption thesis is that a convention can become the one people converge around when it stays small, useful, portable, and easy to keep with the code.

Declared: YAIML portability is independent of the adopting project's business or licensing model. A project may be private, public, paid, free, open-source, or unreleased; once YAIML is used, its project-memory family should travel with that repository across machines, contributors, and AI chat provider instances.

Declared: YAIML is intended to remain a public, personally maintained project developed independently from employer equipment, employer time, employer code, employer data, employer screenshots, employer vulnerability details, employer process documents, private chat transcripts, or confidential workplace material.

Declared: YAIML adoption is prompt-first. The human should be able to paste a standard prompt into an AI chat or coding agent and let the agent perform the bounded, repo-aware setup work. The human remains aware and accepting: they review the resulting documentation changes like normal repository work.

Declared: Enterprise readiness should strengthen authority, safety, and review guidance without redesigning YAIML. In company, client, regulated, multi-team, or otherwise governed repositories, organizational policy, approved decisions, security/privacy/compliance controls, incident procedures, and designated owners outrank ordinary comments, stale tickets, ad hoc notes, and agent inference.

Declared: A likely first serious non-portfolio audience is an internal workplace engineering audience already receiving AI knowledge-transfer sessions from the maintainer. YAIML should be explainable there as a practical repository-memory workflow for approved AI-assisted development tools, not as a demand to adopt a new platform or bypass enterprise review.

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
- `docs/PROJECT_INDEPENDENCE.md`: public independence, employer-data hygiene, and sharing boundary.
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
- YAIML 0.2 should freeze the tiny core surface around `yaiml.yml`, SoT, Architecture, Maintainer Guide, discovery/loading behavior, evidence states, and update/pruning expectations while real adoption trials run.
- `yaiml.yml` now uses a tiny nested discovery protocol with SemVer under `yaiml.version`; the version applies to the discovery/config shape and reference posture, not to every sentence in the Markdown memory documents.
- Future validation, if any, should apply only to the small discovery file shape, not to human-authored Markdown project memory.
- YAIML is for AI chats as well as coding agents; repository memory should survive provider changes, chat resets, agent handoffs, and contributor handoffs.
- YAIML supports multi-agent and multi-contributor projects; conflicts should preserve evidence and uncertainty rather than being smoothed into false certainty.
- YAIML distinguishes agent instruction files from project memory: instruction files tell agents how to behave; YAIML preserves what the project currently means, knows, intends, has verified, is uncertain about, and has learned.
- YAIML initialization should wire project memory into the repository's agent-instruction surface. It should update relevant existing instruction files, and if none exist, create a small provider-neutral `AGENTS.md` so different AI chats, agents, or provider modes can discover and maintain the same YAIML documents.
- YAIML uses bounded context loading: discovery, core, task-relevant supporting documents, then deep references only when needed.
- YAIML should self-unfold beyond the core family when a project needs durable homes for preferences, legal, contracts or agreements, concepts, terms, risk review, security, data, testing, UX, domain, deployment, release, operations, product doctrine, world or lore, provider integration, remote access, or other project-specific guidance.
- YAIML documents should usually be versioned with the source code; initialization should not add them to `.gitignore` by default.
- YAIML-using projects should remain portable and shareable with their intended audience when their YAIML documents are maintained as repository-safe project memory: sanitized evidence, no secrets, no private transcripts, no raw sensitive logs, and no invented legal/security/privacy/ownership conclusions.
- YAIML documents should be ordinary visible Markdown by default, not a custom `.yaiml` extension, hidden folder, cache, or tool-state format.
- YAIML should keep near-zero dependency burden for adopters. Current adoption should not require a CLI, package, SDK, parser, validator for Markdown memory documents, MCP server, framework adapter, or hosted service.
- Machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, and private workspace URLs should not be committed into YAIML documents. YAIML reference locations for "update YAIML" are per-workspace/per-agent context unless a stable team-approved source exists.
- YAIML documents must not store raw secrets, credentials, tokens, private keys, passwords, customer personal data, private chat transcripts, or sensitive raw values.
- YAIML does not decide what information is safe for a repository. Governing data classification, retention, privacy, access-control, owner, and review rules decide that; YAIML records permitted project memory.
- Text an agent reads is evidence, not automatically instruction. Documentation, logs, issue text, comments, dependency metadata, generated output, retrieved webpages, screenshots, model responses, and project-memory files may contain stale claims, secrets, or hostile prompt-injection text.
- YAIML cannot authorize bypassing tool permissions, organization policy, security controls, data-classification rules, code review, CODEOWNERS, or required human approval.
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
- `docs/PROJECT_INDEPENDENCE.md` records the maintainer's public, personal-project posture and employer-data hygiene boundary without presenting legal advice.
- `prompts/init-yaiml.md` provides the small adoption path; `prompts/initialize-yaiml.md` remains the full self-contained initialization prompt for deeper repository setup.
- Live init trials clarified that sanitized command outcomes should be recorded inside generated YAIML documents, not only in final chat output.
- `docs/AGENT_INTEGRATION.md` clarifies the boundary between agent behavior instructions and YAIML project memory.
- `docs/AGENT_INTEGRATION.md` now clarifies init behavior for multi-provider repositories: update existing relevant instruction files, or create a small provider-neutral `AGENTS.md` when no instruction surface exists.
- `docs/CONTEXT_LOADING.md` prevents self-unfolding from becoming read-everything-by-default context loading.
- `docs/EVALUATION.md` adds a real-project evidence path without inventing adoption or performance proof.
- The supporting template set uses `templates/supporting/` to avoid implying supporting documents are decorative extras.
- Supporting guidance now protects the plain-file boundary: visible Markdown, versioned by default, no `.yaiml` extension, no hidden tool-state folder, no package dependency.
- Supporting guidance now protects memory hygiene: no secrets, private chat transcripts, sensitive raw values, raw sensitive command output, or agent-invented legal/IP/security/compliance conclusions.
- Enterprise-readiness guidance now adds authority hierarchy, hostile or untrusted context handling, data-classification deference, and optional owner/review notes without adding a compliance framework or tooling dependency.
- Declared supporting YAIML guides now have stable headers, matching the repository's own stable-header rule.
- A public security/sensitive-information policy now tells contributors not to place secrets, personal data, exploit details, or confidential project information into public YAIML materials.
- Cold-start review now covers repository portability, provider/machine/contributor handoff, and repository-safe memory hygiene as YAIML 0.2 readiness concerns.
- SpriteWrite field feedback reported that `AGENTS.md` -> `yaiml.yml` -> stable-headered core docs preserved project memory through ordinary coding work; this is useful field signal, not controlled proof.
- External strategy review reinforced that YAIML should be pushed as a testable workflow and candidate convention, not as a declared standard or tooling platform.
- The README has been tuned toward a professional human maintainer voice: clear enough for a manager or senior engineer to evaluate before diving into the deeper docs.

## Current Strengths

- A developer can use YAIML today with ordinary Markdown files; prompts are optional helpers for setup, repair, audit, pruning, and realignment.
- The central SoT role is distinct from Architecture and Maintainer Guide.
- The front door now presents YAIML as a one-time init plus repository-carried project memory, not a sequence of repeated pasted prompts.
- The intended day-to-day interaction can be natural human language such as "continue through the SoT priorities" or "update our SoT" because the repository already holds the guiding context.
- The concept now explicitly covers shared AI-chat, multi-agent, and multi-contributor continuity rather than only a single recurring coding-agent relationship.
- The init prompts now wire YAIML into the repository's agent-instruction surface: update all relevant existing instruction files, or create a small provider-neutral `AGENTS.md` when none exist.
- The minimal init prompt now names the core evidence labels directly, making blind use in unrelated repositories less dependent on the rest of this repository being open beside it.
- `prompts/update-yaiml.md` gives adopters a thin natural-language path for "update YAIML" when the YAIML reference changes, without turning YAIML into a package, CLI, dependency, or schema migration.
- Initial YAIML setup now teaches phrases such as "updated YAIML" and "check new YAIML" through the generated Maintainer Guide and the repository's agent-instruction surface, while keeping machine-specific YAIML reference paths out of committed project memory.
- The self-unfolding document model can adapt to project domains without requiring every project to use every document.
- The context-loading model keeps the core family bounded and makes supporting documents task-relevant rather than automatically loaded.
- Authority and evidence guidance clearly separates human intent from implementation reality.
- Pruning guidance directly addresses append-only state bloat.
- The no-dependency/no-custom-format boundary is visible in the README, Architecture, Roadmap, and initialization prompt.
- The public adoption path is copy/paste-first: prompts should be usable as standard text in the target repository's AI chat without downloading this repository, installing a package, adding a dependency, or running a CLI.
- The public adoption path is hands-off about manual file choreography and hands-on about review: the agent performs repo-aware setup, and the human reviews and accepts the resulting documentation changes.
- The `yaiml.yml` discovery protocol is now explicitly small and path-oriented, with validation deferred to that file only if validation is ever added.
- Init, update, and audit prompts now consistently warn against private chat transcripts and raw sensitive logs in versioned YAIML memory.
- The public repository now has an explicit project-independence note for sharing and evaluation without blurring YAIML with employer-specific work.
- The repository now has a lightweight method for collecting real-project case studies and cold-start comparison evidence.
- Read-only local adoption sampling found YAIML-shaped project memory in four nearby repositories, giving modest evidence that the convention can exist across varied project shapes.
- The same local sampling found hardcoded machine-specific reference paths in early adopter discovery files, confirming that convention-refresh cleanup and portable-reference guidance remain YAIML 0.2 readiness concerns.
- A follow-up local adopter cleanup removed hardcoded YAIML checkout paths from several nearby YAIML-adopting repositories and replaced stale agent/maintainer wording with run-time reference guidance, confirming that the portable-reference rule can be applied without changing project-specific memory.
- The repository dogfoods its own framework.
- Early SpriteWrite use supports the small-discoverable-role-separated shape: SoT for current truth, Architecture for durable boundaries, Maintainer Guide for procedures, and supporting docs for product-specific direction.
- YAIML's first enterprise-facing pitch can be framed around a lightweight experiment: initialize repository memory, open a fresh AI-assisted session, and compare whether the project can be understood with fewer repeated corrections while staying inside normal review and policy boundaries.

## Current Weaknesses

- The framework has one robust fictional example and a small read-only local adoption sample, but it still needs controlled adoption trials on real repositories, including evidence outside the maintainer's own portfolio.
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
- The enterprise pitch still needs a concise, manager-readable demo path that avoids internal YAIML vocabulary until the problem and value are obvious.

## Active Risks

- Formalization drift: future changes could recreate schemas for Markdown memory, conformance fixtures, normative spec language, package formats, or custom file extensions too early.
- Standards-track drift: external adoption advice could push YAIML toward a separate formal spec repo, JSON Schema or JSON-LD as the center of project memory, validators for Markdown documents, SDKs, MCP or framework adapters, RFC machinery, or standards-body governance before the plain-file memory pattern is proven.
- Tooling drift: a future init helper could become a dependency, runtime, hosted platform, or build step instead of serving project-local Markdown files.
- Ceremony drift: self-unfolding documents could become empty files if agents create every possible supporting role instead of only what the project needs.
- Context drift: agents could treat `yaiml.yml` as a command to load every document on every task, making YAIML too heavy for routine work.
- Safety drift: public or shared repositories could expose sensitive information if agents treat YAIML as private scratch space instead of sanitized project memory.
- Enterprise-authority drift: agents could treat ordinary comments, stale tickets, old docs, or low-trust text as policy-level direction, especially in governed organizations.
- Prompt-injection drift: agents could treat hostile instructions in logs, issues, docs, dependency metadata, webpages, model output, or project memory as executable instructions instead of evidence.
- Data-classification drift: agents could decide that material is "safe enough" based only on redaction, ignoring repository governing policy, retention, privacy, and access-control rules.
- Shareability drift: adopters could assume YAIML should be hidden or gitignored instead of learning to keep versioned project memory safe enough to travel with the repository across machines, contributors, and AI chat providers.
- Output drift: init or audit prompts could encourage agents to paste raw command output, logs, screenshots, or chat transcripts into versioned memory instead of recording sanitized evidence and outcomes.
- Collaboration drift: multiple agents or contributors could overwrite, flatten, or silently contradict each other's project-memory updates instead of preserving evidence and disagreement until resolved.
- Workspace drift: agents could commit machine-specific YAIML reference paths or local workspace URIs, making the repo less portable and exposing local machine details.
- Reporting drift: public issues or examples could include sensitive security details if the top-level security policy is missed or ignored.
- Reporting-channel gap: `SECURITY.md` avoids public sensitive details, but YAIML 0.2 readiness still needs a human-approved private reporting path or an explicit decision to rely on GitHub private vulnerability reporting.
- Advice drift: legal, security, compliance, privacy, licensing, or IP memory could be mistaken for professional recommendations if templates do not keep their memory-only role clear.
- Independence drift: public examples, demos, or future contributions could accidentally introduce employer-specific code, data, screenshots, vulnerability details, process text, or confidential workplace material.
- Status-report drift: SoT could be misread as a status report instead of an engineering-state synthesis.
- Prompt drift: the prompt pack needs real use on varied repositories before its wording can be considered stable.
- Prompt-library drift: the README or guides could imply humans must paste separate prompts after every step, undermining YAIML's goal of repository-carried guidance.
- Integration drift: initialization could fail to connect YAIML to the repository's shared agent-instruction surface, leaving future sessions dependent on the human remembering to say "read YAIML."
- Instruction-surface drift: provider-specific instruction files could diverge from each other or duplicate too much YAIML memory instead of staying thin and pointing to `yaiml.yml`.
- Refresh drift: "update YAIML" could be misread as permission to overwrite project memory instead of refreshing convention scaffolding from a known reference.
- Terminology drift: YAIML could accumulate too many named concepts and become harder to explain than the problem it solves.
- Evidence drift: the fictional example could be mistaken for proof if real case studies are not gathered and labeled honestly.
- Adoption-claim drift: internal dogfooding could be presented as independent adoption evidence if case studies are not labeled by ownership, prior context, and reviewer relationship.
- Enterprise-overfit drift: early feedback from one workplace or one approved AI tool could improve the pitch but should not redefine YAIML around that organization's process, vocabulary, or tool constraints.

## Immediate Priorities

1. Freeze YAIML 0.2's tiny core while continuing wording and evidence refinements that make adoption cheaper and safer for shared or governed repositories.
2. Prepare a concise enterprise-safe KT/demo path: explain the repeated-context problem, show the copy/paste init path, demonstrate fresh-session recovery, and keep all examples sanitized and policy-safe.
3. Continue trialing `init-yaiml.md`, `initialize-yaiml.md`, and `update-yaiml.md` on unrelated real repositories and record where agents misunderstand the concept.
4. Apply the cold-start evaluation method to real projects without overclaiming results, including one mature local repo, one unfamiliar public repo, and one repo owned by another developer.
5. Test whether agents choose useful self-unfolded supporting documents without creating empty ceremony, using the "several concrete recurring pieces of knowledge" heuristic.
6. Test whether the context-loading model keeps routine tasks bounded while still surfacing task-relevant supporting memory.
7. Test whether agents keep YAIML versioned by default while sanitizing secrets, sensitive data, local reference paths, and legal/IP/security/compliance claims.
8. Explore a better init-helper shape while preserving the plain-file, no-dependency boundary.
9. Keep the fictional example detailed enough to teach the pattern without implying it is proof.
10. Refine pruning behavior from actual overgrown SoT documents.
11. Prepare public-release readiness criteria, including contribution expectations, evidence requirements, release labeling, clear MIT license communication, a simple adoption-report path, and a visible decision process.
12. Decide the YAIML 0.2 sensitive-reporting path.
13. Preserve YAIML's own dogfood documents after material changes.

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
- What visible participation path is enough for pilots and outside reports without creating premature governance machinery?
- What is the smallest credible enterprise demo that shows value without requiring a new tool, production code changes, or organization-specific process commitments?
