---
yaiml: 0.2
kind: release-trust
title: Canopy Dispatch Release And Trust
purpose: Preserve release gates, privacy posture, trust-sensitive checks, and operational risk notes for the fictional Canopy Dispatch project.
belongs-here: release readiness, privacy gates, data retention concerns, public-output checks, incident-response notes.
not-here: full architecture, current sprint list, ordinary command reference.
durability: current plus audit-sensitive; prune stale mechanics but preserve meaningful trust lessons.
read-with: SoTD; Canopy Dispatch Architecture; Canopy Dispatch Maintainer Guide.
agent-guidance: This is a fictional YAIML example. Never describe a trust-sensitive behavior as released unless implementation evidence supports it.
---

# Canopy Dispatch Release And Trust

## Trust Posture

Canopy Dispatch handles sensitive local information during stressful events. The app should minimize exposure, make responsibility visible, and avoid implying guarantees it cannot make.

## Release Gates

Before a release that changes incident, public status, notification, export, or retention behavior:

- Run incident lifecycle and assignment audit tests.
- Run redaction leakage tests.
- Review public-facing copy for overclaiming.
- Confirm demo data is fictional.
- Update SoTD if active risks or verified capabilities changed.

Before enabling public status:

- Confirm every public card is generated through the redaction boundary.
- Verify exact addresses, names, phone numbers, private notes, and vulnerable-person details are absent.
- Confirm the public page says updates are partial coordination notes, not emergency-service truth.
- Perform a human review with seeded sensitive examples.

## Data Retention Notes

Current fictional default: resolved incidents retain operational timeline and closure outcome, but private notes and contact details are candidates for shorter retention.

Open risk: the retention model is not yet strict enough for real deployment. Treat export, backup, and deletion behavior as release-blocking until reviewed.

## Copy Rules

Use precise words:

- sent: the app requested delivery;
- delivered: provider reports delivery;
- read: responder opened the message, if that signal exists;
- accepted: responder explicitly accepted the assignment.

Do not use delivered, read, or accepted as synonyms.

## Trust Lessons

- A calm interface can still be unsafe if authority is ambiguous.
- Redaction must be a boundary, not a final proofreading step.
- Demo data teaches agents and humans what the product values, so fake data still needs careful shape.
- Notification success is operational evidence, not command authority.
