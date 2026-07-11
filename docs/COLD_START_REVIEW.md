---
yaiml: 0.1
role: review
title: Cold Start Review
purpose: Manual review notes for whether an unfamiliar coding agent can understand and use YAIML from this repository alone.
belongs-here: cold-start findings, repository usability checks, gaps that affect first-time agent understanding.
not-here: permanent architecture, command reference, implementation promises.
durability: current review note; replace after major repository shifts.
read-with: SoTY; Architecture; Maintainer Guide.
update-when: a major conceptual or structural revision changes the first-time user path.
agent-guidance: Treat this as review evidence, not a normative source. Verify current files before relying on it.
---

# Cold Start Review

Date: 2026-07-01

## Scenario

An unfamiliar coding agent enters the repository with no prior YAIML chat context and reads:

1. `yaiml.yml`
2. `docs/SoTY.md`
3. `docs/ARCHITECTURE.md`
4. `docs/MAINTAINER_GUIDE.md`
5. `README.md`
6. `docs/AGENT_INTEGRATION.md`, `docs/CONTEXT_LOADING.md`, and `docs/EVALUATION.md`
7. `CONTRIBUTING.md` and `ROADMAP.md`
8. Core templates, supporting templates, and prompt pack
9. `examples/canopy-dispatch/`

## Result

Pass with open risks after the front-door, minimal-initialization, context-loading, and evaluation refinement passes.

The repository explains YAIML as an incubating plain-file convention for AI Project Engineering: project management, memory, definition, and agent continuity. SoT is clearly the central artifact, with Architecture and Maintainer Guide as supporting default roles. The stable header is described as semantic guidance for agents rather than a parser-oriented format. The README now leads with a minimum useful setup before the full initialization path, and the full initialization prompt still carries embedded YAIML context for use outside this repository.

## Checks

- A new agent can identify SoT, Architecture, and Maintainer Guide as the default YAIML family.
- A new agent can identify that YAIML self-unfolds into project-specific supporting documents such as Preferences, Legal, Contracts, Concepts, Terms, Risk Review, Security, Testing, Product Doctrine, World or Lore, Remote Access, and more as needed.
- A new agent can see supporting templates for several high-leverage self-unfolded roles without being told to create every role by default.
- A new agent can identify `SOT.md` as the recommended default filename and project-specific names such as `SoTY.md` or `SoTT.md` as optional project character.
- A new agent can follow the read, execute, update lifecycle from the README and prompts.
- A new agent can choose `prompts/init-yaiml.md` for a small trial or `prompts/initialize-yaiml.md` for a deeper repository initialization.
- A new agent can paste `prompts/initialize-yaiml.md` into another repository without also needing this repository's support docs open.
- A new agent can identify the context-loading layers and avoid reading unrelated supporting documents for a narrow task.
- A new agent can identify that Canopy Dispatch is an example, not proof, and that real case studies should use `docs/EVALUATION.md`.
- A new agent can identify that YAIML documents are intended to be versioned with source code by default, not added to `.gitignore` automatically.
- A new agent can identify that YAIML must not store raw secrets, sensitive personal data, or AI-invented legal/IP conclusions.
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
- The cold-start evaluation method itself needs real use before its dimensions can be considered reliable.
