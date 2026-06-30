---
yaiml: 0.1
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

YAIML is a lightweight project-context system for AI Project Engineering.

Its architecture is conceptual rather than software-based. The repository supplies guides, templates, prompts, examples, and dogfood memory documents. The artifacts are meant to work in any Git repository with any capable coding agent.

## Core Roles

SoT owns current engineering state: identity, active developer direction, current capabilities, active priorities, active risks, useful recent lessons, current divergence, and unresolved questions.

Architecture owns durable project self-model: components, ownership boundaries, invariants, intended architecture, transitional paths, violations, and retired approaches.

Maintainer Guide owns procedural memory: setup, commands, diagnostics, focused checks, danger files, and failure playbooks.

The roles should remain separate. SoT should not become a command reference. Architecture should not become a work log. Maintainer Guide should not become a product manifesto.

## Artifact Responsibilities

- `README.md` introduces the problem and immediate use path.
- `docs/` explains the convention and hosts YAIML's own living documents.
- `templates/core/` provides starter versions of the three required roles.
- `templates/optional/` provides examples for supporting memory documents.
- `prompts/` provides provider-neutral operating procedures.
- `examples/canopy-dispatch/` demonstrates a robust fictional YAIML family with product doctrine, authority boundaries, operational playbooks, and release/trust memory.
- `docs/COLD_START_REVIEW.md` records the latest manual cold-start usability pass.
- `yaiml.yml` discovers YAIML's own memory documents.

## Stable Header Boundary

The stable header is an agent-facing orientation block, not a validation schema.

It should be consistent enough for agents to recognize and flexible enough for projects to adapt. Future tooling may parse it, but current design should optimize for a model opening the file and understanding how to use the prose that follows.

Firm bones: role, authority, evidence, update trigger, pruning behavior, conflict behavior, and human authority.

Soft edges: exact field names, phrasing, document title, local vocabulary, optional sections, and project-specific retention details.

## Optional Documents

Supporting documents may exist when a project has a memory domain that would otherwise bloat the core family. Examples include security, domain model, data model, UX doctrine, legal, release guide, or remote access.

Optional documents must declare what memory they own and how they prune. They do not become mandatory just because they are useful somewhere.

## Deferred Tooling

Deferred:

- CLI;
- parser;
- validator;
- SDK;
- package format;
- hosted service;
- provider adapters;
- IDE integrations;
- schema or conformance fixtures.

Future tools should serve the convention. They should not redefine YAIML as a technical-document standard.

## Retired Approaches

Retired for the current phase:

- `SPEC.md` as normative center;
- JSON Schema as a primary project artifact;
- conformance fixture directories;
- RFC-style requirement language;
- treating YAIML as a schema or package format.

These should not return unless a human explicitly changes the project phase.
