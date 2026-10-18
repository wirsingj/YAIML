---
yaiml-revision: "0.1.01b3573c87d5279e"
role: revision-guide
title: Revisions And Change Records
purpose: Connect file revisions, project changes and YAIML releases without losing concurrent contributions.
not-here: Project facts, automatic merge decisions, identity proofs or an executable versioning service.
durability: Durable method; preserve recorded lineage and project retention policy.
update-when: Revision, migration, integration or audit responsibilities change.
agent-guidance: Record actual changes and evidence; never invent missing history or infer authority from a stamp.
---
# Revisions And Change Records

## Three Separate Versions

| Identity | Meaning and owner |
| --- | --- |
| YAIML product release | Published guidance generation in [RELEASE.md](RELEASE.md), with an exact source commit or disclosed snapshot recorded by the adopter |
| Discovery version | The layout label in `yaiml.yml`; preserve it during ordinary content edits |
| Project revision | `x.y.z`: YAIML release major, project-local iteration counter, random change tag |

For example, `0.27.1f463a82b7dc905e` is project iteration 27 using YAIML major 0. It is not product release 0.27, a verification date, or [Semantic Versioning](https://semver.org/). A random final component does not satisfy SemVer's numeric patch rule. Product releases use numeric major/minor/patch labels; document revisions use this separate convention.

Use a fresh 16-character lowercase hexadecimal tag from available cryptographic randomness for each iteration. This short identifier is UUID-like, not a full [UUID](https://www.rfc-editor.org/rfc/rfc9562.html), timestamp, signature or guaranteed unique value. Check known records for collisions. If randomness is unavailable, report revision assignment incomplete instead of fabricating an identifier. No particular language, installed package or service is required.

## Complete One Iteration

An iteration is one coherent, completed change: implementation, documentation, a confirmed conversational decision, an applied refresh, or new evidence that changes recorded understanding. Repeated writes while preparing that change share one revision. Several independent completed tasks may have separate revisions before a commit. Read-only work, unchanged refresh, speculative discussion and rerunning unchanged checks create none.

1. Read the change record's header and current heads; inspect the actual worktree and relevant prior entries. Re-read concurrent edits before writing.
2. Preserve existing facts and perform the authorized change. Reconcile current memory and verification claims in their owners.
3. Allocate `y` as one greater than the highest counter in the known project lineage, initially 1. Use a decimal integer without a fixed width; do not sort it lexically or round it through floating point. Retain the counter across a YAIML major upgrade; `x` follows the applied release major. Source-resource counters belong to the source project and never raise the adopter's counter.
4. Stamp changed YAIML-managed Markdown with the iteration revision. Leave untouched files and their stamps unchanged. Audit affected code, configuration and other project files by path without injecting headers into them.
5. Add one concise entry to the core `changes.md` and update its current heads and own stamp. Include all files actually added, modified, removed or renamed by this iteration, including memory, routes, discovery and the change record itself. Identify unrelated existing work separately; never claim another contributor's edits as this task's work.
6. Check the entry against the final diff and affected stamps. Verification results must name what actually ran and its limits. A check failure is a result, not permission to conceal the change. Report incomplete writes or records honestly.

Use `yaiml-revision: "0.27.1f463a82b7dc905e"` in a memory header. In `SKILL.md`, place that string under frontmatter `metadata` to preserve host-supported fields. For a plain Markdown entry page, prompt or instruction route, use `<!-- yaiml-revision: 0.27.1f463a82b7dc905e -->` outside copyable payloads. Preserve equivalent local metadata when its meaning is clear. This adds no Markdown body schema or parser requirement.

Managed Markdown comprises declared YAIML memory, owned guidance/templates, canonical skills, and YAIML-owned entry pages/routes. Do not stamp unrelated project Markdown merely because it exists. A shared host instruction file can carry a stamp for its YAIML section without claiming ownership of other instructions.

Unmodified acquired resources retain their upstream stamps and exact bytes; source provenance distinguishes them from local revisions. A locally adapted resource receives a local stamp, with the incoming source revision recorded in maintenance guidance and the audit entry. Instantiating a template creates local memory with a local revision; a starter's stamp describes the starter, not the target's history. Preserve legal/notices byte-for-byte when required. Historical examples and compatibility fixtures can retain old formats when clearly labeled. Record these exceptions rather than silently claiming universal stamp coverage.

## Core Change Record

Default to `.yaiml/changes.md`; reuse an existing equivalent audit owner, preserve its entries and retention, or choose a nonconflicting path. Keep SoT, Architecture and Maintainer Guide current and concise. The fourth core role owns a durable audit of changes, not a transcript, command log or second backlog.

Each entry identifies its revision, parent revision(s), date, intent/authorized decision source, concise outcome, affected paths and consequential verification/limitations. Include old and new paths for renames, and mark deletions. An exact commit can be added when known; do not predict the hash of a commit containing the entry. Git supplies exact diffs and ancestry when available; a revision ID is a lookup aid, not a content hash. Without Git, retain the record and state the evidence limits.

Read the header, current heads and relevant recent entries during normal orientation, not the entire accumulated audit. Preserve entries by default. Corrections after a completed iteration get a new linked entry; do not silently rewrite past outcomes. Compression of current memory does not erase the audit. Archive, redact or consolidate records only under the project's explicit retention/privacy authority, preserving traceability and never assuming Git alone satisfies it. Exclude sensitive content from the start.

## Concurrent Work And Integration

Two branches may both produce counter 28 with different tags and the same parent. Neither counter, tag, timestamp nor file order selects the winner. Keep both entries and independent changes. Before integration compare the actual branches and common ancestor, resolve meaning through project authority, and recheck the combined result.

A completed reconciliation creates a revision with a counter above both known lineages and both heads as parents. Stamp files whose final content changed through reconciliation; unchanged imported files retain their existing stamps. Keep imported entries intact and list them as incorporated, without duplicating their file histories. A plain fast-forward retains the existing lineage and needs no synthetic iteration.

Reverts are new changes linked to the reverted revision. Squashing or cherry-picking Git commits must preserve the audit IDs and record consequential integration decisions. If identical IDs describe different changes, retain both claims and resolve the collision with a fresh ID and explicit mapping; do not overwrite one. Interrupted work remains incomplete until the actual files and record agree; a later session repairs the gap without inventing past evidence. These records can inform a future semantic Git tool; no automatic merger or tamper-proof audit is implemented.

## Adopt From Older YAIML

Init/refresh establishes the fourth role and revision tracking in place, without resetting mature knowledge or relocating files. Preserve existing version labels and prior records. If an older local sequence has clear semantics, retain its mapping; otherwise create an explicitly prospective baseline at counter 1 and state that earlier iterations are unknown. Never reinterpret `yaiml: 0.2` or discovery `version` as a file counter.

For each existing managed artifact, inspect its role, header and actual path; preserve its body and legacy labels while adding the baseline stamp in the compatible location. Include local custom skills and YAIML routes; newly acquired, unmodified upstream resources retain their source stamps instead. Record the exact stamped paths, exceptions, preserved audit owner and source release/commit in the baseline entry. Check that no project knowledge disappeared and every changed path is covered. A repeated updater run must leave that baseline and untouched stamps unchanged, rather than start again at 1.

Keep the older discovery shape: add the changes role where compatible (`core.changes` in the current shape, `documents.changes.path` in the recognized legacy shape). When a consumer cannot accept an added role, use an explicit host/maintenance pointer and report that limitation; do not rewrite its format or claim compatibility without checking. A reader that ignores the new role can retain its original functionality without providing audit support; report those separately.
