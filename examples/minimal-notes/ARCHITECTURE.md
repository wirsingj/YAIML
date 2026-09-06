---
yaiml: 0.2
role: architecture
title: Architecture
purpose: Durable architecture understanding for the Minimal Notes example.
belongs-here: intended shape, boundaries, invariants, rejected complexity.
not-here: current priorities, command reference, complete history.
durability: durable; update when the intended example shape changes.
read-with: SOT; Maintainer Guide.
update-when: boundaries, responsibilities, or rejected approaches change.
agent-guidance: Distinguish intended architecture from implemented reality.
---

# Architecture

## System Model

Intended: Minimal Notes would be a single-user local application with note data stored on the user's machine.

Verified: This example does not implement that application. It only demonstrates the YAIML memory shape.

## Boundaries

- UI would own note editing and search interactions.
- Storage would own local note persistence.
- Search would read note text and return matching note identifiers.

## Invariants

- Notes should remain local by default.
- The example should not introduce accounts, sync, cloud storage, or AI features.

## Retired Approaches

- Do not turn this example into a full sample application.
- Do not add supporting YAIML documents unless the example stops being minimal.
