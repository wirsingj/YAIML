---
yaiml: 0.2
role: architecture
title: Architecture
purpose: Durable system shape, boundaries, invariants, and intended architecture.
belongs-here: current architecture, intended architecture, ownership boundaries, data flow, invariants, debt, retired approaches.
not-here: current priorities, command reference, complete file inventory.
durability: durable; update when architecture changes materially.
read-with: SoT; Maintainer Guide.
update-when: boundaries, responsibilities, invariants, target architecture, or architectural debt change.
agent-guidance: Distinguish current, intended, transitional, uncertain, and obsolete architecture. Do not treat accidental implementation as design.
---

# Architecture

Adapt these headings; omit empty or irrelevant sections. Explain design meaning so future readers can distinguish intended boundaries from accidental implementation.

## System Model And Components

Describe major components, their responsibilities, and data flow. Do not mirror the whole directory tree.

## Boundaries And Invariants

Explain ownership of decisions, data, state, UI, integrations, and domain logic. Preserve the rules that should survive future changes and their decision sources.

## Current And Intended Architecture

Separate verified implementation from declared design. Include transitional paths, known violations, and unresolved design questions where relevant.

## Danger Zones

Name fragile boundaries, concentrated responsibilities, generated outputs, or sensitive modules that need particular care. Link procedures in the Maintainer Guide.

## Decisions And Retired Approaches

Preserve important rationale and rejected designs that should not quietly return. Remove obsolete detail that no longer affects decisions.
