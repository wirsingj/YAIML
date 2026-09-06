---
yaiml: 0.2
kind: lifecycle-guide
title: Pruning And Lifecycle
purpose: Explain how YAIML documents retain, compress, and forget project memory.
belongs-here: pruning rules, document lifecycles, retention differences, stale-memory guidance.
not-here: current project priorities, command procedures, complete history, legal advice.
durability: durable; update when retention or pruning doctrine changes.
read-with: SoTY; Core Document Family; Ambiguity And Evidence.
update-when: pruning behavior, lifecycle expectations, or supporting-document retention guidance changes.
agent-guidance: Preserve useful continuity without append-only bloat. Keep human-governed retention constraints visible.
---

# Pruning And Lifecycle

Healthy project memory requires forgetting.

An agent-maintained SoT can become valuable because it accumulates understanding from the developer-agent loop. It can also become unusable because it accumulates everything.

YAIML asks agents to rewrite, condense, and remove.

## SoT Lifecycle

SoT should prune aggressively.

Preserve:

- project identity;
- north star;
- active risks;
- current priorities;
- declared human intent;
- current divergence;
- current uncertainty;
- meaningful accomplishments that still describe current capability;
- important lessons that should shape future work;
- recent changes that still affect present reasoning.

Remove or compress:

- resolved risks;
- stale priorities;
- implementation details that no longer affect future work;
- duplicated principles;
- superseded decisions;
- old progress logs;
- completed work recoverable from Git history.

If SoT starts feeling like a diary, prune it.

SoT is allowed to remember accomplishments. It should not remember them as a chronological trophy case. It should synthesize them into current capabilities, active lessons, or changed priorities.

## Cleanup Trigger

Repository agent instructions may define phrases such as "clean up YAIML", "compress YAIML", "compact project memory", "prune project memory", or "prune SoT" as YAIML maintenance requests.

Those phrases should not start feature work, a broad architecture rewrite, or an archive creation pass. They mean: read the YAIML discovery file, inspect the affected memory documents, rewrite stale or repetitive sections, remove resolved active items, and preserve current truth, human direction, evidence, uncertainty, active risk, and useful lessons.

Routine pruning is also expected after material work. A normal SoT update should remove stale or resolved state while recording the new current truth. An explicit compression request is useful when the memory has become repetitive, too large, contradictory, or log-like.

## Architecture Lifecycle

Architecture should remain a coherent model.

Preserve:

- durable ownership decisions;
- system boundaries;
- important invariants;
- transitional architecture while it is still true;
- rejected approaches whose return would be dangerous.

Remove or mark:

- descriptions that are no longer true;
- transitional paths that have ended;
- file-by-file tours that no longer explain meaning;
- architecture debt that has been resolved.

## Maintainer Lifecycle

Maintainer Guide should stay practical and current.

Preserve:

- verified setup and command procedures;
- focused checks;
- diagnostics;
- danger files;
- current failure playbooks;
- release or recovery procedures.

Remove or mark:

- dead commands;
- moved paths;
- obsolete procedures;
- old environment notes that no longer apply;
- historical instructions kept only because they once worked.

## Self-Unfolded Documents

Not every document should prune the same way.

Legal, compliance, audit, contract, agreement, or decision-history documents may require human approval before destructive pruning. Preferences, terms, concepts, risk reviews, product doctrine, world/lore, operations, release, and provider documents may each need different retention rules.

Supporting documents should declare their own lifecycle in the stable header:

- what memory they own;
- what does not belong there;
- whether the content is durable, volatile, governed, or audit-sensitive;
- when stale entries should be removed, compressed, or retained;
- when human approval is needed before pruning.

The principle is not "delete everything." The principle is that each document should know what kind of memory it is.

## Worked Maintenance Examples

These are fictional teaching examples. Compression may shorten supplied evidence, but must not add facts, rationale, scope, or verification that it does not establish.

### Human Decision Supersedes Earlier Decision

Before:

```text
Declared: The app should support both local files and cloud sync.
```

New evidence:

```text
Human decision on 2026-09-05: keep v1 local-only; cloud sync is deferred.
```

Correct current state:

```text
Declared (maintainer decision, 2026-09-05): v1 is local-only; cloud sync is deferred, superseding the earlier local-and-cloud direction.
Unknown: the decision does not state a rationale.
Retired for now: do not add sync plumbing unless the maintainer reopens that decision.
```

Preserve a supplied rationale when it helps prevent repeated mistakes. Do not invent one to explain a decision.

### Assumption Is Disproven

Before:

```text
Inferred: `settings-store.js` probably stores recent documents in browser storage.
```

New evidence:

```text
Verified by source inspection: `settings-store.js` writes UI preferences only. Other storage paths have not been inspected.
```

Correct current state:

```text
Verified by source inspection: `settings-store.js` writes UI preferences only.
Obsolete: the inference that this module stores recent documents was disproven.
Unknown: whether any other path persists document text.
```

Do not rewrite the old inference as if it had always been verified history.

### Resolved Risk Leaves Active Sections

Before:

```text
Active risk: release packages may include local diagnostic screenshots.
```

New evidence:

```text
Verified on 2026-09-05 at fictional revision abc123, local Windows build: release sanity passed; inspection of the generated source ZIP found no `tests/artifacts/` entries. Package script inspection confirmed that exclusion.
```

Correct current state:

```text
Recent verification (abc123, local Windows build, 2026-09-05): release sanity passed; generated source ZIP inspection found no `tests/artifacts/` entries. Recheck after packaging changes.
Useful lesson: keep diagnostic artifacts ignored and out of source packages.
```

Remove the item from Active Risks unless a related risk still exists.

### Compression Preserves An Easily Lost Constraint

Before:

```text
2026-08-01: fixed the language fallback.
2026-08-03: tested Korean auto-translate.
2026-08-08: adjusted fallback again.
```

With only these entries, the compressed state is:

```text
Unknown: notes report language-fallback changes and a Korean auto-translate check, but record neither expected behavior nor test outcome. Inspect the decision, implementation, and check evidence before relying on them.
```

Now suppose a product decision is also available:

```text
Maintainer decision D-7: preferred-language fallback must not present original-language text as a successful translation. Use live/current captions or a clear unavailable state if translated timedtext fails.
```

Then preserve the constraint without inventing verification:

```text
Declared (D-7): failed translated timedtext must fall back to live/current captions or a clear unavailable state, never original-language text presented as a successful translation.
Unknown: the old work-log entries do not establish whether implementation meets D-7 or any check passed.
```

The run history can remain in Git. Retain the decision reference and verification gap in current memory.

### Git Merge Succeeds But Memory Contradicts Itself

Merged text:

```text
Declared: the app is YouTube-only for v1.
Verified: generic video support is shipped in release manifests.
```

Correct current state:

```text
Disputed: project memory says v1 is YouTube-only, while another edit claims generic video support is shipped.
Evidence to inspect: release manifests, release checklist, and the human decision that set v1 scope.
Unknown until inspected: whether the release boundary changed or the second claim is wrong.
```

Do not smooth the contradiction into one confident paragraph just because Git merged without conflict.
