---
yaiml: 0.2
role: sot
title: SOT
purpose: Current engineering state and direction for the project.
belongs-here: goals, developer asks, current capabilities, active work, audit findings, risks, testing state, priorities, divergence, useful recent lessons.
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

## Current Engineering State

Record what is verified now. Do not describe planned behavior as implemented behavior.

## Product Or System Identity

- Verified:
- Declared:
- Unknown:

## Developer Direction

Record current human asks, product rules, accepted decisions, and corrected directions. Do not rewrite this to match accidental implementation.

## Active Work

Record the work currently in motion or most likely to affect the next AI chat, agent session, or contributor handoff.

## Current Capabilities

Summarize meaningful accomplishments as current capability, not as a chronological work log.

## Audit Findings

Record security, architecture, performance, UX, or code-quality findings that still matter.

## Testing State

Summarize what has been verified, what checks are trusted, and what remains untested or uncertain.

## Active Risks And Debt

Keep this list current. Remove resolved risks.

## Known Divergence

Record disagreement between declared intent, architecture, documentation, code, tests, or runtime behavior.

## Evidence And Lessons

Capture audit findings, testing findings, bugs found through use, implementation lessons, and areas needing more inspection.

## Immediate Priorities

Keep this short.

## Next Work

Name the next few useful moves. Avoid turning this into a full backlog.

## Open Questions

List questions that shape near-term work or human decisions.
