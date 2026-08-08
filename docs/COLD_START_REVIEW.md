---
yaiml: 0.2
role: review
title: Cold Start Review
purpose: Manual review notes for whether an unfamiliar AI chat or coding agent can understand and use YAIML from this repository alone.
belongs-here: cold-start findings, repository usability checks, gaps that affect first-time AI-session understanding.
not-here: permanent architecture, command reference, implementation promises.
durability: current review note; replace after major repository shifts.
read-with: SoTY; Architecture; Maintainer Guide.
update-when: a major conceptual or structural revision changes the first-time user path.
agent-guidance: Treat this as review evidence, not a normative source. Verify current files before relying on it.
---

# Cold Start Review

Date: 2026-07-11

## Scenario

An unfamiliar AI chat or coding agent enters the repository with no prior YAIML context and reads:

1. `yaiml.yml`
2. `docs/SoTY.md`
3. `docs/ARCHITECTURE.md`
4. `docs/MAINTAINER_GUIDE.md`
5. `AGENTS.md`
6. `README.md`
7. `docs/AGENT_INTEGRATION.md`, `docs/CONTEXT_LOADING.md`, and `docs/EVALUATION.md`
8. `CONTRIBUTING.md`, `SECURITY.md`, and `ROADMAP.md`
9. Core templates, supporting templates, and prompt pack
10. `examples/canopy-dispatch/`

## Result

Pass with open risks after the front-door, minimal-initialization, context-loading, repository-portability, and evaluation refinement passes.

The repository explains YAIML as an early public plain-file convention for AI Project Engineering: project management, memory, definition, and AI-chat, agent, and contributor continuity. SoT is clearly the central artifact, with Architecture and Maintainer Guide as supporting default roles. The stable header is described as semantic guidance for future AI sessions rather than a parser-oriented format. The README now leads with a copy/paste try-it path before showing the file list, and the full initialization prompt still carries embedded YAIML context for use outside this repository. The prompt library distinguishes project-memory updates from YAIML convention refreshes.

The current front door also explains that YAIML portability is independent of an adopting project's business or licensing model. A project may be private, public, paid, free, open-source, or unreleased; YAIML should travel with that repository across machines, contributors, and AI chat provider instances when maintained as repository-safe project memory.

## Checks

- A new AI session can identify SoT, Architecture, and Maintainer Guide as the default YAIML family.
- A new AI session can identify that YAIML self-unfolds into project-specific supporting documents such as Preferences, Legal, Contracts, Concepts, Terms, Risk Review, Security, Testing, Product Doctrine, World or Lore, Remote Access, and more as needed.
- A new AI session can see supporting templates for several high-leverage self-unfolded roles without being told to create every role by default.
- A new AI session can identify `SOT.md` as the recommended default filename and project-specific names such as `SoTY.md` or `SoTT.md` as optional project character.
- A new AI session can follow the read, execute, update lifecycle from the README and prompts.
- A new AI session can choose `prompts/init-yaiml.md` for a small trial or `prompts/full-init-yaiml.md` for a deeper repository initialization.
- A new AI session can identify `prompts/update-yaiml.md` as the workflow for refreshing local YAIML scaffolding from a human-provided or workspace-local reference without overwriting project memory.
- A new AI session can paste `prompts/full-init-yaiml.md` into another repository without also needing this repository's support docs open.
- A new AI session can see that initial YAIML setup should teach "update YAIML" / "check new YAIML" through Maintainer Guide and the repository's agent-instruction surface, without committing machine-specific reference paths.
- A new AI session can identify the context-loading layers and avoid reading unrelated supporting documents for a narrow task.
- A new AI session can identify that Canopy Dispatch is an example, not proof, and that real case studies should use `docs/EVALUATION.md`.
- A new AI session can identify that YAIML documents are intended to be versioned with source code by default, not added to `.gitignore` automatically.
- A new AI session can identify that YAIML should travel with the repository across machines, contributors, and AI chat provider instances.
- A new AI session can identify that YAIML must not store raw secrets, sensitive personal data, private chat transcripts, raw sensitive logs, or AI-invented legal/IP conclusions.
- The stable header can be understood without a parser.
- Declared YAIML documents, including supporting guides, now begin with stable headers.
- Evidence, uncertainty, human intent, and implementation reality are described separately.
- Pruning guidance says to synthesize SoT instead of appending forever.
- The Canopy Dispatch example demonstrates a fictional project where SoT carries product doctrine, trust risks, verified evidence, architecture boundaries, maintainer playbooks, and active engineering priorities.

## Remaining Risks

- The example is fictional, so it should be checked for plausibility, specificity, and accidental drift into generic filler.
- Future tooling boundaries remain intentionally deferred and should not dominate near-term edits.
- The exact long-term strictness of project-specific SoT filenames versus the boring `SOT.md` default remains a founder/tooling decision.
- The expanded initialization prompt still needs real-world trials to prove it is detailed enough without becoming too long for routine use.
- Self-unfolding document guidance needs real-world trials to prove agents add the right documents instead of adding too many.
- `CONTRIBUTING.md` and `ROADMAP.md` are now checked because they can preserve stale licensing or tooling assumptions outside the YAIML manifest.
- Memory hygiene guidance needs real-world trials to prove agents sanitize sensitive evidence while preserving enough actionable risk context.
- Repository-portability guidance needs real-world trials to prove generated YAIML remains useful across machines, contributors, and AI chat providers without becoming private scratch memory.
- YAIML 0.2 still needs a human-approved sensitive-reporting path or an explicit decision to rely on GitHub private vulnerability reporting.
- YAIML convention refresh needs real-world trials to prove agents can update local prompts/templates/guidance while preserving project-specific memory.
- The cold-start evaluation method itself needs real use before its dimensions can be considered reliable.

## Local Adoption Sampling

Date: 2026-07-11

Scope: read-only inspection of four nearby local repositories that already contain YAIML-shaped project memory. This was not a controlled cold-start comparison and should not be treated as proof of effectiveness.

Observed:

- Three inspected adopters have a discoverable `yaiml.yml` and a recognizable SoT/Architecture/Maintainer Guide family.
- One older adopter has a looser YAIML shape: `yaiml.yml` points to a core document family and supporting project-memory files, but its SoT naming and supporting map predate the current boring-default guidance.
- The local adopters preserve useful project-specific memory rather than only copying generic templates.
- All four inspected local adopters contain a machine-specific YAIML reference path in `yaiml.yml`. That confirms the current no-hardcoded-local-reference guidance and `prompts/update-yaiml.md` are needed cleanup paths, not theoretical polish.
- Several adopter maintenance notes still say to use the "known YAIML reference in `yaiml.yml`." Future refresh trials should verify that agents remove those committed local paths and keep reference locations in human/workspace context instead.

Lesson:

YAIML initialization can produce useful repo-carried memory in varied projects, but adopter cleanup still needs validation outside this local workspace before examples or claims imply the portability rule has always been satisfied.
