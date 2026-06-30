---
yaiml: 0.1
kind: sot
title: SoTD
purpose: Preserve the current engineering state, product direction, active risks, and next priorities for the fictional Canopy Dispatch project.
belongs-here: current product identity, verified capabilities, recent lessons, active risks, audit findings, near-term priorities, open questions, human directives.
not-here: complete changelog, durable component model, command reference, full release checklist.
durability: volatile; keep current, synthesize aggressively, remove stale risks when resolved.
read-with: Canopy Dispatch Architecture; Canopy Dispatch Maintainer Guide; Release And Trust.
update-when: product direction, risk posture, implementation evidence, or immediate priorities materially change.
agent-guidance: This is a fictional YAIML example. Keep human intent separate from implementation evidence. Mark uncertainty. Do not promote planned behavior to verified behavior.
---

# SoTD

## North Star

Canopy Dispatch is a fictional neighborhood storm-response coordination app. It helps a small volunteer team intake requests, assign responders, track safety status, and publish limited public updates during power, tree, water, or supply disruptions.

The product should feel calm under pressure: fewer tabs, fewer mystery states, clear ownership, and no accidental exposure of private household details.

## Current Concept

Declared: Canopy Dispatch is not a 911 replacement, city emergency system, social feed, surveillance tool, or volunteer marketplace. It is a lightweight coordination board for known community organizers and invited responders.

Verified in this fictional example: the repository contains an operator dashboard, responder mobile view, incident timeline, mock notification adapter, seed data, and tests for assignment, status transitions, and redaction behavior.

Unverified: the external SMS provider, map geocoding, and public status page are represented by adapters and fixtures, but they have not been exercised against live services.

## Current Capabilities

- Intake forms create incident cards with urgency, location hint, contact preference, and privacy notes.
- Coordinators can assign one primary responder and multiple watchers.
- Responders can mark en route, on scene, blocked, resolved, or needs escalation.
- Incident timelines preserve important state changes and coordinator notes.
- Public updates intentionally redact names, exact addresses, phone numbers, and private notes.
- A local demo mode can run from seeded storm scenarios.

## Recent Human Direction

- Prefer trust and clarity over automation.
- Do not optimize for dispatch speed if the result makes responsibility ambiguous.
- Public pages should communicate area-level status, not household-level details.
- Keep responder workflows usable on a wet phone in bad lighting.
- Treat notification delivery as helpful but never as the source of truth.

## Meaningful Accomplishments

- The app now has one incident state machine instead of scattered status strings.
- Assignment logic records who changed ownership and why.
- Public redaction has tests around address, contact, and note leakage.
- The demo dataset now includes blocked-road, welfare-check, supply-drop, and duplicate-report scenarios.
- The maintainer guide distinguishes demo commands from production release checks.

## Active Risks

- Notification delivery failures are visible in logs but not yet summarized in the coordinator UI.
- Duplicate incidents can still fragment attention during a fast-moving storm.
- The responder view has not been tested enough on small screens with long location descriptions.
- The app stores sensitive contact details, so export, backup, and retention behavior need stricter review.
- The fictional public status page exists in concept and test fixtures, but not as a verified deployed surface.

## Current Priorities

1. Add a coordinator-visible notification health panel.
2. Improve duplicate incident detection without auto-merging private reports.
3. Audit mobile layout with long names, long streets, and low-connectivity banners.
4. Review retention rules for contact details and private notes.
5. Keep the public-status work behind explicit release review until redaction is verified end to end.

## Known Divergence

Human intent says notification delivery must not become the source of truth. Some UI copy still implies that a sent message means a responder definitely received the assignment. That copy needs correction.

The architecture says all public output should pass through the redaction boundary. A helper in the mock public feed still formats incident summaries directly for tests. It should either move behind the redaction helper or be deleted.

## Testing State

Passing in the fictional repository:

- incident state-machine tests;
- assignment audit-log tests;
- public redaction unit tests;
- coordinator dashboard smoke test with seeded incidents.

Not yet proven:

- real notification provider behavior;
- public status deployment;
- offline recovery after browser refresh;
- accessibility pass for responder mobile controls.

## Open Questions

- Should duplicate detection suggest a merge, link related incidents, or only warn coordinators?
- How long should Canopy Dispatch retain resolved private notes by default?
- Should responders see exact household contact information before accepting an assignment?
- Is public status useful enough to justify the risk and maintenance cost?
