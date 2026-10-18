---
yaiml-revision: "0.3.e5a6701538b64592"
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

## Revision And Audit Acceptance

Evaluate against the requested outcomes, not just presence of metadata: a normal implementation and a confirmed conversation-only decision each produce one revision and complete affected-path entry; a no-op, read-only task and unchanged check rerun produce none. Untouched files retain stamps. New evidence corrects its owning claim and records the limited check. Legacy upgrades preserve prior facts, labels, audit entries and paths while declaring unknown history; custom-layout routes resolve. Acquired source counters never advance local counters.

Fork from one parent: both branches may choose the same next counter with different tags. Reconcile independent changes and both entries; the resulting revision exceeds both counters and links both heads, without treating ordering as authority. Exercise fast-forward, revert, interruption and duplicate-ID handling. Distinguish a manual protocol exercise or structural check from actual fresh-session adherence; test the latter across ordinary requests before a 1.0 claim.


The Canopy Dispatch example demonstrates what YAIML can look like, but it is fictional. It is not proof that YAIML improves agent work.

[YTMMOCC](case-studies/YTMMOCC.md) is a real maintainer-owned adoption case. It shows useful repository-carried memory in a published browser-extension project, but it is still internal dogfooding evidence rather than independent proof.

YAIML needs real-project evidence gathered without inflated claims.

A useful evidence set for the public pilot phase should include three distinct case studies:

- one mature repository already known to the maintainer, labeled as internal dogfooding rather than outside proof;
- one unfamiliar public repository initialized without private project context;
- one repository owned by another developer or team.

Internal portfolio repositories can show that YAIML is useful in practice, but they should not be counted as independent adoption evidence.

Keep fictional examples, maintainer-owned field evidence, and independent trials labeled separately.

Separate the object being evaluated. This repository's memory, contribution process and package consistency establish source-project health. A newcomer receiving the product must independently acquire it, recover their own context and use its methods. Our daily use benefits from accumulated maintainer conversation and direct repairs; it is useful dogfooding, not evidence that the same experience requires only one prompt elsewhere.

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
- Result, failures, extra context/reminders/manual repairs supplied, and unresolved uncertainty:
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

Verify actual startup instructions: a no-history worker can still inherit its parent's project guidance. Exclude contaminated controls from comparisons. Record runner failures separately from convention failures; unchanged files after blocked execution do not establish idempotence. The [synthetic trials](case-studies/ADOPTION_TRIAL.md#synthetic-projects-and-session-boundaries) encountered both limitations.

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

## Concurrent-Contributor Check

Use isolated branches from one baseline and the same task permissions. Assign bounded changes without a YAIML reminder: independent facts, competing decisions, a deletion against another contributor's update, and code changes whose memory claims land in different sections. Include a broad-compression branch to assess review churn.

Before integration, apply the project's review policy. Check retained independent facts, unresolved authority, branch versus deployment claims, discovery paths after moves, and evidence scope in the combined tree. Repeat after a target advance or revert. Measure unrelated lines changed, lost constraints, resurrected risks, manual corrections, and final memory size. An old passing result cannot certify merged code.

Text-merge experiments can demonstrate conflict mechanics; they do not test agent behavior. An optional second reviewer may be compared with the same-agent pass, but neither CI nor a subagent is an adoption requirement.

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

## One-Prompt Skills Lifecycle

Evaluate the published entry point from a new user's position: only the init prompt, target project and ordinary host tools. No maintainer paths, preloaded YAIML memory or prior conversation. If testing unpublished work, supply an isolated reference snapshot and label the source override; do not claim public retrieval was exercised. Inspect preloaded host instructions/skill catalogs for contamination even with no chat history.

For a lighter normal-work path, record whether the shared loop suffices without ritual catalog/skill reads, while constraints, verification updates and revision records still survive. Measure guidance words separately from actual session usage; neither a shorter file nor one successful trial establishes token savings. A targeted replay after a fix supplements, rather than erases, the original failure.

| Scenario | Independent acceptance criteria |
| --- | --- |
| First paste | Agent retrieves complete reusable resources and establishes target facts/routes without a second workflow prompt; source-project memory, policies and private/local skills stay outside the adoption |
| Non-code product | Assesses actual document/skill deliverables without treating code absence as an unimplemented product; preserves the distinction between an application proposal and working software |
| Fresh ordinary session | Recovers relevant decisions and updates material understanding without a YAIML reminder |
| Conversational decision and recall | A confirmed decision without an edit request persists; another fresh session recovers it from project files without the earlier chat or a YAIML reminder; a read-only follow-up changes no files |
| Explicit audit / to-do | Honors perspectives/count, existing priorities and task scope; verifies work and reports blocked/fewer items honestly |
| New verification evidence | Reconciles owning passages, stable-header status/date/scope and summaries; replaces stale fresh-session uncertainty with observed instruction/catalog availability and actual method use, preserving untested workflows, menus, other hosts and contrary evidence |
| Composed request | Carries findings into authorized selection/work/verification without requiring separate user invocations |
| Offline reuse | Available local methods work without upstream access or recursive fetching |
| Useful growth | Adds a justified fact owner or reusable method in the established home, checks local references/catalog/native routes, avoids speculative rules/empty artifacts; exercise both default and custom homes |
| Acquisition with changed terms | A missing upstream resource triggers license comparison; changed permissions require authorization before dependent adoption, refusal/pending approval preserves working files, and unchanged terms cause no repeat approval |
| Refresh and repeat | Preserves local skills/adaptations; excludes source-project-only additions; surfaces conflicting changes; repeated unchanged setup produces no churn |
| Source-project use | Its own instructions identify the authoring role; init/refresh preserves authored canonical resources and does not install a published version over development work; copied methods or a matching name alone do not make an adopter the source project |
| Upgrade an earlier installation | Acquires methods from the current reference without requiring installed skills; preserves legacy discovery, project facts, local protections, custom methods and unfinished edits; reports blocked host routes as partial |
| Interrupted acquisition | Working routes remain intact; missing methods are not advertised as ready; applied revision exceptions remain explicit |
| Host change / nested scope | Correct instruction owner, relative routes, arguments and separate subproject boundaries survive |

Record actual artifacts, original-file hashes and skill selections, not merely instruction wording. Distinguish canonical files present, native entries discovered in a fresh session, and invocation with arguments following the canonical method. Plain-text `/...` in a noninteractive runner does not test a host's slash menu. Structural package/link checks can run without another agent, but do not establish behavior. Independent workers require YAIMLACP confirmation. Separate source-availability failures, host activation limitations and workflow failures. Count follow-up reminders or manual repairs as assisted recovery; a later success does not turn the original attempt into an unassisted pass. Keep trial artifacts isolated from this reference repository; publish only concise current evidence and limitations.
