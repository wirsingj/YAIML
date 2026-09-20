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

Date: 2026-09-20. Baseline: 4111d4f.

## Findings And Corrections

Reviewed the multi-contributor path across branch work, memory updates, compression, integration, authority, and evidence. The prior guidance protected concurrent edits but did not define how shared memory should be reconciled at PR/MR integration.

- Routine synthesis now edits the smallest coherent affected passages, leaving unrelated structure stable. Broad compression and moves are separately scoped and coordinated.
- Memory describes its checkout; proposals, approved direction, implementation, and deployed behavior remain distinct.
- Integration compares the common ancestor, actual target, and combined implementation/memory. Independent contributions survive; whole-document side selection is rejected.
- Clean merges still need semantic review. Decision conflicts follow existing authority and only dependent work waits for resolution.
- Target advances, reverts, and other integration changes trigger affected-claim checks; prior verification is not promoted to combined-tree success.
- Concurrent writers use separate workspaces or coordinate ownership. Re-reading files does not provide locking.
- Init's persistent pointer, refresh/update/compression prompts, templates, and local instructions carry the relevant behavior. No coordinator, subagent, CI service, schema, or discovery migration was added.

## Verification

Four temporary synthetic three-way merges were executed with Git: independent edits combined cleanly; competing decisions and delete-versus-update produced textual conflicts; different sections containing contradictory direction and shipped-state claims merged cleanly. Assertions checked exit status and retained claims. These demonstrate merge mechanics, not successful autonomous reconciliation.

Temporary inspection passed for 50 Markdown files, 96 local links/anchors, three discovery maps, and 25 declared paths/headers, plus fences, UTF-8, conflict markers, targeted private-path/secret patterns, and whitespace. The scan is not an exhaustive security audit. Core memory remains within its existing budgets. License, discovery map, independence declaration, and dated case studies are unchanged.

## Remaining Limits

Manual instruction-path review also considered unavailable target context, shared checkouts, target advance, reverts, retained evidence and separately scoped compression. Those scenarios were not executed as agent trials. Multi-developer review burden, repeated pruning, fresh-session reliability and total cost remain unmeasured. [Evaluation](EVALUATION.md#concurrent-contributor-check) supplies a bounded next trial.

Current priorities belong in [SoTY](SoTY.md); earlier audit history remains in Git.
