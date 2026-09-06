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

Date: 2026-09-06

## Scope And Method

Three manual audit/correction passes reviewed the repository as material a reader might hand to an unfamiliar AI agent:

1. Reader path, verbosity, repetition, and core-memory size.
2. Authority, discovery/header semantics, template consistency, and evidence boundaries.
3. Regression review of the shortened instructions, examples, local references, and publication diff.

Baseline: commit `cbe412e`, which preserves the worktree revisions present at the start of this review. Scope includes README, agent instructions, all declared memory, prompts, templates, examples, roadmap, and public policies.

The same assisting agent performed the edits and review. This is not an independent review, controlled fresh-session trial, or evidence that another model will follow the prompts successfully.

## Findings And Corrections

| Finding | Correction |
| --- | --- |
| README and init repeat much of the reference | README links to topic guides; init retains a self-contained minimum without embedding three full templates |
| Core memory repeats artifact lists, doctrine, and checklist items | Consolidated roles, current state, and procedures into their own documents |
| Core templates invite repeated facts under overlapping headings | Combined sections and made omission of empty headings explicit |
| Realignment permits broad deletion before establishing corrected intent | Requires human-directed scope, preserves unrelated work, and distinguishes design from transitional implementation |
| Header fields, companion hints, and versions invite strict-format assumptions | Explained flexible headers, non-recursive reading, path resolution, and discovery versus prose revisions |
| Fictional results and local-storage language can imply more than intended | Added nearby fictional-result labels and clarified that an AI tool has its own data handling |
| Review/evaluation wording risks overstating evidence | Kept inspection distinct from trials; improved baseline isolation, comparable conditions, and reporting limits |
| Earlier approved text could appear immutable | Clarified that authorized decisions may supersede it, with the change recorded |

## Verification

Local inspection ran on Windows using Git, Python, and the existing PyYAML library. Temporary review checks were not added as project tooling.

- Parsed all three discovery maps; all 23 declared document paths resolved and their files had stable header delimiters.
- Checked all 48 tracked Markdown files for balanced code fences and local Markdown links, including heading anchors; no errors found.
- A targeted scan found no concrete machine-specific reference values in the checked patterns. This is not a comprehensive secret scan.
- `git diff --check` passed for the corrections.
- The MIT License and discovery map contents were unchanged by the audit corrections.

These checks establish local structural consistency, not Markdown schema conformance or agent effectiveness. External links, store listings, extension behavior, and prior case-study checks were not revalidated.

Whitespace-delimited word counts against the baseline:

| Document | Before | After |
| --- | ---: | ---: |
| README | 2,317 | 742 |
| Init prompt | 4,305 | 1,178 |
| SoTY | 1,233 | 734 |
| Architecture | 1,093 | 570 |
| Maintainer Guide | 2,245 | 721 |

These measure text reduction, not token cost or improved outcomes.

## Remaining Limits

The shortened prompt still needs fresh-session adoption, refresh, and compression trials, including legacy discovery layouts. Independent projects and comparable baselines are needed before claims of broad compatibility or productivity improvement.

The prior review recorded local adopter sampling on 2026-07-11: useful project-specific memory coexisted with older maps and machine-specific reference paths. That report was not reproduced here. Retain its practical lesson—test portability and cleanup—without treating local sampling as independent proof.

A private sensitive-reporting path remains unestablished by the evidence recorded here. Current active priorities belong in [SoTY](SoTY.md); evaluation procedure belongs in [Evaluation](EVALUATION.md).
