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

“Update YAIML”, “updated YAIML”, or “check new YAIML” means compare local convention guidance, prompts, templates, and instruction pointers against a human-provided or workspace-local reference. Preserve project memory and existing discovery layout; migrate only on explicit request with compatibility established.

“Clean up YAIML”, “compress YAIML”, “compact project memory”, “prune project memory”, or “prune SoT” means remove stale, repeated, resolved, or log-like content while preserving current truth, human direction, evidence, uncertainty, active risks, and useful lessons. Respect governed retention rules.

Keep machine-specific reference paths and private workspace URLs out of versioned files. If a refresh reference is unavailable, request one rather than guessing.
