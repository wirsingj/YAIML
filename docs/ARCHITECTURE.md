---
yaiml: 0.2
kind: architecture
title: YAIML Architecture
purpose: Preserve YAIML's durable conceptual model, artifact boundaries, and deferred tooling boundaries.
belongs-here: conceptual architecture, artifact responsibilities, role boundaries, deferred approaches.
not-here: current priorities, command procedures, complete file inventory.
durability: durable; update when roles, artifact responsibilities, or deferred tooling boundaries change.
read-with: SoTY; YAIML Maintainer Guide.
agent-guidance: Verify repository shape before claiming artifacts. Surface conflicts. Preserve human direction.
---

# YAIML Architecture

## System Model

YAIML is an incubating plain-file convention and reusable template docset for AI Project Engineering.

Its architecture is conceptual rather than software-based. The repository supplies guides, templates, prompts, examples, and dogfood memory documents. The artifacts are meant to work in any Git repository with capable AI chats, coding agents, and human contributors.

The convention is the primary artifact. Documents, templates, prompts, examples, and future helpers exist to preserve current engineering understanding across chats, agents, and contributors; they are not independent mechanisms to expand for their own sake.

YAIML may later have better init helpers, but the architectural target remains plain files in the user's project. A helper may create, discover, review, refresh, or assemble YAIML context; it should not make the adopting project depend on YAIML as a runtime library, package-manager dependency, hosted platform, or build step.

YAIML documents should remain normal Markdown files by default, not a custom `.yaiml` extension. The visible, boring file format is part of the architecture: it keeps the memory editable by humans, readable by generic tools, reviewable in Git, and accessible to capable agents and AI chats. `yaiml.yml` may discover the family, but it is not the product center or a schema.

## Core Roles

SoT owns current engineering state: identity, active developer direction, current capabilities, active priorities, active risks, useful recent lessons, current divergence, and unresolved questions. `SOT.md` is the recommended default filename for unfamiliar repositories; project-specific names are supported when useful.

Architecture owns durable project self-model: components, ownership boundaries, invariants, intended architecture, transitional paths, violations, and retired approaches.

Maintainer Guide owns procedural memory: setup, commands, diagnostics, focused checks, danger files, and failure playbooks.

Supporting documents own self-unfolded memory domains: preferences, legal, contracts or agreements, concepts, terms, risk review, security, data, testing, UX, domain, deployment, release, operations, product doctrine, world or lore, provider integration, remote access, and other project-specific guidance as needed.

The roles should remain separate. SoT should not become a command reference. Architecture should not become a work log. Maintainer Guide should not become a product manifesto.

## Artifact Responsibilities

- Root files handle public entry, agent instructions, licensing, sensitive reporting, contribution guardrails, roadmap, and discovery.
- `README.md` introduces the problem and immediate use path for humans deciding whether to adopt YAIML.
- `docs/` explains the convention and hosts YAIML's own living documents.
- `templates/core/` provides starter versions of the three required roles.
- `templates/supporting/` provides examples for supporting memory documents.
- `prompts/init-yaiml.md` provides the smallest useful adoption path.
- `prompts/initialize-yaiml.md` provides the deeper self-contained initialization path.
- `prompts/` also provides provider-neutral hydration, memory update, YAIML update, audit, pruning, and realignment procedures.
- `examples/canopy-dispatch/` demonstrates a robust fictional YAIML family with product doctrine, authority boundaries, operational playbooks, and release/trust memory.
- `docs/COLD_START_REVIEW.md` records the latest manual cold-start usability pass.
- `docs/AGENT_INTEGRATION.md` explains how YAIML relates to `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, and similar files.
- `docs/CONTEXT_LOADING.md` defines bounded context-loading layers.
- `docs/EVALUATION.md` defines a lightweight case-study and cold-start comparison method.
- `docs/ADOPTION_AND_UPGRADES.md` defines first-time adoption, existing YAIML updates, and version awareness.
- `yaiml.yml` discovers YAIML's own memory documents.

## Context Loading Boundary

YAIML uses layered context loading:

- discovery: `yaiml.yml` and repository agent instructions;
- core: SoT, Architecture, and Maintainer Guide;
- task-relevant: supporting documents selected because the task touches their domain;
- deep-reference: historical decisions, audits, release notes, or specialized material loaded only when needed.

Supporting documents should not recursively require the entire family without reason.

## Stable Header Boundary

The stable header is an agent-facing orientation block, not a validation schema.

It should be consistent enough for agents to recognize and flexible enough for projects to adapt. Future tooling may parse it, but current design should optimize for a model opening the file and understanding how to use the prose that follows.

Firm bones: role, authority, evidence, update trigger, pruning behavior, conflict behavior, and human authority.

Soft edges: exact field names, phrasing, document title, local vocabulary, optional sections, and project-specific retention details.

## Self-Unfolding Documents

Supporting documents may exist when a project has a memory domain that would otherwise bloat the core family or needs different retention behavior. Examples include preferences, legal, contracts or agreements, concepts, terms, risk review, security, domain model, data model, testing, UX doctrine, deployment, release, operations, product doctrine, world or lore, provider integration, or remote access.

Self-unfolded documents must declare what memory they own and how they prune. They do not become mandatory just because they are useful somewhere.

## Deferred Tooling

Deferred:

- CLI;
- parser;
- validator;
- SDK;
- package format;
- package-manager dependency;
- runtime library;
- database or storage layer;
- orchestration framework;
- background service;
- custom `.yaiml` document format;
- hosted service;
- provider adapters;
- IDE integrations;
- schema or conformance fixtures.

Future tools should serve the convention. They should not redefine YAIML as a technical-document standard.

Addition test: if a new artifact does not improve a future AI chat, coding agent, or contributor's ability to reconstruct a project's current engineering understanding, it probably does not belong in YAIML.

## Retired Approaches

Retired for the current phase:

- `SPEC.md` as normative center;
- JSON Schema as a primary project artifact;
- conformance fixture directories;
- RFC-style requirement language;
- treating YAIML as a schema or package format.
- requiring a custom file extension for project memory.

These should not return unless a human explicitly changes the project phase.
