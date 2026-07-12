# Update YAIML Convention Files

You are an AI coding assistant in a repository that already uses YAIML.

The human may say this as "update YAIML", "YAIML is updated", "run an update on our YAIML", or "refresh our YAIML setup".

## Goal

Refresh the repository's YAIML convention scaffolding against a newer YAIML reference while preserving the repository's own project memory.

YAIML is the canonical project and standard name. If the repository still contains temporary ARCS terminology, clean it back to YAIML in place.

This is not the same as updating the project's SoT after ordinary work. Do not rewrite project-specific current state, architecture, maintainer knowledge, risks, or priorities just because the YAIML reference changed.

YAIML remains plain Markdown and YAML project memory. Do not add a package dependency, CLI, runtime, schema validator, database, storage layer, orchestration framework, hosted service, background service, autonomous coding agent, or build step.

## Before Editing

1. Read repository agent instructions first, such as `AGENTS.md`, `CLAUDE.md`, `.cursorrules`, contribution docs, or workspace notes.
2. Read `yaiml.yml`; if only `arcs.yml` exists, read it as a temporary ARCS-era discovery file to migrate back to YAIML.
3. Read the stable headers for the core YAIML documents before their bodies.
4. Check the current git status or equivalent worktree state. Treat existing uncommitted changes as intentional work in progress.
5. Do not reset, discard, overwrite, or hide existing work.

## Find The YAIML Reference

Use the first available source:

1. A path or URL the human provided in the request.
2. A per-workspace or per-agent configuration value that is not committed to the repository.
3. A nearby local YAIML reference repository if recent agent context clearly identifies one.

If no YAIML reference can be identified, do not guess. Report that a reference path or URL is needed.

Do not write machine-specific filesystem paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs into versioned YAIML files. They are per-workspace/per-agent context, not project memory.

If the human wants a durable team-wide reference later, record only a stable, team-approved public or internal project reference. Until then, keep local paths in the prompt, local agent memory, environment, or ignored workspace notes. Do not invent a reference URL. Do not fetch from the network unless the environment allows it and the human request or existing non-versioned workspace context makes the source clear.

## Compare

Inspect the reference repository or reference files for:

- README front-door guidance;
- `prompts/init-yaiml.md`;
- `prompts/initialize-yaiml.md`;
- `prompts/hydrate-agent-session.md`;
- `prompts/update-project-memory.md`;
- `prompts/audit-against-reality.md`;
- `prompts/prune-sot.md`;
- `prompts/major-project-realignment.md`;
- `prompts/update-yaiml.md`, if present;
- core templates;
- supporting templates;
- docs that define evidence, context loading, stable headers, agent integration, pruning, safety, licensing posture, adoption, upgrade, legacy migration, version awareness, or evaluation.

Do not assume every adopting project should copy the reference repository wholesale. Look for convention changes that improve continuity, safety, clarity, or agent behavior.

## Apply

Apply only updates that are useful and compatible with this repository:

- update local YAIML prompts if this repository keeps copies;
- update local YAIML templates if this repository keeps copies;
- update agent-instruction pointers when the current YAIML guidance has changed;
- update `yaiml.yml` only as a small discovery file, not as a schema, database, or place for machine-specific reference paths;
- migrate `arcs.yml`, ARCS stable-header keys, prompt filenames, document titles, and links back to YAIML naming when present;
- update the repository's own YAIML documents only when the refresh changes how future AI chats, agents, or contributors should understand or maintain this repository.

Preserve project-specific memory. Do not replace:

- SoT current state;
- architecture facts;
- maintainer commands;
- project-specific risks;
- human decisions;
- local naming choices;
- supporting documents that contain real project knowledge.

Do not install a second YAIML docset beside temporary ARCS-era files. Rename and update the existing docset in place.

## Safety Rules

- Do not store secrets, credentials, tokens, private keys, passwords, customer personal data, private chat transcripts, raw sensitive logs, sensitive raw values, exploit details, or confidential information in YAIML.
- Do not store machine-specific YAIML reference paths or local workspace URIs in versioned YAIML files.
- Do not invent legal, IP, licensing, security, privacy, or compliance conclusions.
- Do not change the project license.
- Do not create new supporting documents unless the project already has several concrete recurring pieces of knowledge that need that home.
- Do not make broad stylistic rewrites.
- Do not describe planned YAIML tooling as implemented.

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
