---
yaiml: 0.1
kind: evaluation-guide
title: Evaluation And Case Studies
purpose: Provide lightweight ways to gather real evidence about YAIML without inventing proof.
belongs-here: real-project case-study template, cold-start comparison method, evaluation dimensions, limitations.
not-here: fabricated metrics, adoption claims, academic benchmark suite, competitive claims against unreviewed tools.
durability: durable but experimental; update when real evaluations reveal better questions.
read-with: SoTY; Cold Start Review; Context Loading.
update-when: case studies are run, evaluation dimensions change, or evidence standards improve.
agent-guidance: Record limitations honestly. Do not turn one small test into universal proof.
---

# Evaluation And Case Studies

The Canopy Dispatch example demonstrates what YAIML can look like, but it is fictional. It is not proof that YAIML improves agent work.

YAIML needs real-project evidence gathered without inflated claims.

## Case Study Template

Use this shape for a real project trial:

```md
# YAIML Case Study: Project Name

## Project And Timeframe

- Project:
- Repository type:
- Dates:
- Agent or tools used:
- Human reviewers:

## Repository Shape

- Main languages and frameworks:
- Project size:
- Existing docs or agent instructions:
- Test/build/deploy shape:

## Before YAIML

- Problems observed before YAIML:
- Repeated agent misunderstandings:
- Missed constraints:
- Stale or scattered project knowledge:

## Documents Introduced

- Core documents:
- Supporting documents:
- Why each supporting document existed:
- Documents considered but not created:

## Evolution

- How the documents changed over time:
- Stale or incorrect memory corrected:
- Resolved risks removed:
- Human corrections preserved:

## Cold-Start Tasks

- Task A:
- Task B:
- Task C:

## Observed Failures

- False claims:
- Missed constraints:
- Reintroduced rejected approaches:
- Architecture misunderstandings:
- Commands or tests missed:
- Human corrections required:

## Useful Work Completed

- Implementation, audit, debugging, design, or documentation work completed:
- Evidence that work respected project constraints:
- Quality of final YAIML update:

## Context Cost

- Documents loaded:
- Supporting documents skipped:
- Approximate time or turns before useful work:
- Any context overload observed:

## Conclusions And Limitations

- What YAIML appeared to help:
- What it did not help:
- Remaining failures:
- Why this case study should not be overgeneralized:
```

## Cold-Start Comparison Method

Use bounded comparisons rather than broad claims.

1. Choose a real repository and a small set of bounded tasks.
2. Prepare ordinary repository instructions for both sessions.
3. Give Agent or Session A the repository and ordinary instructions.
4. Give Agent or Session B the same repository plus YAIML.
5. Give both the same tasks.
6. Compare results without pretending one small test proves universal effectiveness.

Tasks should be small enough to review and specific enough to reveal project understanding.

## Evaluation Dimensions

Track:

- incorrect implementation claims;
- missed project constraints;
- reintroduction of rejected approaches;
- architecture misunderstandings;
- commands or tests missed;
- human corrections required;
- time or turns before useful work;
- quality of the final document update;
- context or token overhead;
- whether stale information was pruned;
- whether uncertainty stayed visible.

## Reporting Discipline

Do not invent:

- user counts;
- adoption claims;
- performance metrics;
- case-study outcomes;
- comparisons against tools that were not tested.

Good evidence can be modest. A useful result might be: "In this one repository, the YAIML-assisted session found a retired architecture approach before editing, while the non-YAIML session reintroduced it." That is evidence to investigate, not a universal claim.
