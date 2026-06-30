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

## Optional Documents

Not every document should prune the same way.

Legal, compliance, audit, or decision-history documents may require human approval before destructive pruning. Supporting documents should declare their own lifecycle in the stable header.

The principle is not "delete everything." The principle is that each document should know what kind of memory it is.
