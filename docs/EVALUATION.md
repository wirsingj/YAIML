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

Keep one short report per trial, with these fields. Use “not measured” or “not run” where appropriate; omit empty narrative sections.

```md
# Trial: project and task

- Source revision and permitted immutable references:
- YAIML reference revision, plus any uncommitted changes:
- Date, agent/model, access, budget, and human reviewer:
- Relationship to project (maintainer-owned, outside snapshot, or owner-led):
- Starting docs, selected task, and criteria fixed before execution:
- Files actually read; files created or changed; documents deliberately skipped:
- Actual commands and outcomes, including unrun checks:
- Result, failures, human corrections, and unresolved uncertainty:
- Prompt size, inspected content, generated memory, and repeat-run changes:
- Total session cost when available; measurement method and excluded costs:
- Evidence retained, where permitted; limitations and next question:
```

Report source inspection, a same-session exercise, a fresh-session comparison, and independent owner feedback as different evidence. Working on another person's public code does not establish their adoption or endorsement.

## Cold-Start Comparison Method

Use bounded comparisons rather than broad claims.

1. Choose a real repository, a fixed revision, and bounded tasks with review criteria set before running them.
2. Prepare isolated copies with the same source and ordinary documentation. Session A gets the baseline without YAIML; Session B gets that baseline plus the recorded YAIML files and minimal discovery pointer. Keep ordinary instructions equivalent, except for that necessary pointer.
3. Start separate fresh sessions without shared chat history, prior answers, or edits from the other condition. Record model/version when available, tool access, permissions, and time or context budgets; keep them comparable.
4. Give both the same task wording. Record what each session actually loads, including any baseline documentation that already performs YAIML-like roles.
5. Compare results against the preset criteria. Repeat when practical; report run counts, failures, and variation rather than selecting a favorable example.
6. Preserve permitted evidence in an approved location. Publish sanitized summaries and reproducible references, not private transcripts or sensitive raw logs.

Tasks should be small enough to review and specific enough to reveal project understanding.

Prevent baseline sessions from discovering added YAIML files through search, history, or preexisting context. Retain concise reviewer notes explaining which result better respected project constraints.

Do not describe a personal walkthrough or hypothetical comparison as an independent fresh-session trial. If the same maintainer, prior project context, or prior chat history influenced the run, label that limitation.

This comparison tests the added memory package, not whether YAIML outperforms equally informative ordinary documentation. For that question, add a condition with the same facts in existing docs without YAIML organization. Account for the cost of creating and maintaining either version.

## Ready-To-Run Comparison

The [local adoption exercise](case-studies/ADOPTION_TRIAL.md) identifies a public `strip-tags` revision and the inspected files. It supplies a candidate, not a completed comparison. Use isolated copies of that same revision; create and retain the YAIML package before either comparison session starts. Keep these reviewer criteria outside both sessions.

Give each fresh session the same bounded requests, with equivalent access and budget:

1. “Trace file or stdin input through the CLI to text extraction. Explain where `--first` stops selection. Cite source; do not edit or run the app.”
2. “Compare the declared Python support range with the configured CI matrix. What does this establish, and what remains unknown? Do not infer passing runs or change support policy.”
3. “Write a maintenance handoff of at most 120 words: relevant checks, unverified behavior, and release boundaries. Read-only inspection is allowed; do not install dependencies or run application, build, or release commands.”

Reviewer criteria: the first answer follows the CLI/library boundary and the first-match exit across selectors; the second distinguishes package metadata, configured coverage, and executed results; the third identifies local checks without claiming they passed or authorizing a release. Count unsupported claims, missed constraints, inspected content, and useful correct answers. Report the cost of building the memory package separately from the comparison sessions.

No comparison result is recorded yet. A project owner reviewing or performing their own trial is still needed for independent adoption evidence. Publish only permitted, sanitized results through [Contributing](../CONTRIBUTING.md#feedback-and-adoption-reports).

## Repeated-Update Pruning Check

Fix a bounded sequence before execution: ordinary work that resolves a risk, changes a decision, adds a necessary constraint, then repeats an unchanged request. Use fresh sessions where practical; do not ask them to prune or mention YAIML.

After each task, inspect whether existing facts were replaced, resolved items removed, and required decisions, evidence limits, and uncertainty retained. Measure the entire affected memory family so moving history into supporting files cannot masquerade as compression. Record unjustified growth, lost knowledge, and manual reminders as failures; necessary growth is acceptable. Compare old and revised instruction pointers on equivalent isolated snapshots if testing this revision's effect.

This is a proposed check, not an executed result.

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
- first-run versus repeated-run cost, including whether an unchanged repository avoids needless rewrites;
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
