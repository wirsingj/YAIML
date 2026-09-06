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

YAIML, Yet Another AI Markup Language, is a lightweight plain-file convention and reusable template docset for making a repository understandable and maintainable across humans, AI chats, coding agents, and contributor handoffs.

## Version Awareness

Use `yaiml.yml` as the lightweight discovery protocol when a repository has a YAIML docset.

The file should help an agent identify:

- whether YAIML is present;
- which YAIML discovery layout the docset follows;
- where the core documents live;
- which supporting documents exist;
- whether the discovery file needs a compatibility refresh.

The version describes the discovery format. It is not a Markdown revision counter or a claim that document bodies follow a machine-validatable schema.

The recommended discovery marker is the three-part string `0.2.0`. Roadmap milestones and optional Markdown header hints are separate; neither requires a discovery-version bump. To compare revisions of the reference guidance, use the supplied reference's Git revision or dated snapshot, not the discovery marker alone.

Current recommended shape:

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

Paths are relative to the directory containing `yaiml.yml`, normally the repository root. Use portable paths to files inside the repository. Include only existing supporting documents; omit `supporting` when none are needed. The example's `risk_review` entry is illustrative, not a file to create automatically.

Keep this file portable. Do not store machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs in it.

Future validation, if it exists, should be limited to this small discovery file. YAIML project memory remains human-authored Markdown with stable roles, evidence discipline, and pruning expectations rather than a schema-controlled document body.

## Discovery Layout Compatibility

YAIML consumers should understand the discovery layout used by the target repository before reading or migrating it.

The recommended `0.2.0` layout is shown above.

Recognizable older layout:

```yaml
yaiml: "0.2"
usage: loose-project-memory
documents:
  sot:
    path: STATE_OF_THE_UNION.md
  architecture:
    path: ARCHITECTURE.md
  maintainer:
    path: MAINTAINER_GUIDE.md
supporting:
  - path: docs/YAIML.md
    role: local-usage-guide
```

Safe behavior:

- Read both layouts as discovery hints, not as schemas for the Markdown bodies.
- Prefer the current nested `yaiml.version` / `core` / `supporting` layout for new adopters.
- Preserve mature adopter memory and local SoT names during refreshes.
- Do not silently migrate a repository just because an older recognizable layout is present.
- Do not confuse discovery-format versioning with ordinary Markdown edits. Updating a paragraph in SoT does not require changing the discovery format version.
- Migrate discovery only when the human explicitly requests discovery migration, the consumer understands both layouts, and all local paths and roles can be preserved. A general initialization or refresh request does not authorize migration.
- Repair stale paths within the existing layout. Path repairs do not require a discovery-format version change. If compatibility is unclear, preserve the map and report the gap while completing compatible edits.

For an unfamiliar layout or version, inspect explicit paths and local instructions before interpreting it. Do not guess role mappings, overwrite unknown entries, or downgrade the marker. Report ambiguity that blocks discovery; continue compatible work where possible. No automated consumer compatibility is claimed here.

Compatibility has three separate questions:

| Change | Expected refresh behavior |
| --- | --- |
| Clearer prose, shorter templates, or better evidence guidance | Apply useful guidance to existing memory; no layout or filename migration |
| Local filenames, headings, `role`/`kind` headers | Preserve equivalent local choices and meaningful content |
| Older `documents.*.path` map | Read it and repair paths in place; migration is a separate request |
| Coordinator-specific fields or consumers | Preserve unrelated extensions and check the actual reader before structural or formatting changes |
| Unfamiliar future discovery format | Do not claim compatibility or silently downgrade; report the unresolved mapping |

Reader compatibility is narrower than human readability. A local tool may accept the shown layouts but mishandle different indentation, inline comments, or other valid YAML spellings. Preserve working formatting during routine refresh; test the exact map with its actual consumers before a requested migration. Do not turn a limited reader into a new restriction on Markdown memory.

Future incompatible guidance should explain what changed, what can remain unchanged, and the migration implications before recommending adoption. Existing project knowledge should not need rewriting solely to match a newer template.

## First-Time Adoption

YAIML adoption is evidence-based documentation work, not a generic file-copy operation.

The default adoption route is copy/paste prompt text into the target repository's AI chat. Do not require a download, package install, CLI, or dependency just to start using YAIML.

An adoption agent should:

1. Use the self-contained init prompt; no other download or reference is required. Consult additional guidance only when it is available and relevant.
2. Inspect source, tests, configuration, docs, scripts, visible workflows, and existing agent instructions enough to establish useful project understanding. Bound the inspection and report material areas not inspected.
3. Identify the repository's actual state, architecture, maintainer procedures, risks, and uncertainty.
4. Preserve existing useful project documentation.
5. Select and adapt the appropriate YAIML templates.
6. Create repository-specific documents rather than copying placeholders unchanged.
7. Clearly mark unknowns instead of guessing.
8. Avoid claiming aspirational work is already implemented.
9. Consolidate or reference existing documentation rather than duplicating it unnecessarily.
10. Add or update `yaiml.yml` as a discovery file.
11. Update relevant existing agent instruction files, or create a small provider-neutral `AGENTS.md` when none exist, so future AI chats, agents, and provider modes discover the same YAIML memory.
12. Report which documents were created or modified, what evidence was inspected, what remains uncertain, and what checks were run.

Default core documents are SoT, Architecture, and Maintainer Guide. Supporting documents should be added only when the repository already has several concrete recurring pieces of project knowledge that deserve their own home.

Example prompt:

```text
I want this repository to adopt YAIML. Read the YAIML reference, inspect the repository, create an appropriate repository-specific YAIML docset, preserve existing useful documentation, and do not invent project facts.
```

## Existing YAIML Update

A YAIML update refreshes an adopted YAIML docset to follow newer reference guidance while preserving repository-specific truth.

An update agent should:

1. Read the new YAIML reference source.
2. Read the repository's current YAIML documents.
3. Inspect the current repository implementation enough to distinguish YAIML-reference drift from project-memory drift.
4. Compare the adopted docset against the newer reference.
5. Preserve project-specific SoT, architecture, maintainer knowledge, risks, human decisions, and supporting memory.
6. Update obsolete structure, terminology, headings, responsibilities, and guidance.
7. Add newly recommended sections only when they are relevant.
8. Remove obsolete template residue without removing useful project information.
9. Repair internal links and renamed files.
10. Repair discovery paths in the existing layout; apply the discovery migration policy above before changing formats.
11. Summarize what changed because the YAIML reference changed versus what changed because repository truth had drifted.

Never replace mature repository-specific documents with empty or generic templates.

A repeat refresh with no material guidance or project change should leave files unchanged. Preserve custom fields and working formatting. Remove an obsolete machine-specific reference entry only when its purpose is understood, and repair local instructions that depended on it. Keep reference locations in the human prompt or non-versioned workspace configuration.

Reference guidance is input to review, not authority to copy this repository's own priorities, personal policies, license, or agent permissions into another project. Re-read concurrently changed files before applying edits and preserve unresolved contributor conflicts.

Example prompt:

```text
I have a new version of the YAIML reference at [path]. Review this repository's current YAIML docset, compare it with the newer reference, preserve repository-specific truth and the existing discovery layout, update relevant guidance and internal references, and summarize the update.
```

## Normal Implementation Work

Once YAIML is adopted, routine work should use the docset as repository-carried context.

Example prompt:

```text
Read my request, read the repository's YAIML documents, inspect the relevant implementation, execute the work, update the YAIML documents where project truth changed, verify the result, and report what was done.
```

## Refreshing Multiple Repositories

A coordinator can carry one human request across projects while each repository retains its own memory and rules. YAIML supplies the convention and refresh prompt; it does not supply a dispatcher or automatic migration engine.

1. Select the repositories and one identifiable YAIML reference revision or snapshot. If the reference has uncommitted edits, identify that explicitly; a commit ID alone does not describe them.
2. Inspect each target's current worktree, discovery layout, instruction pointers, and relevant memory. Distinguish convention refresh from a request to audit implementation or pursue SoT priorities.
3. Pass the original request, reference content or accessible location, revision, repository scope, and permitted actions to each receiving agent. Confirm the handoff retains them instead of reducing the request to a generic documentation audit.
4. Apply compatible changes in each repository, preserving local decisions, evidence, paths, layout, custom fields, and unrelated work. Application changes and discovery migration require their own scope.
5. Verify local links, path discovery, instruction integration, and preservation of meaningful memory. Report applied, unchanged, partial, or blocked results per repository. A dispatched task is not a completed upgrade.
6. Commit and push only where authorized. Keep rollback available through ordinary reviewed diffs and commits; never restore whole files over newer contributor work.

Start with one representative project before expanding the batch. Keep private paths and task-routing metadata in the coordinator's appropriate local context. Do not copy the portfolio registry or another project's facts into target memory.
