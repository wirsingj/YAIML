# Update YAIML Convention Files

You are an AI coding assistant in a repository that already uses YAIML.

The human may say this as "update YAIML", "YAIML is updated", "run an update on our YAIML", or "refresh our YAIML setup".

## Goal

Refresh the repository's YAIML convention scaffolding against a newer YAIML reference while preserving the repository's own project memory.

This is not the same as updating the project's SoT after ordinary work. Do not rewrite project-specific current state, architecture, maintainer knowledge, risks, or priorities just because the YAIML reference changed.

YAIML remains plain Markdown with a discovery map. Do not add runtime infrastructure, packages, CLIs, or Markdown schema/conformance tooling. Do not change application code, install dependencies, or run expensive checks solely for a convention refresh.

## Before Editing

1. Read repository agent instructions first, such as `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, contribution docs, or workspace notes.
2. Read `yaiml.yml`.
3. Read the stable headers for the core YAIML documents before their bodies.
4. Check the current git status or equivalent worktree state. Treat existing uncommitted changes as intentional work in progress.
5. Identify the repository's current YAIML discovery layout before editing. Current recommended layouts use nested `yaiml.version`, `core`, and `supporting`; older recognizable layouts may use `documents.sot.path`, `documents.architecture.path`, and `documents.maintainer.path`.
6. Do not reset, discard, overwrite, or hide existing work.

Resolve discovery paths before following them. A map or symlink does not authorize access outside the target repository. Use only references authorized by the request or workspace context.

## Find The YAIML Reference

Use the first available source:

1. A path or URL the human provided in the request.
2. A per-workspace or per-agent configuration value that is not committed to the repository.
3. A nearby local YAIML reference repository if recent agent context clearly identifies one.

If no YAIML reference can be identified, do not guess. Report that a reference path or URL is needed.

Do not write machine-specific filesystem paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs into versioned YAIML files. They are per-workspace/per-agent context, not project memory.

If the human wants a durable team-wide reference later, use a stable, team-approved public reference in versioned guidance. Keep private workspace references in non-versioned configuration. Do not invent a reference URL. Do not fetch from the network unless the environment allows it and the human request or existing non-versioned workspace context makes the source clear.

## Compare

Identify the supplied reference revision or dated snapshot when available; the discovery marker alone cannot identify a prose revision. Start with its init prompt and adoption/upgrade guidance, then compare the target's existing instruction pointers and maintenance notes. If the previously applied reference is known, use the relevant changes between references to focus inspection.

Read other reference prompts, templates, and topic guides only when the target keeps copies or a material difference needs clarification. Do not load the entire reference inventory or create local copies merely to compare them. Stop when applicable differences are addressed or explicitly unresolved; an identical reference still needs local drift checked, not a wholesale reread.

Do not assume every adopting project should copy the reference repository wholesale. Look for convention changes that improve continuity, safety, clarity, or agent behavior.

Treat the reference as convention guidance, not permission to override the target's rules. Do not import the reference project's own facts, personal policies, license choice, or agent permissions. If the reference includes uncommitted edits, record that the commit ID alone does not identify it.

## Apply

Apply only updates that are useful and compatible with this repository:

- update local YAIML prompts if this repository keeps copies;
- update local YAIML templates if this repository keeps copies;
- update agent-instruction pointers when the current YAIML guidance has changed;
- update `yaiml.yml` only as a small discovery file, not as a schema, database, or place for machine-specific reference paths;
- migrate discovery layout only when the human explicitly requests discovery migration, the consumer understands both layouts, and all local paths and roles can be preserved; a general refresh request does not authorize migration;
- repair stale paths within the existing layout; ordinary Markdown edits and path repairs do not require a discovery-format version change;
- preserve unrelated custom fields and working formatting; exercise the actual consumer before a requested migration, since readable YAML is not proof that a tool recognizes it;
- remove obsolete machine-specific reference entries when their purpose is clear and repair instructions that relied on them;
- update the repository's own YAIML documents only when the refresh changes how future AI chats, agents, or contributors should understand or maintain this repository.

Preserve project-specific memory. Do not replace:

- SoT current state;
- architecture facts;
- maintainer commands;
- project-specific risks;
- human decisions;
- local naming choices;
- recognizable older discovery layouts unless migration meets the explicit-request and compatibility conditions above;
- supporting documents that contain real project knowledge.

Re-read files changed since inspection before writing; preserve concurrent edits and unresolved conflicts. Update existing instruction pointers rather than appending duplicates. If nothing material needs changing, leave the files alone. Do not mark a partial refresh as fully applied.

For a coordinated batch, each receiving agent needs the original refresh request, the selected reference revision/content or accessible location, target scope, and permitted actions. Verify those survive the handoff. Record completion per repository; queued or dispatched work is not an upgrade result.

## Safety Rules

- Do not store secrets, credentials, tokens, private keys, passwords, customer personal data, private chat transcripts, raw sensitive logs, sensitive raw values, exploit details, or confidential information in YAIML.
- Do not store machine-specific YAIML reference paths or local workspace URIs in versioned YAIML files.
- Do not invent legal, IP, licensing, security, privacy, or compliance conclusions.
- Do not change the project license.
- Do not create new supporting documents unless the project already has several concrete recurring pieces of knowledge that need that home.
- Do not make broad stylistic rewrites.
- Do not describe planned YAIML tooling as implemented.
- Preserve applicable copyright and permission notices on copied reference material.
- Leave commits and pushes to the authorization supplied for the target repositories.

## Output

Report:

- YAIML reference source used, or that none was found;
- current local YAIML version or posture, if identifiable;
- reference YAIML version or posture, if identifiable;
- files compared;
- files changed;
- project-specific memory intentionally preserved;
- incompatible or skipped reference changes, with reasons;
- risks or uncertainty left for the human;
- checks run and whether they passed.
