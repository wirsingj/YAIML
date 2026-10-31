---
yaiml: 0.2
role: maintainer
title: Maintainer Guide
purpose: Current procedures for the Minimal Notes example.
belongs-here: checks, maintenance notes, known non-commands.
not-here: product intent, durable architecture, full history.
durability: current-only; remove stale procedures quickly.
read-with: SOT; Architecture.
update-when: example files or maintenance checks change.
agent-guidance: Do not invent commands. Mark unimplemented procedures honestly.
---

# Maintainer Guide

## Quick Start

Read `yaiml.yml`, then read `SOT.md`, `ARCHITECTURE.md`, and this file.

## Verified Commands

None. This example has no package, build, test, or application code.

## Important Files

- `yaiml.yml`: discovery file.
- `AGENTS.md`: tells future agents to read YAIML first.
- `SOT.md`: current project state.
- `ARCHITECTURE.md`: intended system shape.
- `MAINTAINER_GUIDE.md`: this procedural note.

## Maintenance Notes

Keep this example boring. It exists to show that YAIML can be useful before a project needs supporting documents.

For “update YAIML” or “check new YAIML”, compare with a supplied reference while preserving project-specific memory and discovery layout. Do not commit local reference locations.

For “compress YAIML” or “prune SoT”, remove stale or repeated memory while preserving decisions, evidence, and uncertainty. These requests maintain the example; they do not ask for application implementation.
