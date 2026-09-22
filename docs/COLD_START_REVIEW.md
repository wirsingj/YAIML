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

Date: 2026-09-22. Baseline: d391962; review includes the documentation changes prepared with this note.

## Findings And Corrections

Reviewed all repository documents, prompts, templates, and examples for adoption clarity and support for README claims.

- Init's pointer now carries evidence and authority distinctions into later sessions, including defined versus executed checks. Setup connects applicable existing instruction routes across agents, preserves their scope and shared includes, and reports incomplete routes individually.
- New-repository handling now explicitly leaves absent implementation and undecided design unclaimed; new discovery is explicitly rooted at the repository top level.
- README now explains individual continuity, team review, and portable project knowledge; defines SoT before use; and distinguishes YAIML's lack of a service from the chosen AI tool's data handling.
- Stable Headers called verification timing required while its minimum example omitted it. Verification remains scoped to claims, with an optional document-level summary.
- Prior Art overstated other approaches' limitations and YAIML's uniqueness. Descriptions now cite checked primary sources and acknowledge overlap. Older case-study counts lack a recorded baseline/method; the report now labels those limits and the causal hypothesis.

## README-To-Init Check

| Reader expectation | Prompt support |
| --- | --- |
| One self-contained prompt, no installation | Opening and Inspect First bound setup to repository evidence and inexpensive checks |
| Preserve existing work and useful docs | Inspect First and Add Discovery preserve dirty work, role owners, filenames, and older layouts |
| Small, evidence-aware memory | Core roles, supporting-file threshold, budgets, labels, and verification scope |
| Ordinary future work across agents maintains memory | Connect Future Sessions updates applicable existing instruction routes to one memory family and reports activation gaps |
| Shareable team workflow | Pointer preserves review authority, focused edits, branch reconciliation, and retention rules |

These are verified instruction provisions, not observed success in a fresh agent session.

## Verification

Temporary parser-based inspection passed for 50 Markdown files, 97 local links/anchors, three YAML discovery maps, and 25 declared paths/headers. The init map matches the minimal example. UTF-8, fences, conflict markers, targeted private-path/token patterns, whitespace, and unchanged license checks passed. Comparison sources are linked in [Prior Art](PRIOR_ART.md). No application build or runtime tests exist here.

## Remaining Limits

The standalone prompt was manually reviewed for empty repositories, mature docs, filename collisions, uncommitted/concurrent work, older discovery, repeat use, read-only access, multiple instruction files, shared includes, nested scope, and missing tool support. No fresh-agent adoption or provider-switch trial was run. Team review burden, repeated pruning, and total cost remain unmeasured. External adopter state and historical measurements were not revalidated. Pattern scans are limited checks, not a security assurance. [Evaluation](EVALUATION.md) supplies the next trials.

Current priorities belong in [SoTY](SoTY.md); earlier audit history remains in Git.
