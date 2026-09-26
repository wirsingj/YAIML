---
yaiml: 0.2
role: review
title: Cold Start Review
purpose: Manual review notes for whether an unfamiliar AI chat or coding agent can understand and use YAIML from this repository alone.
belongs-here: cold-start findings, repository usability checks, gaps that affect first-time AI-session understanding.
not-here: permanent architecture, command reference, implementation promises.
durability: current review note; replace after major repository shifts.
read-with: SoTY; Architecture; Maintainer Guide.
update-when: adoption or persistent-instruction changes materially affect first-time or future-session behavior.
agent-guidance: Treat this as review evidence, not a normative source. Verify current files before relying on it.
---


# Cold Start Review

Date: 2026-09-26. Baseline: 6fe0a50; review includes the documentation changes prepared with this note.

## Findings And Corrections

Scope: evidence guidance, init's persistent pointer, refresh/audit prompts, the maintainer template, and YAIML's own instructions and memory. README claims were checked for consistency; adoption structure and discovery are unchanged.

The maintainer reported a depth-layering regression in another project and supplied that agent's proposed guidance. This establishes a reported failure, not its cause: the application, checks, and investigation were not inspected here.

Repository inspection found existing intent/evidence distinctions but no explicit requirement to ground behavioral expectations independently of the candidate. [Evidence guidance](AMBIGUITY_AND_EVIDENCE.md#contradictions-and-regression-checks) now covers that gap, baseline limitations, and contradictory feedback. Init carries a compact rule into persistent instructions; refresh carries it to existing adopters. Neither setup nor refresh authorizes application fixes or new test infrastructure.

## Manual Challenge Review

Reviewed the guide and standalone pointer against these cases. This is a reading-based consistency check, not an agent execution trial.

| Case | Required interpretation supported by the revised text |
| --- | --- |
| Two implementations share an inversion; equality check passes | Agreement is insufficient; check independently established expected ordering |
| Tests echo the selected setting, but rendered behavior is rejected | Check the user-visible outcome; do not redefine acceptance around the setting |
| Authorized direction deliberately changes previous behavior | Preserve the new decision; an old baseline is not proof of correctness |
| No accepted baseline or reliable expected result exists | Report the gap without inventing evidence; continue independent authorized work |
| A reported symptom cannot be reproduced locally | Keep report, conditions, and hypothesis separate; non-reproduction does not refute it |
| A later session receives only the installed instruction pointer | Independent checks, default isolation, and decision authority are present there |
| Initialization discovers a possible regression | Preserve it as uncertainty; do not change application behavior during setup |

Factual disputes require relevant evidence; changing intent or acceptance criteria still requires established decision authority. The fictional example illustrates this distinction and is not a reconstruction of the reported incident.

## Verification

Temporary parser-based inspection passed for 50 Markdown files, 98 local links/anchors, three YAML discovery maps, and 25 declared paths/headers. The init map matches the minimal example. UTF-8, fences, conflict markers, targeted private-path/token patterns, whitespace, and unchanged license checks passed. No application build or runtime tests exist here.

## Remaining Limits

No fresh-agent, application-regression, or provider-switch trial was run. The new guidance is motivated by feedback and a verified wording gap; its effect on recurrence is untested. Team review burden, repeated pruning, and total cost remain unmeasured. External adopter state and historical measurements were not revalidated. Pattern scans are limited checks, not a security assurance. [Evaluation](EVALUATION.md) supplies the next trials.

Current priorities belong in [SoTY](SoTY.md); earlier audit history remains in Git.
