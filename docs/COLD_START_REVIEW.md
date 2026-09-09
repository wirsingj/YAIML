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

Date: 2026-09-08. Baseline: `c9b4c8b`.

## Scope And Findings

Broad manual review of the reader path, seven prompts, reference guidance, templates, fictional examples, case evidence, licensing consistency, security boundaries, compatibility, and memory cost. The assisting agent reviewed and edited the material in the same session; this is not an independent evaluation or a legal/security certification.

| Area | Finding and correction |
| --- | --- |
| Adoption and normal use | The adoption guide still demonstrated explicit YAIML reminders and a reference-dependent setup request. It now uses the standalone init and ordinary task wording. |
| File safety | Default filenames and path checks left output handling implicit. Init now explicitly preserves unrelated files occupying default names and resolves memory/instruction paths before reads or writes. |
| Reading cost | Adoption and refresh repeated preservation rules across long checklists. They were consolidated, and context guidance now explicitly permits reusing already-loaded current memory. |
| Authority and budgets | A label could be mistaken for authenticated approval, or a budget for a length to fill. Guidance now rejects both interpretations while preserving necessary growth and retention. |
| Phase and evaluation | A milestone implied a separate helper was needed. It now asks for a repeatable maintenance workflow. A comparison request now explicitly permits read-only inspection without running application/build/release commands. |

Core roles, human direction, meaningful local choices, migration safeguards, examples, and evidence limits remain. The init prompt still carries the full setup convention without requiring a reference download or installation.

## Size And Pruning

Whitespace-delimited counts include the entire document and header:

| Document | Before | After |
| --- | ---: | ---: |
| prompts/init-yaiml.md | 1545 | 1525 |
| prompts/update-yaiml.md | 1104 | 658 |
| docs/ADOPTION_AND_UPGRADES.md | 1718 | 1120 |
| docs/SoTY.md | 872 | 761 |
| docs/MAINTAINER_GUIDE.md | 926 | 865 |

SoTY and Maintainer Guide remain within their 1,000-word working targets; unchanged Architecture remains 669/800. Completed audit history was removed from this review in favor of the current findings and links to retained case evidence. No archive or runtime tooling was added. These are size measurements, not measured total token savings.

## Verification

Temporary local inspection scripts checked 49 Markdown files, 82 local links, three discovery maps, 24 declared document paths and headers, and four fenced YAML examples. Checks passed for balanced fences, tracked link targets and anchors, path scope, YAML parsing, merge markers, and targeted credential/machine-path patterns. The pattern scan covers the current tree, not an exhaustive secret or history audit. The whitespace diff check also passed. These are repository checks, not a YAIML conformance system.

The retained [adoption-trial](case-studies/ADOPTION_TRIAL.md) artifacts still match recorded hashes for the original public snapshot, five generated files, and five unchanged legacy files; generated-file word counts also match. All 18 pinned [YTMMOCC case-study](case-studies/YTMMOCC.md) file references resolve in the local Git objects. These checks do not rerun prompt adoption, extension behavior, or store observations.

The existing MIT text was compared with the [OSI reference](https://opensource.org/license/mit); license and maintainer declarations are unchanged. No ownership or legal-compliance conclusion follows. GitHub's [reporting endpoint](https://api.github.com/repos/wirsingj/YAIML/private-vulnerability-reporting) returned HTTP 200 with `enabled: true` on 2026-09-08; no setting was changed or report submitted.

## Remaining Limits

No fresh-session comparison, cross-provider execution, independent owner-led trial, or total-session cost measurement was performed. Filename-collision, unsupported-persistence, read-only, concurrency, budget, and uncertain-authority scenarios were reviewed as instruction paths, not executed agent tests. The [prepared comparison](EVALUATION.md#ready-to-run-comparison) and ordinary-request demo remain next evidence steps.

Current priorities belong in [SoTY](SoTY.md). Future reviews should respond to concrete failures and evidence rather than accumulate more rules by default.
