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
