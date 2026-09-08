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

Date: 2026-09-07. Baseline: `f7d8ef8`.

## Scope And Findings

Audit of YAIML's adoption path, refresh/compression guidance, evidence, human readability, privacy/reporting, license preservation, and current priorities. The same assisting agent reviewed and edited the repository. This is not an independent evaluation, legal opinion, or security certification.

The main actionable finding was that creating `AGENTS.md` alone did not establish a persistent route for the active agent. Init now identifies and connects its supported instruction mechanism, including a missing file when necessary, checks activation and discovery scope, and reports setup gaps. Routine reading and maintenance before task completion require no separate YAIML request. Read-only tasks and unchanged memory remain respected.

The standalone init prompt is now 1,361 whitespace-delimited words, up from 1,255. It still needs no reference download or installation. The demo now asks ordinary questions and supplies a changed product decision without naming YAIML, so a future run can check both automatic reading and writing. No new fresh-session run occurred in this review; configured instructions are not proof of observed loading.

## Prior Priority Outcomes (2026-09-06)

| Priority | Outcome and limit |
| --- | --- |
| Trial init, refresh, and compression | Executed isolated document exercises on a public source checkout and a maintainer-owned legacy memory snapshot; recorded sizes and unchanged files. These were same-session exercises, not ongoing adopter field trials. |
| Comparable fresh-session tasks | Prepared fixed tasks and reviewer criteria. Separate fresh sessions and independent owner participation have not occurred; this priority remains open. |
| Exercise older discovery | Refreshed and compressed the local guide in the legacy snapshot while preserving the entire map, core memory, and agent instructions. No reader migration or universal compatibility claim. |
| Short demo and private reporting | Added the fictional demo. Enabled GitHub private reporting; the update returned HTTP 204 and a subsequent uncached read returned `enabled: true`. No vulnerability report was submitted. |
| Scoped evidence and pruning | Added a bounded trial summary, replaced this review, and updated SoTY's current state and remaining priorities. |

The [trial summary](case-studies/ADOPTION_TRIAL.md) records conditions, inspected revisions, measured sizes, and limits. The public initialization produced five files totaling 717 words; a same-session repeat and same-reference refresh required no edits. Legacy guide refresh/compression changed 943 words to 1,033, then 596, without changing the map or core documents.

## Verification

Local checks passed for 49 Markdown files, 77 local links/anchors, three discovery maps, 24 declared document paths with stable headers, and four fenced YAML examples. Checks included case-sensitive paths, fences, UTF-8 decoding, merge markers, and targeted credential/machine-path patterns. `git diff --check` passed. This is structural review and a current-tree pattern scan, not an exhaustive secret or history audit.

The inspection helpers used existing local tools only; no validation framework or runtime was added to YAIML. The license and discovery layouts remain unchanged. Manual instruction review covered existing and missing instruction files, unsupported persistence, scoped paths, read-only tasks, and unchanged memory; these are coverage checks, not executed cross-provider trials.

The existing MIT License remains unchanged. Original source and license files in the public trial checkout were preserved byte-for-byte. This verifies preservation, not ownership or legal compliance. Prior case-study runtime checks and store observations were not rerun.

GitHub reporting state was checked on 2026-09-06 through the [repository reporting endpoint](https://api.github.com/repos/wirsingj/YAIML/private-vulnerability-reporting). [GitHub's API documentation](https://docs.github.com/en/rest/repos/repos#enable-private-vulnerability-reporting-for-a-repository) describes this setting; the reporting route is linked in [Security](../SECURITY.md).

## Remaining Work

The [prepared comparison](EVALUATION.md#ready-to-run-comparison) still requires separate fresh sessions and permitted independent participation. Same-agent success cannot establish general reliability, total token savings, or cross-provider performance. The demo's fresh-session portion is instructions, not an executed result.

Discovery compatibility remains scoped to the exercised files. Concurrent edits, unfamiliar future layouts, and repeated use in other agent environments need additional trials. Current priorities belong in [SoTY](SoTY.md).
