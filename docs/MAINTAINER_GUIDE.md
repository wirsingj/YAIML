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

1. **Reader path:** read README as a newcomer, then the init prompt by itself. Check that adoption is understandable without opening every guide or creating empty documents.
2. **Meaning and consistency:** compare affected reference guidance with prompts, templates, examples, agent instructions, and living memory. Preserve document roles, human directives, uncertainty, and discovery compatibility.
3. **Evidence and retention:** distinguish inspected evidence, prior reports, and fictional examples. Apply the [synthesis steps](PRUNING_AND_LIFECYCLE.md#sot-lifecycle) to affected memory; check that history was removed rather than renamed as lessons or moved into supporting files.
4. **Mechanical review:** check changed Markdown links and anchors, discovery paths, stable headers, code fences, placeholders, whitespace, and unintended sensitive or machine-specific values.
5. **Final diff:** confirm scope, licensing, and phase boundaries. Commit coherent changes and push when authorized. Report actual checks and remaining limits.

Review init by itself for small projects, mature docs, filename collisions, missing access or instruction files, repeat use, concurrent edits, and unfamiliar discovery. Keep the prompt self-contained and inspection bounded. Distinguish configured persistent instructions from observed loading; fresh-session checks should use ordinary requests without naming YAIML and verify both reading and writing, including read-only tasks.

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

Update the affected reference guide first, then dependent prompts, templates, and examples. Keep:

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

## Publication

Review the worktree before staging so unrelated work is preserved. Use ordinary commits; do not rewrite shared history. Check remote state before pushing. If it has advanced, inspect and integrate compatible changes without discarding another contributor’s work.

The current review evidence belongs in [Cold Start Review](COLD_START_REVIEW.md), not an accumulating checklist here.
