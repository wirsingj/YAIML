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

Date: 2026-09-05

## Scenario

An unfamiliar AI chat or coding agent enters the repository with no prior YAIML context and reads:

1. `yaiml.yml`
2. `docs/SoTY.md`
3. `docs/ARCHITECTURE.md`
4. `docs/MAINTAINER_GUIDE.md`
5. `AGENTS.md`
6. `README.md`
7. `docs/AGENT_INTEGRATION.md`, `docs/CONTEXT_LOADING.md`, and `docs/EVALUATION.md`
8. `docs/ADOPTION_AND_UPGRADES.md` and `docs/case-studies/YTMMOCC.md`
9. `CONTRIBUTING.md`, `SECURITY.md`, `AI_USAGE.md`, and `ROADMAP.md`
10. Core templates, supporting templates, and prompt pack
11. `examples/minimal-notes/` and `examples/canopy-dispatch/`

## Result

Manual inspection found guidance for the intended adoption path. Fresh-session success has not been established.

The repository explains YAIML, Yet Another AI Markup Language, as an early public plain-file convention for AI Project Engineering: project management, memory, definition, and AI-chat, agent, and contributor continuity. SoT is clearly the central artifact, with Architecture and Maintainer Guide as supporting default roles. The stable header is described as semantic guidance for future AI sessions rather than a parser-oriented format. The README now leads with practical value, a compact file example, and a copy/paste try-it path. The single init prompt carries embedded YAIML context for use outside this repository and now distinguishes source-defined commands from successful command execution.

The current front door also explains that YAIML portability is independent of an adopting project's business or licensing model. A project may be private, public, paid, free, open-source, or unreleased; YAIML should travel with that repository across machines, contributors, and AI chat provider instances when maintained as repository-safe project memory.

This review is a manual walkthrough, not an independent fresh-session trial.

## Inspected Guidance

- README and init prompt describe the three core roles, `SOT.md` default, optional local names, and supporting documents only when justified.
- Init embeds adoption instructions; refresh preserves mature memory and existing discovery layouts unless migration is explicitly requested and compatibility is established.
- Context-loading guidance selects task-relevant supporting documents. Portability guidance keeps memory versioned and excludes machine-specific reference paths and sensitive material.
- Evidence and compression guidance separates declared direction, inspected definitions, execution outcomes, and unknowns. The worked examples now preserve missing rationale and verification gaps.
- Evaluation distinguishes fictional examples, maintainer-owned YTMMOCC evidence, and independent trials. The case study links public source at an inspected revision.

These are observations about the supplied instructions, not measured evidence that an unfamiliar session will follow them correctly.

## Remaining Risks

- The example is fictional, so it should be checked for plausibility, specificity, and accidental drift into generic filler.
- Future tooling boundaries remain intentionally deferred and should not dominate near-term edits.
- The expanded initialization prompt still needs real-world trials to prove it is detailed enough without becoming too long for routine use.
- Self-unfolding document guidance needs real-world trials to prove agents add the right documents instead of adding too many.
- `CONTRIBUTING.md` and `ROADMAP.md` are now checked because they can preserve stale licensing or tooling assumptions outside the YAIML manifest.
- Memory hygiene guidance needs real-world trials to prove agents sanitize sensitive evidence while preserving enough actionable risk context.
- Repository-portability guidance needs real-world trials to prove generated YAIML remains useful across machines, contributors, and AI chat providers without becoming private scratch memory.
- YAIML 0.2 still needs a human-approved sensitive-reporting path or an explicit decision to rely on GitHub private vulnerability reporting.
- YAIML convention refresh needs real-world trials to prove agents can update local prompts/templates/guidance while preserving project-specific memory.
- The cold-start evaluation method itself needs real use before its dimensions can be considered reliable.
- Discovery compatibility guidance needs trials on mature adopters before migrations are recommended as routine.

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
