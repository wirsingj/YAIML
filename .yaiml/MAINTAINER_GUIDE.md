---
yaiml-revision: "0.47.a709c1ceed90c210"
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

Include any [pending corrections](changes.md).

Documentation repository; no application build/test suite. Current [publication review](../docs/evaluation/COLD_START_REVIEW.md#052-publication-review) covers reference closure, both init forms/routes, live latest-tag execution and exact-source public retrieval; fresh-agent behavior remains unverified. Earlier [0.5.1 checks](../docs/evaluation/EVALUATION.md#post-review-cross-host-trial-gate-2026-10-24) retain their own scope. Host-delivered instructions/skill metadata and actual method reads do not validate every invocation or another host.

## Review Procedure

Review substantial revisions:

1. **Adopter experience:** start with init alone and no YAIML context; trace public source or labeled draft through bootstrap, local methods and fresh sessions. Check [lifecycle scenarios](../docs/evaluation/EVALUATION.md#one-prompt-skills-lifecycle). Record extra context, reminders and manual repairs as assistance.
2. **Source project:** keep reusable material in `reference/`, explanation/evaluation/development documents in `docs/`, fictional projects in `examples/` and public direction in root `ROADMAP.md`. Reserve `.yaiml/` for our working context/audit/local methods; discovery may point out to project artifacts. Shared-method changes require adopter and self-use review. Check affected routes, Markdown links/anchors, plain-text paths, commands, reading hints and discovery maps after moves. Preserve historical record bytes and label old paths as history.
3. **Evidence and retention:** distinguish source checks, internal dogfooding, isolated product trials and independent adoption. Apply [synthesis](../docs/PRUNING_AND_LIFECYCLE.md#sot-lifecycle); remove superseded history without disguising or relocating it.
4. **Package and mechanical review:** check acquired-set links/anchors with source-only files absent, not just in the full checkout. Review document ownership as well as reachability/hashes; check the whole `reference/` tree without `.yaiml/` present, verify embedded revision placeholders, README prompt links and standalone/canonical init parity, and index relevant target docs. Check headers, fences, placeholders, whitespace and sensitive/location values.
5. **Final diff:** check scope, licensing and phase boundaries; commit/push when authorized. Report checks and limits.

Review standalone init for small/mature projects, placement/relocation/collisions, missing access, routes, nested scope, repeat use, concurrency, unfamiliar discovery. Fresh-session checks omit YAIML reminders; distinguish configured instructions from observed reading/maintenance. Cover confirmed conversational decisions, tentative ideas, unchanged follow-ups, read-only tasks.

Trace [YAIMLACP](../reference/YAIMLACP.md) through startup, confirmation/decline/no-answer, changed scope/cost, and missing-guide/host cases. Check context-only assessment, bounded handoffs, cancellation, and no infrastructure setup. Manual review establishes wording coverage; actual delegation and cost require a confirmed trial.

Check evidence guidance against shared-error agreement, irrelevant passing tests, missing baselines, authorized behavior changes, and unreproduced reports. Expected outcomes must not merely echo candidate output.

Count affected whole-document whitespace-delimited words, including headers. Report growth reasons and overages outside memory. Preserve necessary knowledge and governed records; budgets never require padding or destructive pruning. Word counts do not prove token savings.

Use isolated snapshots for adoption exercises; record tested revisions, compare original-file hashes and repeat-run changes. Keep raw fixtures, session profiles, logs and generated reports outside this repo or in ignored `.yaiml/tmp/`; commit only reviewed, scoped summaries. [Comparison tasks](../docs/evaluation/EVALUATION.md#ready-to-run-comparison) require fresh sessions; manual review cannot establish fresh-agent behavior.

## Useful Commands

Run at repository root; requires Git and ripgrep.

```powershell
git status --short --branch
rg --files --hidden -g '!.git/**'
git diff --check
git diff --stat
```

For terminology or phase changes, search the specific old wording and inspect each hit in context. References to retired approaches are not themselves violations.

```powershell
rg -n 'SPEC|schema|conformance|validator|parser' README.md reference docs .yaiml
rg -n 'documents:|discovery|version' .yaiml/yaiml.yml reference docs examples
```

Commands are procedures, not passes. Record executed checks and scope in the review note. Use `git diff --cached --check` for staged changes; inspect the commit range after committing.

## Propagating Revisions

The shared guide owns ordinary work; skills add specialized methods; prompts/host entries route to their owners. Update owners and callers together. Check seed parity, isolated package closure, skill metadata/arguments, links/anchors, eleven starters, notice and [coverage](../docs/evaluation/COLD_START_REVIEW.md#maintenance-prompt-coverage). Keep:

- SoTY current when meaning, risks, priorities, or evidence changes;
- Architecture current when roles or artifact boundaries change;
- this guide current when procedures change;
- [changes.md](changes.md) complete for material iterations under [VERSIONING.md](../reference/VERSIONING.md);
- [Cold Start Review](../docs/evaluation/COLD_START_REVIEW.md) current after a substantial reader-path revision.

Use [Adoption And Updates](../docs/ADOPTION_AND_UPGRADES.md#discovery-layout-compatibility) for discovery compatibility. Ordinary Markdown edits and path repairs do not require a discovery-version bump. In adopters, a convention refresh preserves local memory and does not copy this repository wholesale.

## Common Failure Modes

| Symptom | Correction |
| --- | --- |
| Init is hard to find | Put a direct init link near the README title; show setup/upgrades before conceptual details; keep deeper references optional |
| Core memory becomes a diary or catalog | Use the compression prompt; preserve current decisions, evidence, risks, and lessons |
| Every task loads every document | Restore task-based selection; treat `read-with` as a hint |
| Templates produce empty sections | Omit irrelevant headings and add supporting files only for concrete knowledge |
| A prompt treats an inference as permission | Establish authorized direction and scope before dependent changes |
| Guides drift from prompts or examples | Find the owning explanation, correct it, then update dependent artifacts |
| Tooling or formal specification appears | Check the phase and retired approaches in Architecture before proceeding |

## Sensitive Changes

Preserve [licensing](../LICENSE.md) and prior grants. Maintainer approval governs terms, headers and ownership/trademark/endorsement claims. Obtain professional review before publication.

Follow [SECURITY.md](../SECURITY.md) and [Project Independence](../docs/PROJECT_INDEPENDENCE.md). Preserve the maintainer declaration; exclude confidential material and machine-specific reference locations. Do not turn agent-written notes into legal or security assurances.

Case studies must retain dates, evidence sources, ownership, and limits. A documentation edit does not revalidate an external repository or store listing. Before a public pilot, verify that the private reporting route in Security still works; do not submit a dummy vulnerability report to test it.

## Branch Review

Use the [branch workflow](../docs/PRUNING_AND_LIFECYCLE.md#concurrent-branches-and-review) and [record procedure](../reference/CHANGE_RECORDS.md). Check ordinary consolidation, overlap deferral, pending recall, navigation repair, retained history and preparation for review. Preserve unresolved authority. Apply this source project's updates under actual task ownership; acquiring guidance grants no exclusivity.

## Publication

Review the worktree before staging; preserve unrelated work and shared history. Ask the maintainer before every push to `origin` and await approval for that push; prior blanket approvals no longer apply. Check remote state and preserve concurrent changes.

Keep feature work on feature branches. `main` is stable development; merging there is the maintainer's public-ready decision. The source-only [latest workflow](../.github/workflows/latest.yml) advances only `refs/tags/latest` after main updates, without creating a GitHub Release. Numbered tags, if used, stay immutable. Publish resources with the seed, then verify the workflow and public retrieval at the resolved commit. If tag rules or token permissions block advancement, report the failure; do not bypass protections. A manual workflow rerun on main can retry after the maintainer resolves the cause.

`reference/BOOTSTRAP.md` owns consumer product identity; [RELEASE.md](../docs/development/RELEASE.md) owns source readiness. Project-memory-only changes need no product-version bump. Current evidence belongs in [Cold Start Review](../docs/evaluation/COLD_START_REVIEW.md); local checks cannot prove publication.
