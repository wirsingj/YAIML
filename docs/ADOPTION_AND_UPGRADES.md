---
yaiml: 0.2
kind: adoption-update-guide
title: YAIML Adoption And Updates
purpose: Define evidence-based first-time adoption, existing YAIML updates, temporary ARCS cleanup, and version marker guidance.
belongs-here: adoption workflow, update workflow, temporary rename cleanup, version marker guidance, practical prompts.
not-here: project-specific state, command procedures, implementation tooling, service design.
durability: durable; update when YAIML adoption, update, or version-awareness guidance changes.
read-with: SoTY; YAIML Architecture; YAIML Maintainer Guide; Core Document Family.
update-when: standard revision markers, adoption expectations, or update rules change.
agent-guidance: Preserve repository-specific truth. Do not replace mature documents with generic templates. Treat YAIML as the canonical name.
---

# YAIML Adoption And Updates

YAIML is a documentation convention and reusable template docset for making a repository understandable and maintainable by humans and AI coding agents.

YAIML was temporarily renamed ARCS and has now returned to its original name. ARCS references should be removed from normal documentation unless they are needed as a short migration note or a temporary deprecated alias for an unmigrated dependent repository.

## Version Awareness

Use `yaiml.yml` as the lightweight discovery marker when a repository has a YAIML docset.

The marker should help an agent identify:

- whether YAIML is installed;
- which YAIML revision or posture the docset follows;
- where the core documents live;
- which supporting documents exist;
- whether a repository still contains temporary ARCS terminology that needs cleanup.

Minimal shape:

```yaml
yaiml: "0.2"

project:
  id: my-project
  name: My Project

documents:
  sot:
    path: SOT.md
    title: SOT
  architecture:
    path: ARCHITECTURE.md
    title: Architecture
  maintainer:
    path: MAINTAINER_GUIDE.md
    title: Maintainer Guide
```

Keep this marker portable. Do not store machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs in it.

## First-Time Adoption

YAIML adoption is evidence-based documentation work, not a generic file-copy operation.

An adoption agent should:

1. Read the YAIML standard, templates, and prompt guidance available to it.
2. Inspect the target repository thoroughly: source, tests, configuration, docs, scripts, visible workflows, and existing agent instructions.
3. Identify the repository's actual state, architecture, maintainer procedures, risks, and uncertainty.
4. Preserve existing useful project documentation.
5. Select and adapt the appropriate YAIML templates.
6. Create repository-specific documents rather than copying placeholders unchanged.
7. Clearly mark unknowns instead of guessing.
8. Avoid claiming aspirational work is already implemented.
9. Consolidate or reference existing documentation rather than duplicating it unnecessarily.
10. Add or update `yaiml.yml` as a discovery marker.
11. Report which documents were created or modified, what evidence was inspected, what remains uncertain, and what checks were run.

Default core documents are SoT, Architecture, and Maintainer Guide. Supporting documents should be added only when the repository already has several concrete recurring pieces of project knowledge that deserve their own home.

Example prompt:

```text
I want this repository to adopt YAIML. Read the YAIML standard, inspect the repository, create an appropriate repository-specific YAIML docset, preserve existing useful documentation, and do not invent project facts.
```

## Existing YAIML Update

A YAIML update refreshes an installed YAIML docset to follow newer reference guidance while preserving repository-specific truth.

An update agent should:

1. Read the new YAIML reference source.
2. Read the repository's current YAIML documents.
3. Inspect the current repository implementation enough to distinguish standard drift from project drift.
4. Compare the installed docset against the newer reference.
5. Preserve project-specific SoT, architecture, maintainer knowledge, risks, human decisions, and supporting memory.
6. Update obsolete structure, terminology, headings, responsibilities, and guidance.
7. Add newly recommended sections only when they are relevant.
8. Remove obsolete template residue without removing useful project information.
9. Repair internal links and renamed files.
10. Update `yaiml.yml` or the repository's documented YAIML revision marker when appropriate.
11. Summarize what changed because the standard changed versus what changed because repository truth had drifted.

Never replace mature repository-specific documents with empty or generic templates.

Example prompt:

```text
I have a new version of the YAIML standard at [path]. Review this repository's current YAIML docset, compare it with the newer standard, preserve repository-specific truth, migrate relevant structural or terminology changes, update internal references, and summarize the update.
```

## Temporary ARCS Cleanup

If a repository was touched during the temporary ARCS rename, clean it back to YAIML in place.

A cleanup agent should:

- identify ARCS-named discovery files such as `arcs.yml`;
- identify ARCS stable-header keys, prompt names, document titles, agent instructions, links, and template names;
- rename them back to YAIML where safe;
- preserve project-specific content;
- update or recreate `yaiml.yml`;
- record the cleanup in the repository's state document when it changes project-maintenance truth;
- avoid installing a second parallel docset.

Keep ARCS references only where they document the temporary rename or a deprecated compatibility alias that still has a named downstream dependency.

Example prompt:

```text
This repository was temporarily migrated from YAIML to ARCS. YAIML is canonical again. Restore YAIML terminology and filenames in place, preserve project-specific content, remove ARCS branding except for a brief migration note, and do not create a second parallel docset.
```

## Normal Implementation Work

Once YAIML is installed, routine work should use the docset as repository-carried context.

Example prompt:

```text
Read my request, read the repository's YAIML documents, inspect the relevant implementation, execute the work, update the YAIML documents where project truth changed, verify the result, and report what was done.
```