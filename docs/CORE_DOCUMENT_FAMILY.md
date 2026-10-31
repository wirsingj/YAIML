---
yaiml-revision: "0.47.a709c1ceed90c210"
yaiml: 0.2
kind: core-family-guide
title: Core Document Family
purpose: Define the core YAIML document roles and how self-unfolded supporting documents relate to them.
belongs-here: SoT, Architecture, Maintainer Guide and changes responsibilities, supporting document split criteria, fact-placement guidance.
not-here: current project state, command procedures, complete examples, implementation tooling.
durability: durable; update when document responsibilities or split criteria change.
read-with: Concepts; Stable Headers; Pruning And Lifecycle.
update-when: core roles, self-unfolding guidance, or document ownership boundaries change.
agent-guidance: Keep roles semantically firm and syntactically flexible. Avoid creating mandatory document inventories.
---

# Core Document Family

YAIML starts with four distinct core roles, normally in four Markdown documents: three current-memory owners and a retained change record. Reuse existing files that already serve those roles; local filenames and headings may vary.

Skills are reusable methods for working with this memory family. They read current project facts rather than owning competing copies. Shared operating rules, dormant templates and optional coordination guidance support those methods; they are not additional project-state documents. Add a specialist fact owner or project-specific skill only when recurring knowledge or work gives it a concrete purpose.

Project memory describes the work; it is not a replacement home for the work itself. Product documentation, examples, specifications and other deliverables stay in their normal project locations. Discovery can link to those authoritative artifacts without moving or copying them into `.yaiml/`. A Markdown header or revision stamp does not determine which side of that boundary a document belongs on.

New memory and reusable guidance use the established memory home, otherwise project-root `.yaiml/`; later specialist documents follow it. Preserve existing locations unless [re-init relocation](ADOPTION_AND_UPGRADES.md#default-placement) is confirmed; keep discovery/host instruction routes. A default directory or filename grants no overwrite or relocation permission. Inspect collisions, choose a nonconflicting path and record it in discovery. Set role-appropriate budgets for new memory; existing equivalent headers remain valid.

| Role | Owns | Does not own |
| --- | --- | --- |
| SoT | Current identity, human direction, capabilities, risks, priorities, verification limits, divergence, useful lessons | Full history, command reference, durable component model |
| Architecture | Components, data flow, ownership, invariants, current and intended design, relevant rejected approaches | Current task list, procedures, full file inventory |
| Maintainer Guide | Setup, commands, checks, diagnostics, environment assumptions, release and recovery | Product manifesto, architecture rationale, run history |
| changes.md | Completed iterations, parents, intent, affected paths and scoped verification | Transcripts, raw logs, current backlog, duplicated current facts |

## SoT

SoT means **State Of The**. Use `SOT.md` within the chosen memory home, defaulting to `.yaiml/SOT.md`. Project-specific names such as `SoTC.md` (State Of The Captions) or this repository’s `SoTY.md` (State Of The YAIML) are also supported. Name it for the whole project, not the current subsystem or task.

Keep the current engineering situation readable. Completed work belongs as present capability or a lesson that still changes decisions. A recent-verification summary may record consequential checks with their scope; replace it when superseded instead of appending a test log.

Human direction and verified behavior should remain distinguishable. [Ambiguity And Evidence](AMBIGUITY_AND_EVIDENCE.md) explains how to preserve disagreement.

## Architecture

Explain where responsibilities live and why important boundaries exist. Separate current, intended, transitional, uncertain, and retired architecture.

A known implementation violation belongs beside the relevant design boundary. Retain rejected designs only when the reason still helps prevent their accidental return.

## Maintainer Guide

Give the next contributor actionable procedures and the assumptions they depend on. Distinguish source-defined commands from successfully executed checks; include conditions and limits for results that matter.

Remove dead commands and obsolete paths. Link detailed operational references rather than copying them into several documents.

## Changes

Use `.yaiml/changes.md` or an established audit owner. [Versioning](../reference/VERSIONING.md) defines local stamps and lineage; [Change Records](../reference/CHANGE_RECORDS.md) defines retained records, pending context and consolidation. This fourth role locates records and their incorporation receipt, preserving older inline entries. The other three owners synthesize current truth when task ownership permits; pending corrections supplement them until then. Repair navigation immediately. Read the receipt and pending records routinely, deep history selectively. Retain records unless explicit retention/privacy authority permits a traceable correction or archival.

## Adding Supporting Documents

Split a topic out when recurring knowledge would bloat the core, needs a distinct owner, or follows a different retention rule. Security constraints, domain vocabulary, product principles, and release procedures are common examples; the list is open.

A supporting document should immediately hold concrete useful knowledge. Do not create files just because a template exists. Each document’s [stable header](STABLE_HEADERS.md) explains its responsibility, exclusions, and lifecycle.

Keep brief summaries or pointers in the core when readers need awareness of a specialist constraint. Let the supporting document own the detail. Product language, for example, can differ deliberately from internal code terminology; a product document can preserve that decision without duplicating architecture.

## Keeping The Family Small

Read the core for meaningful work and supporting material when task-relevant. Deep history should not become default context; see [Context Loading](CONTEXT_LOADING.md).

Adapt templates as writing aids. Remove empty headings and consolidate overlapping sections. A template’s possible sections are not a required inventory.

Write for a person returning to the project as well as an agent: explain project-specific terms on first use, use short connected prose, and link evidence without turning every sentence into metadata. A small project can start with a few useful sections per document.

When a fact changes, update its owning document and any consequential summary or pointer. Prefer links over repeated explanations. Follow [Pruning And Lifecycle](PRUNING_AND_LIFECYCLE.md), including any governed retention rules.
