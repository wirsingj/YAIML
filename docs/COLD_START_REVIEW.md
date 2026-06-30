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

Date: 2026-06-27

## Scenario

An unfamiliar coding agent enters the repository with no prior YAIML chat context and reads:

1. `yaiml.yml`
2. `docs/SoTY.md`
3. `docs/ARCHITECTURE.md`
4. `docs/MAINTAINER_GUIDE.md`
5. `README.md`
6. Core templates and prompt pack
7. `examples/canopy-dispatch/`

## Result

Pass with open risks after the SoT refinement pass.

The repository explains YAIML as a lightweight standard for AI Project Engineering. SoT is clearly the central artifact, with Architecture and Maintainer Guide as supporting default roles. The stable header is described as semantic guidance for agents rather than a parser-oriented format. The README now gives an agent-first initialization path before the manual setup path and points readers to a robust fictional example.

## Checks

- A new agent can identify SoT, Architecture, and Maintainer Guide as the default YAIML family.
- A new agent can identify `SOT.md` as the neutral starter filename and project-specific names such as `SoTY.md` or `SoTT.md` as preferred real filenames.
- A new agent can follow the read, execute, update lifecycle from the README and prompts.
- The stable header can be understood without a parser.
- Evidence, uncertainty, human intent, and implementation reality are described separately.
- Pruning guidance says to synthesize SoT instead of appending forever.
- The Canopy Dispatch example demonstrates a fictional project where SoT carries product doctrine, trust risks, verified evidence, architecture boundaries, maintainer playbooks, and active engineering priorities.

## Remaining Risks

- The example is fictional, so it should be checked for plausibility, specificity, and accidental drift into generic filler.
- Future tooling boundaries remain intentionally deferred and should not dominate near-term edits.
- The exact long-term strictness of project-specific SoT filenames versus looser discovery remains a founder/tooling decision.
