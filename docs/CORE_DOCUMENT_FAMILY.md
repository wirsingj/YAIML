---
yaiml: 0.2
kind: core-family-guide
title: Core Document Family
purpose: Define the core YAIML document roles and how self-unfolded supporting documents relate to them.
belongs-here: SoT, Architecture, Maintainer Guide responsibilities, supporting document split criteria, fact-placement guidance.
not-here: current project state, command procedures, complete examples, implementation tooling.
durability: durable; update when document responsibilities or split criteria change.
read-with: SoTY; Stable Headers; Pruning And Lifecycle.
update-when: core roles, self-unfolding guidance, or document ownership boundaries change.
agent-guidance: Keep roles semantically firm and syntactically flexible. Avoid creating mandatory document inventories.
---

# Core Document Family

The smallest coherent YAIML core is three roles:

1. SoT
2. Architecture
3. Maintainer Guide

The roles are semantic requirements, not exact templates. A project may rename files, adapt headings, and add local vocabulary, but the responsibilities should remain recognizable.

The core three are the starting spine, not the ceiling. YAIML is a self-unfolding guiding document set for project management, memory, definition, and AI-chat, agent, and contributor continuity.

Use ordinary Markdown files for YAIML documents by default. Do not require a custom `.yaiml` extension. The convention should stay easy to open, diff, preview, edit, and review.

## SoT

SoT is the center of YAIML.

The recommended default filename for unfamiliar repositories is:

```text
SOT.md
```

SoT means **State Of The**. Projects may complete the phrase through the filename when there is an obvious larger project word and the name adds useful project character:

- `SoTC.md`: State Of The Captions
- `SoTT.md`: State Of The Table
- `SoTY.md`: State Of The YAIML

When used, the final letter should refer to the larger project, product, table, app, world, or other top-level thing being remembered. Do not name SoT after a narrow subsystem just because that subsystem is currently being edited.

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
- recent verified checks;
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

SoT should synthesize aggressively. Preserve meaningful accomplishments and lessons, but compress implementation sediment. A small recent-verified-checks section can be useful when it is replaced after new verification; it should not become an append-only test log.

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

It should be actionable, current, and useful to human developers, AI chats, and coding agents.

Wrong or obsolete procedures should be removed quickly.

## Adding Supporting Documents

Add supporting YAIML documents when a memory, rule, definition, risk, preference, or project-management domain would otherwise bloat the core three.

Supporting documents are still source-adjacent project memory by default. Do not use them for raw secrets, credentials, private keys, tokens, passwords, customer personal data, or speculative legal/IP conclusions.

Examples:

- Preferences;
- Security;
- Legal;
- Contracts or Agreements;
- Data;
- Testing;
- UX;
- Domain;
- Concepts;
- Terms or Glossary;
- Risk Review;
- Deployment;
- Release;
- Operations;
- Product Doctrine;
- World or Lore;
- Provider Integration;
- Remote Access;
- API or Integration Notes;
- Accessibility;
- Compliance;
- Decisions;
- Roadmap;
- Migration;
- Performance;
- Observability;
- Support or Triage;
- anything else the project actually needs.

Product Doctrine or a similar supporting document can own product-language decisions when they would otherwise get tangled with architecture. For example, an internal implementation term may remain correct in code while the user-facing product language deliberately uses a different word.

Each supporting document should declare its own responsibility and retention behavior in its stable header.

Do not create supporting documents as empty ceremony. Let the project unfold the set. Split a topic out when it keeps recurring, defines vocabulary, affects risk, preserves preferences, or needs different pruning behavior than SoT, Architecture, or Maintainer Guide.

A useful test: if a proposed document cannot immediately hold several concrete, recurring pieces of project knowledge, it probably should not exist yet.

Every supporting document should improve a future AI chat, coding agent, or contributor's ability to reconstruct the project's current engineering understanding. If it does not, prune, merge, or defer it.

## Context Loading

The core three should remain small enough to load for meaningful work.

Supporting documents should be loaded because the current task touches their domain, not because they exist. A Security Memory document matters for trust boundaries, secret handling, public exposure, or auth work. A Terms document matters for naming and domain distinctions. A Release document matters for rollout, rollback, and readiness work.

Deep references such as audits, decision history, migration records, or release notes should be loaded only when the task needs that history or the human asks for a full review.

## Where Facts Belong

- Current engineering situation belongs in SoT.
- Durable system shape belongs in Architecture.
- How to operate, test, debug, release, or recover belongs in Maintainer Guide.
- Specialized recurring knowledge, definitions, preferences, risks, rules, and doctrine belong in supporting documents when they are large or durable enough to deserve their own home.

If a document starts absorbing another role's job, split or prune it instead of normalizing the blur.
