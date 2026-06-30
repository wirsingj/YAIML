---
yaiml: 0.1
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

This document is procedural memory. Keep it current and practical.

## Quick Start

Record the shortest verified path from checkout to useful local work.

## Verified Commands

```sh
# Add verified commands here.
```

## Environment-Dependent Commands

List commands that depend on local services, secrets, hardware, accounts, or optional tools.

## Focused Checks

List narrow test, lint, typecheck, build, or diagnostic commands.

## Important Files

Map files and directories an agent should know before editing.

## Danger Files

List files where changes are high-risk, generated, security-sensitive, large, or easy to misuse.

## Diagnostics

Record inspection commands and how to read their output.

## Failure Playbooks

### Symptom

Likely owner:

Inspect:

Run:

Common fix direction:

## Release And Recovery

Record current release, rollback, backup, restore, or deployment procedures if they exist.

## Unverified Procedures

List procedures that need validation before a future agent relies on them.
