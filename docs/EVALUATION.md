---
yaiml: 0.2
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

[YTMMOCC](case-studies/YTMMOCC.md) is a real maintainer-owned adoption case. It shows useful repository-carried memory in a published browser-extension project, but it is still internal dogfooding evidence rather than independent proof.

YAIML needs real-project evidence gathered without inflated claims.

A useful evidence set for the public pilot phase should include three distinct case studies:

- one mature repository already known to the maintainer, labeled as internal dogfooding rather than outside proof;
- one unfamiliar public repository initialized without private project context;
- one repository owned by another developer or team.

Internal portfolio repositories can show that YAIML is useful in practice, but they should not be counted as independent adoption evidence.

Keep fictional examples, maintainer-owned field evidence, and independent trials labeled separately.

## Case Study Template

Use this shape for a real project trial:

```md
# YAIML Case Study: Project Name

## Project And Timeframe

- Project:
- Repository type:
- Inspected revision and immutable public source links where accessible:
- Local changes or unpublished evidence, identified separately:
- Dates:
- Agent or tools used:
- Human reviewers:

## Repository Shape

- Main languages and frameworks:
- Project size:
- Existing docs or agent instructions:
- Test/build/deploy shape:
- Public release or listing evidence, if relevant:

## Before YAIML

- Problems observed before yaiml:
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
- Human-reported experience:
- Measured outcomes:

## Context Cost

- Documents loaded:
- Supporting documents skipped:
- Approximate time or turns before useful work:
- Any context overload observed:

## Conclusions And Limitations

- What YAIML appeared to help:
- What it did not help:
- Remaining failures:
- Evidence limits and unverified claims:
- Why this case study should not be overgeneralized:
```

## Cold-Start Comparison Method

Use bounded comparisons rather than broad claims.

1. Choose a real repository and a small set of bounded tasks.
2. Prepare ordinary repository instructions for both sessions.
3. Give Agent or Session A the repository and ordinary instructions.
4. Give Agent or Session B the same repository plus YAIML.
5. Give both the same tasks.
6. Compare results without pretending one small test proves universal effectiveness. Preserve transcripts, summaries, failures, and limitations when safe to share.

Tasks should be small enough to review and specific enough to reveal project understanding.

Useful baselines:

- same repository revision for both sessions;
- same human task wording;
- same ordinary repository instructions;
- recorded YAIML documents loaded by the YAIML-assisted session;
- recorded commands run and outcomes;
- concise reviewer notes explaining which result better respected project constraints.

Do not describe a personal walkthrough or hypothetical comparison as an independent fresh-session trial. If the same maintainer, prior project context, or prior chat history influenced the run, label that limitation.

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
