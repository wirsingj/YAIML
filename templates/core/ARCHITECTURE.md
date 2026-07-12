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

This document preserves design meaning. It should prevent a fresh AI chat, agent, or contributor from treating accidental implementation as intentional architecture.

## System Model

Describe the project at a conceptual level.

## Major Components

List important components and their responsibilities. Do not mirror the whole directory tree.

## Ownership Boundaries

Explain where decisions, data, policy, state, UI, integration, storage, and domain logic belong.

## Current Architecture

Verified implementation shape goes here.

## Intended Architecture

Declared design direction goes here. Mark anything unimplemented clearly.

## Transitional Paths

Describe transitional architecture that is currently true but not the desired endpoint.

## Invariants

List rules that should remain true across changes.

## Known Violations

Record current implementation that violates intended architecture.

## Danger Zones

Name concentrated files, fragile boundaries, security-sensitive areas, generated outputs, or modules that need extra care.

## Retired Approaches

Record approaches that should not quietly return.

## Open Architecture Questions

List unresolved design questions.
