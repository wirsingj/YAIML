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

SoT means State Of The. Use `SOT.md` by default or preserve an established project-specific name.

Adapt these headings to the project. Remove empty or irrelevant sections; retain unknowns that affect decisions. Replace an existing account when facts change; do not append a session summary or repeat the fact under several headings.

## Purpose And Direction

Record project identity, current human asks, accepted decisions, and corrected directions. Name decision sources or owners where relevant. Keep declared intent separate from implementation.

## Current State And Capabilities

Summarize verified behavior with consequential evidence references. Describe completed work as current capability, not a chronological log. Mark inferred or unknown areas.

## Active Risks And Divergence

Record unresolved risks, debt, and conflicts among direction, design, code, tests, or contributor accounts. Remove resolved active items; preserve accepted risks with their decision source.

## Verification

Keep a short replaceable summary of consequential checks and gaps. Separate successful execution from source-defined checks. For prior results, preserve relevant date, revision, environment, and limits. A newer edit does not revalidate a claim.

## Immediate Priorities And Open Questions

Name the next few useful actions and questions that shape them. Link a larger backlog if one exists.

## Useful Lessons

Keep a lesson only if it names a condition and changes a future action. Preserve still-relevant decisions and rejected approaches worth preventing. Let Git retain routine run history.
