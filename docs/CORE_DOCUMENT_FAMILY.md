# Core Document Family

The smallest coherent YAIML core is three roles:

1. SoT
2. Architecture
3. Maintainer Guide

The roles are semantic requirements, not exact templates. A project may rename files, adapt headings, and add local vocabulary, but the responsibilities should remain recognizable.

## SoT

SoT is the center of YAIML.

The neutral starter filename is:

```text
SOT.md
```

SoT means **State Of The**. In a real project, complete the phrase through the filename when there is an obvious larger project word:

- `SoTC.md`: State Of The Captions
- `SoTT.md`: State Of The Table
- `SoTY.md`: State Of The YAIML

The final letter should refer to the larger project, product, table, app, world, or other top-level thing being remembered. Do not name SoT after a narrow subsystem just because that subsystem is currently being edited.

SoT preserves the current engineering state and direction of the project. It may include:

- overall goal;
- current product identity;
- major feature requests;
- developer asks;
- meaningful accomplishments;
- current capabilities;
- active work;
- audit findings;
- architecture concerns;
- security and performance risks;
- testing findings;
- unresolved bugs;
- known debt;
- active priorities;
- near-term goals;
- rejected or corrected directions;
- implementation lessons;
- areas needing inspection.

It is not merely:

- a changelog;
- a backlog;
- a task list;
- a project plan;
- a status report;
- a journal;
- a requirements document.

SoT should synthesize aggressively. Preserve meaningful accomplishments and lessons, but compress implementation sediment.

## Architecture

Architecture preserves durable structural understanding.

It should explain:

- current system shape;
- intended system shape;
- major modules;
- boundaries and ownership;
- data flow;
- authority and responsibility;
- important architectural decisions;
- transitional architecture;
- known architecture debt;
- retired or rejected designs;
- danger zones;
- where future work should live.

It should distinguish current, intended, transitional, uncertain, and obsolete architecture.

Architecture should not become a complete file index or a work log.

## Maintainer Guide

Maintainer Guide preserves practical operating knowledge.

It should explain:

- setup;
- commands;
- tests;
- build and run flows;
- debugging paths;
- important files;
- operational procedures;
- release procedures;
- common failures;
- recovery steps;
- environment assumptions.

It should be actionable, current, and useful to both a human developer and a coding agent.

Wrong or obsolete procedures should be removed quickly.

## Adding Supporting Documents

Add supporting YAIML documents when a memory domain would otherwise bloat the core three.

Examples:

- Security;
- Legal;
- Data;
- Testing;
- UX;
- Domain;
- Deployment;
- Release;
- Operations;
- Product Doctrine;
- World or Lore;
- Provider Integration;
- Remote Access.

Each supporting document should declare its own responsibility and retention behavior in its stable header.

## Where Facts Belong

- Current engineering situation belongs in SoT.
- Durable system shape belongs in Architecture.
- How to operate, test, debug, release, or recover belongs in Maintainer Guide.
- Specialized recurring knowledge belongs in a supporting document.

If a document starts absorbing another role's job, split or prune it instead of normalizing the blur.
