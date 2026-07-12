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

Record inspection commands and how to read their output. Prefer sanitized outcomes over raw output that contains secrets, personal data, private paths, private URLs, or confidential details.

## YAIML Maintenance

Phrases such as "update YAIML", "updated YAIML", "check new YAIML", or "run a YAIML update" mean to compare this repository's local YAIML prompts, templates, guidance, and agent-instruction pointers against a human-provided or workspace-local YAIML reference while preserving project-specific SoT, Architecture, Maintainer Guide, and supporting memory.

Do not hardcode machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs in versioned YAIML files. If no reference is available from the human prompt or local workspace context, ask for one instead of guessing.

## Failure Playbooks

### Symptom

Likely owner:

Inspect:

Run:

Common fix direction:

## Release And Recovery

Record current release, rollback, backup, restore, or deployment procedures if they exist.

## Unverified Procedures

List procedures that need validation before a future AI chat or agent relies on them.
