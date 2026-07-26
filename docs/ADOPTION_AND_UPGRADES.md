---
yaiml: 0.2
kind: adoption-update-guide
title: YAIML Adoption And Updates
purpose: Define evidence-based first-time adoption, existing YAIML updates, and discovery-protocol guidance.
belongs-here: adoption workflow, update workflow, discovery-protocol guidance, practical prompts.
not-here: project-specific state, command procedures, implementation tooling, service design.
durability: durable; update when YAIML adoption, update, or version-awareness guidance changes.
read-with: SoTY; YAIML Architecture; YAIML Maintainer Guide; Core Document Family.
update-when: discovery protocol, adoption expectations, or update rules change.
agent-guidance: Preserve repository-specific truth. Do not replace mature documents with generic templates. Treat YAIML as the canonical name.
---

# YAIML Adoption And Updates

YAIML is a lightweight plain-file convention and reusable template docset for making a repository understandable and maintainable across humans, AI chats, coding agents, and contributor handoffs.

## Version Awareness

Use `yaiml.yml` as the lightweight discovery protocol when a repository has a YAIML docset.

The file should help an agent identify:

- whether YAIML is installed;
- which YAIML discovery layout the docset follows;
- where the core documents live;
- which supporting documents exist;
- whether the discovery file needs a compatibility refresh.

The version belongs to the discovery protocol and reference posture. It is not a claim that every Markdown document body follows a machine-validatable schema.

Minimal shape:

```yaml
yaiml:
  version: "0.2.0"
  core:
    state: SOT.md
    architecture: ARCHITECTURE.md
    maintainer_guide: MAINTAINER_GUIDE.md
  supporting:
    risk_review: docs/RISK_REVIEW.md
```

Keep this file portable. Do not store machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs in it.

Future validation, if it exists, should be limited to this small discovery file. YAIML project memory remains human-authored Markdown with stable roles, evidence discipline, and pruning expectations rather than a schema-controlled document body.

## First-Time Adoption

YAIML adoption is evidence-based documentation work, not a generic file-copy operation.

An adoption agent should:

1. Read the YAIML reference, templates, and prompt guidance available to it.
2. Inspect the target repository thoroughly: source, tests, configuration, docs, scripts, visible workflows, and existing agent instructions.
3. Identify the repository's actual state, architecture, maintainer procedures, risks, and uncertainty.
4. Preserve existing useful project documentation.
5. Select and adapt the appropriate YAIML templates.
6. Create repository-specific documents rather than copying placeholders unchanged.
7. Clearly mark unknowns instead of guessing.
8. Avoid claiming aspirational work is already implemented.
9. Consolidate or reference existing documentation rather than duplicating it unnecessarily.
10. Add or update `yaiml.yml` as a discovery file.
11. Report which documents were created or modified, what evidence was inspected, what remains uncertain, and what checks were run.

Default core documents are SoT, Architecture, and Maintainer Guide. Supporting documents should be added only when the repository already has several concrete recurring pieces of project knowledge that deserve their own home.

Example prompt:

```text
I want this repository to adopt YAIML. Read the YAIML reference, inspect the repository, create an appropriate repository-specific YAIML docset, preserve existing useful documentation, and do not invent project facts.
```

## Existing YAIML Update

A YAIML update refreshes an installed YAIML docset to follow newer reference guidance while preserving repository-specific truth.

An update agent should:

1. Read the new YAIML reference source.
2. Read the repository's current YAIML documents.
3. Inspect the current repository implementation enough to distinguish YAIML-reference drift from project-memory drift.
4. Compare the installed docset against the newer reference.
5. Preserve project-specific SoT, architecture, maintainer knowledge, risks, human decisions, and supporting memory.
6. Update obsolete structure, terminology, headings, responsibilities, and guidance.
7. Add newly recommended sections only when they are relevant.
8. Remove obsolete template residue without removing useful project information.
9. Repair internal links and renamed files.
10. Update `yaiml.yml` when the discovery protocol or paths changed.
11. Summarize what changed because the YAIML reference changed versus what changed because repository truth had drifted.

Never replace mature repository-specific documents with empty or generic templates.

Example prompt:

```text
I have a new version of the YAIML reference at [path]. Review this repository's current YAIML docset, compare it with the newer reference, preserve repository-specific truth, migrate relevant structural or terminology changes, update internal references, and summarize the update.
```

## Normal Implementation Work

Once YAIML is installed, routine work should use the docset as repository-carried context.

Example prompt:

```text
Read my request, read the repository's YAIML documents, inspect the relevant implementation, execute the work, update the YAIML documents where project truth changed, verify the result, and report what was done.
```
