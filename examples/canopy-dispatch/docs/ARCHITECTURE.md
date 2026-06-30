---
yaiml: 0.1
kind: architecture
title: Canopy Dispatch Architecture
purpose: Preserve the durable system model, ownership boundaries, invariants, and intended direction for the fictional Canopy Dispatch project.
belongs-here: component responsibilities, data flow, trust boundaries, current and intended architecture, retired approaches, architecture debt.
not-here: current sprint priorities, command reference, complete incident history, release checklist.
durability: durable; update when ownership boundaries, trust boundaries, or major system shape changes.
read-with: SoTD; Canopy Dispatch Maintainer Guide; Release And Trust.
agent-guidance: This is a fictional YAIML example. Separate implemented structure from intended structure. Flag any privacy boundary violation clearly.
---

# Canopy Dispatch Architecture

## System Model

Canopy Dispatch is organized around a coordinator-owned incident board.

The coordinator dashboard is the authority surface for intake, assignment, escalation, redaction review, and incident closure. The responder surface is a constrained field workflow. The public surface, if enabled, is a redacted read-only projection.

## Core Components

- Incident core: owns incident identity, lifecycle states, priority, assignment, and audit trail.
- Coordinator dashboard: owns triage, assignment, filtering, duplicate review, and operational visibility.
- Responder view: owns accepted assignments, status updates, blocked reasons, and field notes.
- Notification adapter: sends outbound messages and records delivery attempts, but does not own assignment truth.
- Redaction boundary: converts private incident records into safe public summaries.
- Demo data: provides believable storm scenarios for onboarding, tests, and screenshots.

## Data Flow

1. Intake creates a private incident.
2. Coordinator triage assigns priority and ownership.
3. Assignment creates an audit event and may request notification delivery.
4. Responder status updates append to the timeline.
5. Closure records outcome and retention category.
6. Optional public output is generated only through the redaction boundary.

## Invariants

- Private incident records must never be rendered by the public status surface directly.
- Notification delivery does not prove responder acceptance.
- Every assignment change needs actor, timestamp, and reason.
- Closure should preserve enough context for audit without retaining unnecessary private details forever.
- Field workflows should favor explicit statuses over freeform interpretation.

## Current Architecture

Verified in this fictional example: incident lifecycle and assignment logic are centralized. Redaction exists as a named helper with unit tests. Notification delivery is represented by a mock adapter. Coordinator and responder views share incident summaries but do not share all private fields.

Known gap: a mock public feed test helper formats incident summaries without using the redaction helper. It is test-only, but it weakens the architecture story and should be corrected.

## Intended Architecture

The intended architecture keeps three authority layers separate:

- private operations: full incident records for coordinators;
- responder operations: assignment-specific details needed for field action;
- public awareness: redacted area-level status only.

Future notification providers, map services, exports, or public pages should attach through these boundaries instead of reaching into private records directly.

## Retired Approaches

- Freeform status labels were retired in favor of one incident lifecycle.
- Auto-merging duplicate reports was rejected because it can hide conflicting safety information.
- Public household-level cards were rejected because the privacy risk was larger than the coordination value.

## Architecture Watchpoints

- Any new public-facing feature must prove it uses the redaction boundary.
- Any new notification behavior must show coordinator-visible failure states.
- Any new mobile workflow must be tested with long text and poor connectivity states.
- Any export feature must state retention, audience, and redaction behavior before implementation.
