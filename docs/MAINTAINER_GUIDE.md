---
yaiml: 0.2
kind: maintainer
title: YAIML Maintainer Guide
purpose: Preserve current procedures for evolving YAIML without drifting from the living-memory concept.
belongs-here: current commands, review procedures, artifact maintenance, failure playbooks.
not-here: project identity, conceptual architecture, complete history.
durability: current-only; remove dead commands and obsolete paths.
budget: About 1000 words; preserve necessary procedures and evidence if exceeded.
read-with: SoTY; YAIML Architecture.
update-when: repository structure, prompts, templates, or procedures change.
agent-guidance: Verify command claims when practical. Surface conflicts. Preserve human direction.
---

# YAIML Maintainer Guide

This is a documentation repository. There is no application build or test suite to run.

## Review Procedure

Use several focused passes for substantial revisions:

1. **Reader path:** read README, then init alone. Check instructions, templates, coordination, older-adopter coverage, trust boundaries, version labels, and no empty documents. Trace prompts' actions, gates, exceptions and outputs into saved procedures. Require no extra prompts/downloads/lost context; preserve knowledge.
2. **Meaning and consistency:** compare affected guides, prompts, templates, examples, instructions, and memory. Preserve roles, direction, uncertainty, and discovery compatibility. Check external comparisons against primary sources; avoid unsupported exclusivity claims.
3. **Evidence and retention:** distinguish inspected evidence, prior reports, and fictional examples. Apply the [synthesis steps](PRUNING_AND_LIFECYCLE.md#sot-lifecycle) to affected memory; check that history was removed rather than renamed as lessons or moved into supporting files.
4. **Mechanical review:** check changed Markdown links and anchors, discovery paths, stable headers, code fences, placeholders, whitespace, and unintended sensitive or machine-specific values.
5. **Final diff:** confirm scope, licensing, and phase boundaries. Commit coherent changes and push when authorized. Report actual checks and remaining limits.

Review standalone init for small/mature projects, collisions, missing access, routes, nested scope, repeat use, concurrency, unfamiliar discovery. Fresh-session checks omit YAIML reminders; distinguish configured instructions from observed reading/maintenance. Cover confirmed conversational decisions, tentative ideas, unchanged follow-ups, read-only tasks.

Trace [YAIMLACP](YAIMLACP.md) through startup, confirmation/decline/no-answer, changed scope/cost, and missing-guide/host cases. Check context-only assessment, bounded handoffs, cancellation, and no infrastructure setup. Manual review establishes wording coverage; actual delegation and cost require a confirmed trial.

Check evidence guidance against shared-error agreement, irrelevant passing tests, missing baselines, authorized behavior changes, and unreproduced reports. Expected outcomes must not merely echo candidate output.

For budgets, check new, inherited, oversized, legitimately growing, and governed memory. Count whole-document whitespace-delimited words unless locally specified. Targets must not force padding, deletion of necessary knowledge, or bulk header migrations. Report before/after counts, justified net growth, and unresolved overages in the task response; word counts do not prove token savings.

Use isolated snapshots for adoption exercises and record source/reference revisions before editing. Compare original-file hashes and repeat-run changes; keep generated trial memory outside this reference repository and publish scoped summaries. The [comparison tasks](EVALUATION.md#ready-to-run-comparison) require separate fresh sessions; manual instruction review does not satisfy that step.

## Useful Commands

Run from the repository root; Git and ripgrep must be available.

```powershell
git status --short --branch
rg --files --hidden -g '!.git/**'
git diff --check
git diff --stat
```

For terminology or phase changes, search the specific old wording and inspect each hit in context. References to retired approaches are not themselves violations.

```powershell
rg -n 'SPEC|schema|conformance|validator|parser' README.md docs prompts templates ROADMAP.md
rg -n 'documents:|discovery|version' yaiml.yml docs prompts examples
```

These are inspection procedures, not evidence that a review passed. Record actual execution and its scope in the review note. For staged changes use `git diff --cached --check`; after committing, inspect the relevant commit range.

## Propagating Revisions

Update owners then init; adopter-facing changes must reach saved instructions/procedures. Sync templates/supporting/YAIML_GUIDE.md, docs/YAIMLACP.md, ten starters, LICENSE.md. Preserve readable setup; compare obligations, triggers, exceptions, authority, reading routes before/after compression. Check headers/fences/tables, extraction, source parity and [prompt coverage](COLD_START_REVIEW.md#maintenance-prompt-coverage). Keep:

- SoTY current when meaning, risks, priorities, or evidence changes;
- Architecture current when roles or artifact boundaries change;
- this guide current when procedures change;
- [Cold Start Review](COLD_START_REVIEW.md) current after a substantial reader-path revision.

Use [Adoption And Updates](ADOPTION_AND_UPGRADES.md#discovery-layout-compatibility) for discovery compatibility. Ordinary Markdown edits and path repairs do not require a discovery-version bump. In adopters, a convention refresh preserves local memory and does not copy this repository wholesale.

## Common Failure Modes

| Symptom | Correction |
| --- | --- |
| README becomes a second reference manual | Keep definition, adoption, example, limits, and navigation; link detailed rules |
| Core memory becomes a diary or catalog | Use the compression prompt; preserve current decisions, evidence, risks, and lessons |
| Every task loads every document | Restore task-based selection; treat `read-with` as a hint |
| Templates produce empty sections | Omit irrelevant headings and add supporting files only for concrete knowledge |
| A prompt treats an inference as permission | Establish authorized direction and scope before dependent changes |
| Guides drift from prompts or examples | Find the owning explanation, correct it, then update dependent artifacts |
| Tooling or formal specification appears | Check the phase and retired approaches in Architecture before proceeding |

## Sensitive Changes

Preserve `LICENSE.md` as MIT. Do not add license headers or new ownership, trademark, or endorsement claims without explicit maintainer approval.

Follow [SECURITY.md](../SECURITY.md) and [Project Independence](PROJECT_INDEPENDENCE.md). Preserve the maintainer declaration; exclude confidential material and machine-specific reference locations. Do not turn agent-written notes into legal or security assurances.

Case studies must retain dates, evidence sources, ownership, and limits. A documentation edit does not revalidate an external repository or store listing. Before a public pilot, verify that the private reporting route in Security still works; do not submit a dummy vulnerability report to test it.

## Branch Review

Use the [concurrent-branch workflow](PRUNING_AND_LIFECYCLE.md#concurrent-branches-and-review): keep routine edits focused, coordinate broad cleanup separately, compare against the actual target, and review combined meaning and evidence before authorized integration. Preserve unresolved contributor decisions. No extra reviewer service or CI setup is required.

## Publication

Review the worktree before staging so unrelated work is preserved. Use ordinary commits; do not rewrite shared history. Check remote state before pushing. If it has advanced, inspect and integrate compatible changes without discarding another contributor’s work.

The current review evidence belongs in [Cold Start Review](COLD_START_REVIEW.md), not an accumulating checklist here.
