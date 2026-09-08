---
yaiml: 0.2
kind: maintainer
title: YAIML Maintainer Guide
purpose: Preserve current procedures for evolving YAIML without drifting from the living-memory concept.
belongs-here: current commands, review procedures, artifact maintenance, failure playbooks.
not-here: project identity, conceptual architecture, complete history.
durability: current-only; remove dead commands and obsolete paths.
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
3. **Evidence and retention:** distinguish source inspection, executed checks, prior reports, fictional examples, and independent trials. Remove stale active risks and duplicate prose. Preserve unresolved conflicts and governed retention.
4. **Mechanical review:** check changed Markdown links and anchors, discovery paths, stable headers, code fences, placeholders, whitespace, and unintended sensitive or machine-specific values.
5. **Final diff:** confirm scope, licensing, and phase boundaries. Commit coherent changes and push when authorized. Report actual checks and remaining limits.

The init prompt is intentionally self-contained. When shortening it, keep the behavior an adopter needs without relying on links to this repository.

Check that init connects the active agent even when its instruction file is absent, verifies scope and discovery paths, and reports unsupported persistence. Future-session checks should use ordinary task requests without naming YAIML; verify both initial reading and maintenance before task completion, including read-only and unchanged-memory cases.

Review init alone against a small repository, mature existing docs, repeated setup, missing access, concurrent edits, and unfamiliar discovery. Check its stopping rule and command scope as well as its length. Track prompt size separately from observed total session cost; word counts do not prove token savings or successful adoption.

For adoption exercises, use isolated snapshots and record their source/reference revisions before editing. Preserve original-file hashes and compare repeat-run changes. Keep generated trial memory out of this reference repository; publish a scoped case summary. The [comparison tasks](EVALUATION.md#ready-to-run-comparison) require separate fresh sessions; a same-session exercise does not satisfy that step.

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
