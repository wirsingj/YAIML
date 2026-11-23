<!-- yaiml-revision: 0.62.ea5e56759cd3932d -->
# A Current Memory Example

This fictional workshop shows how the four current memory roles fit together. These are annotated excerpts, not a complete installation, an executed init result or evidence that an agent remembered anything. Use [full init](../../reference/prompts/init-yaiml.md) or [offline init](../../reference/prompts/init-yaiml-offline.md) to establish actual project files; do not copy these fictional facts into a real project.

## The Human Brief

> Plan a community workshop for no more than thirty attendees. Keep afternoons free. Use Hall B, but its booking is not confirmed. Prepare a schedule; do not book anything.

The brief authorizes planning. Selecting a venue does not establish a reservation or authorize payment. Those distinctions should survive the next conversation.

## Four Different Jobs

### SOT.md — What Is True Now?

```markdown
# Workshop State

Include pending corrections from changes.md.

## Direction
Confirmed: cap attendance at thirty; keep afternoons free.
Confirmed: plan around Hall B. Booking is still unconfirmed.

## Current State
The brief exists. No completed schedule or reservation evidence exists.

## Next Work
Draft a morning-only schedule for review against the brief.
Obtain venue availability through an authorized channel before treating it as booked.
```

This is current understanding, not a record of every venue discussed. If the human later selects Hall C, current direction changes while the earlier decision remains in the retained audit.

### ARCHITECTURE.md — What Holds The Plan Together?

```markdown
# Planning Structure

Include pending corrections from changes.md.

The brief owns the attendance and timing constraints.
The schedule owns session timing; venue correspondence owns booking evidence.
Human approval governs changes to constraints and any reservation.

Keep intended arrangements distinct from confirmed external commitments.
```

A non-code project still has responsibilities and boundaries. It does not need invented software components.

### MAINTAINER_GUIDE.md — How Do We Work And Check?

```markdown
# Working Procedures

Include pending corrections from changes.md.

Before revising a schedule, read the current constraints and venue status.
Check every proposed session ends before noon and the attendance limit
is preserved. These are planned checks; no schedule has been checked yet.

Record booking confirmation only when supporting correspondence exists.
Follow the installed YAIML_GUIDE.md for memory maintenance and records.
```

Procedures describe how to check; completed results belong with the actual evidence. A list of checks is not a passing result.

### changes.md — What Was Recorded, And What Is Pending?

The audit points to a record directory and lists exact incorporated record IDs. Each record preserves authority, outcome, checks, limits and affected paths. Real setup allocates its own revision and initial record; this excerpt supplies no fictional revision to reuse.

Suppose a later human decision changes the venue to Hall C. With sole ownership, the agent updates current memory and records the change in the same iteration. During overlapping work, it preserves the correction in a pending record until reconciliation. A reader must include pending records before answering which venue is current; reading SOT alone may miss the change.

The older record remains retained. A new decision does not turn yesterday's accurately recorded decision into an error to erase.

## What A Complete Setup Adds

Actual files have populated role headers and revision stamps. A discovery map locates all four owners; supported host instructions point sessions to the operating guide. Full setup also installs local methods, their required resources and notice. The offline prompt supplies its embedded guidance and notice without acquiring skills. This page intentionally omits that setup machinery rather than pretending the excerpts are ready to install.

## Check Understanding

A reader should recover thirty attendees, free afternoons, Hall B as intended venue, an unconfirmed booking and an unfinished schedule. They should not claim a reservation, completed verification or permission to make a purchase.

For a behavioral trial, initialize an isolated project from the brief, then ask a separate authorized fresh session: “What can we rely on for this workshop, and what still needs checking?” Compare its answer with the brief and actual files. Report assistance, missed context and unavailable access honestly. Reading this page or manually constructing these excerpts is not that trial.
