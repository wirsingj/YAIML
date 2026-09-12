---
yaiml: 0.2
role: maintainer
title: Maintainer Guide
purpose: Current procedures, commands, diagnostics, and failure playbooks.
belongs-here: setup, commands, tests, build/run flows, debugging paths, important files, operations, release, recovery.
not-here: product intent, durable architecture, complete history.
durability: current-only; remove dead commands and obsolete paths.
read-with: SoT; Architecture.
update-when: commands, setup, diagnostics, release, or recovery procedures change.
agent-guidance: Verify command claims when practical. Mark environment-dependent or unverified procedures.
---

# Maintainer Guide

Adapt these headings; omit empty or irrelevant sections. Keep procedures current and actionable.

## Setup And Commands

Record the shortest useful path from checkout to local work. Identify required tools and environment assumptions.

Separate commands actually run from commands found by source inspection and procedures still unverified. Record the command, outcome, and relevant date, revision, and environment for results that matter. Do not imply a script passed because it exists.

## Focused Checks And Diagnostics

List useful test, build, lint, or diagnostic procedures and how to interpret results. Mark service, hardware, account, or credential requirements without storing sensitive values. Prefer sanitized outcomes to raw logs.

## Important And Dangerous Files

Map files and boundaries a contributor needs before editing; omit a complete file inventory.

## Failure, Release, And Recovery Procedures

For recurring failures, record symptoms, likely owner, evidence to inspect, and recovery steps. Include release, rollback, backup, or restore procedures when applicable, with verification limits.

## YAIML Maintenance

Record the active agent's persistent instruction route and any setup gaps. Routine work updates affected memory without a separate request; respect read-only scope.

For a convention refresh (“update YAIML”), identify a supplied or workspace-local reference and revision; request one if missing. Preserve project knowledge, discovery layout, custom fields, and concurrent edits. Migrate only with explicit authorization and checked compatibility.

For compression (“prune SoT” or “compress YAIML”), replace stale state and repeated history with current understanding. Preserve decisions, evidence limits, unresolved issues, and governed records. Measure affected memory before/after; explain net growth and necessary overages in the task response, not memory. Keep private reference locations out of versioned files.
