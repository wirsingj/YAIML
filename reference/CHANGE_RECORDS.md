---
yaiml-revision: "0.43.65c0797e642cbbde"
role: change-record-guide
title: Change Records And Current Memory
purpose: Preserve intent and evidence while choosing when shared memory can be consolidated.
not-here: A mode switch, automatic code merger, global worker detector or lock service.
budget: About 2000 words total; normative rules take precedence over explanatory rationale.
durability: Shared procedure; preserve project authority, established paths and audit retention.
update-when: Recording, consolidation, recovery or retention procedures change.
agent-guidance: Reuse current context; routine recording is in VERSIONING. Read integration/recovery detail only when relevant.
---
# Change Records And Current Memory

## Normative Rules

All procedures below are required when their stated conditions apply. The final explanatory section provides rationale only; it adds no requirements.

Every material iteration has one retained record. Current memory combines the core snapshots with pending corrections. Consolidate during ordinary work when ownership permits; defer during overlap. There is no single-user/team mode and no extra user prompt for routine maintenance.

## Read Current Context

The existing `changes.md` locates the record directory (default `changes/` beside it), consolidated revision and exact incorporated record IDs. Retain older inline audit entries. Enumerate filenames and read only IDs absent from the receipt, then relevant snapshots. If the receipt lists missing records or its incorporation state is unclear, report incomplete context and follow recovery below; absence of pending filenames alone proves nothing. With no pending IDs, use current owners and actual artifacts for ordinary handoff or verification-status questions. Read a specific incorporated record only for missing/disputed evidence or an explicit history trace; do not bulk-read history to re-prove current summaries. Reuse loaded context. Parallel counters may match, so numeric/time cutoffs are insufficient.

For a large history, use existing file tools to compare the full receipt and filenames locally, bringing only pending paths, missing IDs and necessary header facts into context where practical. Truncated output is not a complete comparison. Report incomplete access/comparison rather than assuming no pending work; this does not authorize deleting history or replacing exact IDs with a numeric cutoff.

Incorporated means accounted for, including a correction explicitly superseded or reversed by a later recorded decision; it does not mean every historical assertion remains in effect. Keep that earlier ID incorporated so it cannot reappear as pending work.

Compose pending corrections by stated scope and human authority with actual artifacts. A retained baseline or later filename cannot undo another contributor's approved change. Preserve unresolved claims and recompute derived facts. Core-only readers cannot claim current context while records are pending. Short pointers in the core headers/openings locate this audit; they need no edits per pending change.

## Record Schema And External Validation Contract

This is the normative stable record contract for 0.5.x. It defines integration points for external consumers; YAIML implements no validator, gatekeeper or semantic merger. Project memory bodies remain free-form Markdown. The contract below is self-contained; initialize records from the target's actual work, never YAIML's source-project history.

A finalized record has YAML frontmatter with these required fields:

| Field | Required meaning |
| --- | --- |
| `yaiml-revision` | Quoted project revision ID under VERSIONING; must equal the filename stem |
| `parents` | List of immediate prior revision IDs; empty only for a declared prospective baseline |
| `date` | Calendar date in `YYYY-MM-DD` form; never an ordering or authority rule |
| `role` | Literal `change-record` |

The required body sections are **Authority**, **Outcome**, **Checks**, **Limits**, **Affected paths**, each represented by a named Markdown heading or a paragraph label followed by a colon. Authority identifies intent and authorized decision source; Outcome records changed facts/owners and results; Checks states actual verification; Limits preserves unrun checks, uncertainty and gaps; Affected paths lists every actually changed project-relative path, including the record, in code spans, identifying additions/deletions and both paths of renames when applicable. Compatible local extensions may add fields/sections without changing these meanings. Existing historical records are retained as written; upgrades do not rewrite them into this schema.

External tools may validate the following invariants against the iteration's recorded baseline/final state and retained finalization evidence. They must report unavailable evidence as **unverified**, not a pass; structural consistency never proves human authority, correctness or exclusive ownership.

1. **Receipt and pending set:** every exact incorporated ID in `changes.md` corresponds to a retained record file on disk; pending IDs equal record files on disk minus the incorporated set. The consolidated revision identifies the accounted-for snapshot head, while pending records still contribute current context. Retained older inline entries are not fabricated per-record files.
2. **Diff coverage:** a record's Affected paths equals the actual changed-path set of its iteration, including its own path, partial writes, receipt/snapshots, all non-Markdown paths, deletions and both rename endpoints. Use the iteration boundary, not an accumulated branch diff; inspected/unchanged files are check scope only.
3. **Changed stamps:** each changed managed Markdown file carries that iteration's revision in its prescribed stamp location. Unchanged files retain their stamps; unchanged imports and unmodified acquired resources retain source stamps. Legal notices and code/configuration receive no injected stamps. Template placeholders and copied prompt payloads are not the containing document's stamp.
4. **Lineage:** parents identify actual immediate revision ancestry; ordinary local counters advance above known local heads. Reconciliation counters exceed both parent lineages and list both consumed heads as parents. Git ancestry, when available, corroborates the iteration mapping without confusing Git commits with revision IDs: retained IDs survive permitted squashes/cherry-picks and new reverts. Missing ancestry evidence stays unverified; timestamps/tags never settle competing meaning.
5. **Finalization immutability:** no completed record's bytes change after finalization. Compare retained finalized bytes or another established historical baseline; a current stamp alone cannot establish immutability. Corrections/reverts create linked new records and preserve the old bytes, including when `git revert` would delete them or roll the receipt backward. Explicit retention/privacy exceptions still require their own authority and traceable treatment.

These rules are the single normative schema/invariant definition. Other guides link here for record structure and external checks; workflow instructions still own when to record, consolidate or recover. No parser, runtime enforcement or automatic conflict decision is implied.

## Record Once

Use [the iteration steps](VERSIONING.md#complete-one-iteration) and [the record contract](#record-schema-and-external-validation-contract). One `<revision>.md` is both the audit and memory correction. Aim for 100–200 words, expanding for necessary authority/evidence. Use code spans for historical paths. Avoid duplicate audit narratives, full replacement snapshots, unchanged constraints and transcripts.

Confirmed conversation-only decisions follow the same procedure. Tentative, read-only and unchanged work writes nothing. Completed records are immutable; corrections get linked new records. A task that also consolidates uses the same iteration, not another ritual revision. Later consolidation of completed pending records gets its own record and links all consumed heads.

## Decide Whether To Consolidate

Use existing task ownership and coordination context, without scans of unrelated projects or automatic worker launches. An ordinary task with established sole ownership of this working copy can consolidate at completion. Known parallel contributions to the same project memory, a designated integration writer, ambiguous ownership or unexplained changes require deferral. Separate branches do not by themselves establish sole ownership of shared project memory.

Before consolidation, reread affected snapshots, receipt and pending filenames against the state used for this task. If they changed, reorient and reconcile under the actual ownership; do not overwrite another writer. A clean Git status, lack of lock files or a quiet reread does not prove exclusivity. This convention cannot discover silent contributors across hosts or make comparison-and-write atomic; use existing coordination to establish ownership. If that remains uncertain, preserve work in a record and report pending consolidation.

When deferring, leave factual snapshots and the shared receipt unchanged. Repair current navigation immediately after moves/deletions, including links in snapshots, discovery and routes; stamp/audit focused repairs and preserve concurrent edits. This may cause structural conflicts but prevents unusable guidance. Keep historical records intact. Broad compression queues only a concise synthesis request and preservation concerns; it does not copy replacement snapshots.

## Consolidate And Check

With sole ownership, apply pending corrections and the current task to their existing owners, using actual artifacts and authority. Remove superseded claims and needless repetition; preserve constraints, contrary evidence and unresolved decisions. Update verification passages and affected headers, including setup evidence. Recompute combined claims and run relevant checks. A normal task may consolidate existing pending work without a separate request, within its project-memory scope; that does not authorize unrelated code integration.

Finalize the iteration record with all affected paths, including `changes.md`, imported records, moves and deletions. Stamp changed managed Markdown. Verify the record against the final diff. Update the consolidated revision and exact incorporated set only after snapshots, evidence and record agree; include the current record. Do not append the same narrative to `changes.md`. Retain incorporated records as history and skip their bodies during ordinary reading. Report necessary growth and any incomplete consolidation outside memory.

For requested Git integration, inspect the actual target/common ancestor and every consumed head through [yaiml-git](skills/yaiml-git/SKILL.md). A clean merge does not resolve meaning. Preserve imported records and prior audit exactly, reconcile artifacts within scope, then perform the same consolidation. Preparation for a commit/MR can do this with established sole ownership; it grants no commit or publication permission by itself.

## Transition And Recovery

An upgrade preserves existing memory, record directories, receipts and inline history. Establish missing record pointers prospectively; retain the recognized local heads/counter from the inline audit rather than resetting them. The receipt identifies incorporated per-change files, not every historical inline entry. Include existing record IDs only after confirming their corrections are represented in current snapshots or explicitly superseded/reversed with traceable outcomes; ambiguous records stay pending. Do not split or rewrite old entries. An old `maintenance-mode` flag is retired after its rules are reconciled, preserving stricter local authority; it does not erase pending work or make an uncertain receipt complete. Applied-source notes identify the transition and exceptions. Unchanged refresh is a no-op.

After interruption, compare records, snapshots and receipt with actual changes. Report incomplete work until they agree; a receipt cannot manufacture past checks. Missing records, divergent receipts or identical IDs with different bytes require preserving both claims and explicit repair. Reverts are new linked records. Archive/redact only under retention/privacy authority; do not discard history merely because the exact incorporation list grows. Sustained growth and competing consolidators need evaluation; no automatic pipeline is supplied.

## Explanatory Rationale

The exact incorporation set separates historical retention from current corrections: a reversed decision stays accounted for without becoming active again. Ownership-based deferral avoids pretending that a clean worktree detects other contributors. These conventions preserve claims for later reconciliation; they cannot enforce exclusivity or prove that recorded checks were actually run.
