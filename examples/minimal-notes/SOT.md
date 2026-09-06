---
yaiml: 0.2
role: sot
title: SOT
purpose: Current state and direction for the Minimal Notes example.
belongs-here: current product intent, verified behavior, risks, priorities, uncertainty.
not-here: durable architecture, command reference, full history.
durability: volatile; synthesize and prune aggressively.
read-with: Architecture; Maintainer Guide.
update-when: direction, verified behavior, risks, priorities, or useful lessons change.
agent-guidance: Verify claims against files. Preserve human direction. Mark uncertainty. Prune stale detail.
---

# SOT

## North Star

Declared: Minimal Notes is a tiny local note-taking app used to show the smallest useful YAIML shape.

## Current State

Verified: This example contains only YAIML project-memory files. It does not include application source code.

Declared: A real app with this memory would let a person create, edit, search, and delete plain-text notes locally.

## Current Risks

- Unknown: No implementation exists in this example, so no runtime behavior is verified.
- Risk: A future agent could overbuild the example and make it less useful as the minimal path.

## Recent Verified Checks

Verified: The example intentionally contains `yaiml.yml`, `AGENTS.md`, `SOT.md`, `ARCHITECTURE.md`, and `MAINTAINER_GUIDE.md`.

## Immediate Priorities

1. Keep this example small.
2. Use it to show the core YAIML loop without supporting documents.
