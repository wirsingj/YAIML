# YAIML

YAIML preserves the current interpreted understanding of a software project across disposable coding-agent sessions.

The chat can disappear. The provider can change. The agent can change. The project context remains in the repository.

> Coding agents are temporary. The project's engineering understanding should not be.

## Quick Start

Tell your coding agent to initialize YAIML. Paste the contents of [prompts/initialize-yaiml.md](prompts/initialize-yaiml.md) into Codex, Claude, ChatGPT, Cursor, or another repository-aware agent and point it at the project.

The agent should inspect the repository, create the YAIML document family, and populate it with verified current context. It should not change application code during initialization unless you explicitly ask for code changes.

After initialization, start future coding-agent sessions with [prompts/hydrate-agent-session.md](prompts/hydrate-agent-session.md). After meaningful work, use [prompts/update-project-memory.md](prompts/update-project-memory.md).

That is the first usable version of YAIML.

## Manual Setup

If you want to set YAIML up by hand, copy the three core templates into a repository:

```text
SOT.md
ARCHITECTURE.md
MAINTAINER_GUIDE.md
```

`SOT.md` is the neutral starter filename. For a real project, rename it to a project-specific SoT name when there is an obvious larger project word:

- `SoTC.md` for State Of The Captions;
- `SoTT.md` for State Of The Table;
- `SoTY.md` for State Of The YAIML.

The final letter should point to the larger project or product being remembered, not to an arbitrary subsystem like renderer or sidebar.

Add a small `yaiml.yml` that points to the files:

```yaml
yaiml: "0.1"
project:
  id: my-project
  name: My Project
documents:
  sot:
    path: SoTP.md
  architecture:
    path: ARCHITECTURE.md
  maintainer:
    path: MAINTAINER_GUIDE.md
```

## Examples

This repository includes a robust fictional example:

[Canopy Dispatch](examples/canopy-dispatch/) shows a neighborhood storm-response coordination app with SoTD, architecture notes, maintainer playbooks, and release/trust memory.

It is intentionally fake, but detailed enough to show what useful YAIML memory looks like after real engineering pressure: current capabilities, product doctrine, verified evidence, trust risks, architecture boundaries, maintainer checks, and open questions.

## Rights And Reuse

This repository is public for visibility and review, but it is not open source yet.

No open-source license is currently granted. See [LICENSE.md](LICENSE.md). Do not copy, redistribute, repackage, sell, or build derivative works from YAIML without explicit written permission from the copyright holder.

## The Engineering Problem

Modern software work with coding agents happens at two levels:

1. Source code, tests, configuration, and technical artifacts.
2. Continuous natural-language engineering direction: product intent, feature requests, design corrections, audits, bugs found in use, architecture concerns, priorities, rejected directions, and lessons learned.

That second layer can become enormous. Most of the raw conversation should not be preserved forever, but its useful engineering meaning must survive. Otherwise each new Codex, Claude, Cursor, Gemini, or local-model session has to reconstruct the project from source files, stale chat, and guesswork.

YAIML is a lightweight project-context system for that loop.

## Project Layers

YAIML has several layers that should not be collapsed:

- **Philosophy**: coding agents are temporary, but project understanding should persist.
- **Framework**: AI Project Engineering needs durable context for natural-language direction as well as source code.
- **Document family**: SoT, Architecture, Maintainer Guide, and optional supporting documents.
- **Reference kit**: this repository's templates, prompts, guides, examples, and dogfooded YAIML documents.
- **Future tooling**: possible helpers around initialization, discovery, auditing, context assembly, or IDE/agent integration.

## What YAIML Is

YAIML is a lightweight standard and reusable document family for AI Project Engineering.

It is not:

- a YAML format;
- a schema;
- a serialization protocol;
- a conformance system;
- an RFC-style specification;
- a replacement for `AGENTS.md`;
- a generic knowledge base;
- a hosted memory product.

YAIML is semantically structured and syntactically loose. The core roles are stable. The exact filenames, headings, and local vocabulary may vary.

## The Core Workflow

YAIML supports this working loop:

1. The developer describes a goal, concern, bug, correction, or feature.
2. The agent reads the YAIML document family.
3. The agent reconciles the request with current state, architecture, operating guidance, evidence, and uncertainty.
4. The agent inspects the repository.
5. The agent implements, audits, tests, or reports.
6. The agent updates affected YAIML documents so they describe the project after the work.
7. A future agent reads those documents and continues without requiring the old chat.

YAIML documents are not passive documentation after development. They are part of the active engineering process.

## SoT Is The Center

The central YAIML artifact is **SoT**.

SoT means **State Of The**. The phrase is intentionally incomplete; the project completes it.

For a real project, the filename should usually expand with one final project letter:

- `SoTC.md` can mean State Of The Captions.
- `SoTT.md` can mean State Of The Table.
- `SoTY.md` means State Of The YAIML in this repository.

Do not force awkward titles such as `State Of The: Renderer`. SoT should refer to the larger project, product, table, app, world, or other top-level thing whose engineering state is being preserved.

SoT is the project engineering control surface. It synthesizes the active development loop: current product identity, major developer asks, current capabilities, meaningful accomplishments, audit findings, architecture concerns, security and performance risks, testing results, unresolved bugs, known debt, active priorities, corrected directions, and implementation lessons.

It is not merely a changelog, backlog, status report, journal, requirements document, or project plan. It may contain aspects of those, but its job is broader: preserve the project's current engineering state and direction for the next coding agent.

## Supporting Documents

Two supporting roles form the default YAIML family:

- **Architecture** preserves durable system shape, ownership boundaries, intended design, current design, transitional architecture, known debt, and retired approaches.
- **Maintainer Guide** preserves setup, commands, tests, debugging paths, important files, operational procedures, common failures, and recovery steps.

Projects may add documents such as Security, Legal, Data, Testing, UX, Domain, Deployment, Release, Operations, Product Doctrine, World or Lore, Provider Integration, or Remote Access.

Use the documents the project actually needs.

## Stable Headers

Every YAIML document begins with a small stable header. The header orients an unfamiliar coding agent before it reads the body.

The header is not primarily machine metadata. It is not a schema. It is not a rigid form. It should answer:

- what this document is;
- what responsibility it owns;
- what belongs here;
- what does not belong here;
- how durable or volatile it is;
- which related YAIML documents to read;
- when it should be updated;
- how the agent should handle evidence, uncertainty, conflicts, pruning, and human direction.

See [Stable Headers](docs/STABLE_HEADERS.md).

## Authority And Evidence

YAIML must not silently blend different kinds of truth.

- Human direction is authoritative about intended meaning and product direction.
- Code, tests, commands, and runtime behavior are authoritative about what currently exists.
- Agent inference is useful but must stay marked as inference.
- Open questions and disputed claims should remain visible.

When intent and implementation conflict, record the conflict. Do not rewrite intent to match broken code. Do not describe intended behavior as though it already exists.

## Pruning

The goal is useful continuity, not maximum memory.

SoT should synthesize and prune aggressively. It should preserve meaningful accomplishments and important lessons while compressing implementation sediment. Architecture should retain durable decisions and current structure. Maintainer Guides should remove obsolete commands and procedures. Legal, audit, or history documents may require stricter retention.

## Use YAIML Tonight

1. Paste [initialize-yaiml.md](prompts/initialize-yaiml.md) into your coding agent.
2. Let the agent inspect the repository and create the YAIML files.
3. Start later sessions with [hydrate-agent-session.md](prompts/hydrate-agent-session.md).
4. After meaningful work, use [update-project-memory.md](prompts/update-project-memory.md).

No install is required.

## Deferred

Future tooling may include initialization helpers, document discovery, freshness checks, audit assistance, context assembly, IDE integration, agent adapters, document health checks, and provider integrations.

Those tools do not exist here today. This repository is the lightweight document system, templates, prompts, guidance, examples, and YAIML's own dogfood memory.
