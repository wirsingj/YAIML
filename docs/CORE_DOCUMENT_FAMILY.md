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

YAIML starts with three distinct roles, normally in three Markdown documents. Reuse existing files that already serve those roles; local filenames and headings may vary.

A default filename is not permission to replace unrelated content. Choose a nonconflicting path and record it in discovery. When adapting a template into new memory, set a role-appropriate word budget; existing equivalent headers remain valid.

| Role | Owns | Does not own |
| --- | --- | --- |
| SoT | Current identity, human direction, capabilities, risks, priorities, verification limits, divergence, useful lessons | Full history, command reference, durable component model |
| Architecture | Components, data flow, ownership, invariants, current and intended design, relevant rejected approaches | Current task list, procedures, full file inventory |
| Maintainer Guide | Setup, commands, checks, diagnostics, environment assumptions, release and recovery | Product manifesto, architecture rationale, run history |

## SoT

SoT means **State Of The**. Use `SOT.md` by default. Project-specific names such as `SoTC.md` (State Of The Captions) or this repository’s `SoTY.md` (State Of The YAIML) are also supported. Name it for the whole project, not the current subsystem or task.

Keep the current engineering situation readable. Completed work belongs as present capability or a lesson that still changes decisions. A recent-verification summary may record consequential checks with their scope; replace it when superseded instead of appending a test log.

Human direction and verified behavior should remain distinguishable. [Ambiguity And Evidence](AMBIGUITY_AND_EVIDENCE.md) explains how to preserve disagreement.

## Architecture

Explain where responsibilities live and why important boundaries exist. Separate current, intended, transitional, uncertain, and retired architecture.

A known implementation violation belongs beside the relevant design boundary. Retain rejected designs only when the reason still helps prevent their accidental return.

## Maintainer Guide

Give the next contributor actionable procedures and the assumptions they depend on. Distinguish source-defined commands from successfully executed checks; include conditions and limits for results that matter.

Remove dead commands and obsolete paths. Link detailed operational references rather than copying them into several documents.

## Adding Supporting Documents

Split a topic out when recurring knowledge would bloat the core, needs a distinct owner, or follows a different retention rule. Security constraints, domain vocabulary, product principles, and release procedures are common examples; the list is open.

A supporting document should immediately hold concrete useful knowledge. Do not create files just because a template exists. Each document’s [stable header](STABLE_HEADERS.md) explains its responsibility, exclusions, and lifecycle.

Keep brief summaries or pointers in the core when readers need awareness of a specialist constraint. Let the supporting document own the detail. Product language, for example, can differ deliberately from internal code terminology; a product document can preserve that decision without duplicating architecture.

## Keeping The Family Small

Read the core for meaningful work and supporting material when task-relevant. Deep history should not become default context; see [Context Loading](CONTEXT_LOADING.md).

Adapt templates as writing aids. Remove empty headings and consolidate overlapping sections. A template’s possible sections are not a required inventory.

Write for a person returning to the project as well as an agent: explain project-specific terms on first use, use short connected prose, and link evidence without turning every sentence into metadata. A small project can start with a few useful sections per document.

When a fact changes, update its owning document and any consequential summary or pointer. Prefer links over repeated explanations. Follow [Pruning And Lifecycle](PRUNING_AND_LIFECYCLE.md), including any governed retention rules.
