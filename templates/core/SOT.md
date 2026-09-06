---
yaiml: 0.2
role: sot
title: SOT
purpose: Current engineering state and direction for the project.
belongs-here: goals, developer asks, current capabilities, risks, testing and verification state, priorities, divergence, useful recent lessons.
not-here: durable architecture, command reference, complete history.
durability: volatile; synthesize and prune aggressively.
read-with: Architecture; Maintainer Guide.
update-when: direction, verified reality, risks, priorities, or useful engineering lessons change.
agent-guidance: Verify implementation claims. Preserve human intent. Mark uncertainty. Surface conflicts. Prune stale detail.
---

# SOT

SoT means State Of The. `SOT.md` is the recommended default filename for unfamiliar repositories. A project may rename the file to a project-specific SoT name when that adds useful project character, such as `SoTP.md`, `SoTC.md`, or `SoTT.md`.

## North Star

Declared: Unknown until project inspection or human direction.

## Authority And Review

- Maintainer or owner:
- Last meaningful review:
- Higher-authority sources:
- Review path for material changes:

In shared or governed repositories, approved decisions, current maintainers, owners, and documented repository rules outweigh stale notes, stray comments, and agent inference.

## Current Engineering State

Record what is verified now. Do not describe planned behavior as implemented behavior.

## Product Or System Identity

- Verified:
- Declared:
- Unknown:

## Developer Direction

Record current human asks, product rules, accepted decisions, and corrected directions. Do not rewrite this to match accidental implementation.

## Current Capabilities

Summarize meaningful accomplishments as current capability, not as a chronological work log.

## Active Risks And Debt

Keep this list current. Include audit findings only while they still affect current work. Remove resolved risks.

## Testing And Verification State

Summarize what has been verified, what checks are trusted, and what remains untested or uncertain.

## Recent Verification

Keep a short replaceable summary of the latest trusted checks. Separate checks that passed from commands or tests that merely exist. Replace this section after newer verification; do not append forever.

## Useful Recent Lessons

Capture lessons that should change future work. Avoid preserving routine run history.

## Known Divergence

Record disagreement between declared intent, architecture, documentation, code, tests, or runtime behavior.

## Immediate Priorities

Keep this short. Name the next few useful moves without turning this into a full backlog.

## Open Questions

List questions that shape near-term work or human decisions.
