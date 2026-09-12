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

Pruning is part of each material memory update, not a later cleanup phase. A document below its word budget can still contain unnecessary history.

## SoT Lifecycle

Before writing, identify what changed and where that fact already lives:

1. Replace its existing account with current understanding rather than adding a dated update.
2. Remove superseded claims and resolved risks or priorities in the affected sections. Preserve relevant decision sources and unresolved disagreements.
3. Keep completed work only when it describes a current capability, a constraint or decision still in force, or a lesson that changes a future action.
4. Keep one detailed home per fact. Replace duplicates with a short pointer when readers need awareness.
5. Read the result as someone starting the next task. Remove content that only explains what this session did.

A useful lesson names the condition and the action it changes. “Reviewed documentation” is history; “After renaming a core document, repair discovery and instruction links” can be a useful procedure. Put it in the role that owns it.

Do not preserve every dated result as “evidence.” Keep the consequential current result and its limits; retain older results only when they explain an active regression, decision, or governed record. Let committed history retain superseded detail. Never claim that editing a summary revalidated its contents.

## Cleanup Trigger

“Clean up YAIML”, “compress YAIML”, “compact project memory”, “prune project memory”, and “prune SoT” request the same synthesis over the selected documents. They do not authorize feature changes or new archives.

During ordinary work, clean affected sections; an explicit compression request can justify a wider pass. Respect read-only scope. Re-read concurrent changes and confirm detail is committed or otherwise safely retained before relying on history. Removing sensitive text does not erase prior exposure; see [Security](../SECURITY.md).

## Word Budgets

Choose targets by role and reading frequency. Preserve local budgets and equivalent prose; do not pad text or inflate a target to fit existing bloat. Count whole-document whitespace-delimited words, including headers, unless the local budget specifies otherwise.

Measure affected documents before and after editing. Compress safely first; necessary new knowledge and governed retention may justify growth. Report net growth with the knowledge that requires it, and any overage with a scoped next action. Put these measurements in the task response, not another historical section in memory. Do not load unrelated files merely to count them.

A budget is a review threshold, not a deletion quota. Preserve human direction, current facts, consequential evidence, uncertainty, unresolved conflicts, and governed records even when an overage remains. Inherited overgrowth does not authorize a bulk rewrite during initialization.

## Instructions That Generate Bloat

Look for competing instructions that route every observation into an inbox, append a session summary, or preserve every completed item. Resolve their authority before changing them; relocation into the Maintainer Guide does not fix an instruction that still accumulates history.

A prior local review recorded both frequent-update growth and infrequent-update role drift. Those observations motivate checking the update rule itself; they do not prove that one instruction always wins or that a budget prevents recurrence. [SoTY](SoTY.md) retains the unresolved evidence questions.

Replace accumulation rules with the synthesis steps above, then compress within scope. A short current priority list can belong in SoT; an ever-growing completed-task list does not. Do not open new “lessons,” “verification,” or supporting documents just to relocate a diary.

## Architecture Lifecycle

Keep the current and intended system model, active transitions, invariants, and useful decision rationale. Remove ended transitions and obsolete component tours. Retain rejected designs only while their rationale helps prevent a concrete mistake. [Core Document Family](CORE_DOCUMENT_FAMILY.md) owns role boundaries.

## Maintainer Lifecycle

Keep actionable procedures and their assumptions. Replace dead commands, moved paths, and obsolete recovery steps; do not accumulate execution logs. Link current evidence when needed rather than copying the same result from SoT.

## Self-Unfolded Documents

Split only concrete recurring knowledge that needs its own responsibility or retention rule. Splitting does not itself reduce total memory.

Legal, compliance, audit, contract, incident, or decision-history records may require retention or human approval before destructive pruning. Follow their declared lifecycle and review rules. Preserve required records in their authorized home; do not apply volatile SoT rules to them.

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
