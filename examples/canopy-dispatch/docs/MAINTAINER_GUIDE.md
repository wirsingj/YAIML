---
yaiml: 0.2
kind: maintainer
title: Canopy Dispatch Maintainer Guide
purpose: Preserve current setup, commands, focused checks, debugging paths, and failure playbooks for the fictional Canopy Dispatch project.
belongs-here: verified commands, local setup, testing procedures, diagnostics, important files, operational playbooks.
not-here: product vision, durable architecture rationale, full release history.
durability: current-only; remove stale commands and obsolete paths quickly.
read-with: SoTD; Canopy Dispatch Architecture; Release And Trust.
agent-guidance: This is a fictional YAIML example. Treat commands as example project commands, not commands for the YAIML repository itself. Verify before trusting in a real project.
---

# Canopy Dispatch Maintainer Guide

## Quick Start

This fictional project has a normal application runtime and a seeded demo mode. In a real repository, verify every command before preserving it here.

## Common Commands

Install dependencies:

```powershell
npm install
```

Run the local demo:

```powershell
npm run dev -- --seed storm-demo
```

Run focused tests:

```powershell
npm test -- incident-state assignment-audit redaction
```

Run mobile layout checks:

```powershell
npm run test:viewport -- responder
```

Build a release candidate:

```powershell
npm run build
```

## Focused Reviews

Run these after meaningful changes:

- Compare `docs/SoTD.md` with changed product behavior and remove resolved active risks.
- Check that public output still flows through the redaction boundary.
- Review notification copy for language that confuses sent, delivered, read, and accepted.
- Test responder screens with long incident titles, long street names, and offline banners.
- Confirm demo data does not include real names, phone numbers, or addresses.

## Important Files

- `docs/SoTD.md`: current state, risks, priorities, and known divergence.
- `docs/ARCHITECTURE.md`: durable system shape and privacy boundaries.
- `docs/RELEASE_AND_TRUST.md`: release gates, privacy posture, and trust checks.
- `src/incident/`: fictional incident lifecycle and assignment logic.
- `src/redaction/`: fictional public-output boundary.
- `src/notifications/`: fictional delivery adapters and failure recording.
- `tests/fixtures/storm-demo/`: fictional seeded scenarios.

## Diagnostics

When assignment behavior looks wrong:

1. Check the incident timeline before reading UI state.
2. Confirm the latest assignment event has actor, timestamp, and reason.
3. Verify notification attempts did not overwrite assignment truth.

When public output looks too detailed:

1. Search for direct formatting of private incident records.
2. Confirm the redaction helper is used.
3. Add or update a leakage test before changing display copy.

When responders report stale state:

1. Check whether the coordinator board shows a newer event.
2. Compare local field status with timeline events.
3. Review notification health before assuming acceptance failed.

## Failure Playbooks

### Public Status Leaks Private Data

Symptoms:

- exact address appears publicly;
- resident name or phone appears publicly;
- private coordinator note appears publicly.

Begin here:

1. Disable public status publication.
2. Find the rendering path that bypassed redaction.
3. Add a redaction test reproducing the leak.
4. Update `docs/SoTD.md` and `docs/RELEASE_AND_TRUST.md` with the incident and follow-up risk.

### Notification Provider Fails During A Storm

Symptoms:

- assignment notifications show repeated failures;
- responders report no messages;
- coordinator dashboard still shows assignments as if delivery succeeded.

Begin here:

1. Treat coordinator assignment state as authoritative.
2. Surface failed delivery attempts to coordinators.
3. Use manual contact fallback.
4. Do not mark assignments accepted unless the responder explicitly accepts.

### SoT Becomes A Chronological Log

Symptoms:

- completed tasks overwhelm active risks;
- fixed bugs remain in active priorities;
- current direction is hard to find.

Begin here:

1. Preserve human directives, current capabilities, active risks, divergence, and immediate priorities.
2. Compress old accomplishments into a few durable lessons.
3. Move durable structural learning into Architecture if it belongs there.
