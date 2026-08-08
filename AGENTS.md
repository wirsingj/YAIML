# Instructions for Agents Working on YAIML

Before making changes:

1. Read `yaiml.yml`.
2. Read the stable header at the top of each declared YAIML document before reading its body.
3. Treat `docs/SoTY.md`, `docs/ARCHITECTURE.md`, and `docs/MAINTAINER_GUIDE.md` as this repository's living project memory.
4. Treat examples, templates, prompts, and guides as supporting artifacts that must stay synchronized with the living-memory concept.

Working rules:

- Preserve the distinction between SoT, architecture, and maintainer procedures.
- Preserve the distinction between declared intent and implementation evidence.
- Treat YAIML as shared project memory for AI chats, coding agents, and human contributors, not private scratch notes for one agent.
- Dogfood YAIML retention and uncertainty rules in this repository.
- Treat natural-language requests such as "continue through the SoT list" or "update our SoT" as instructions to use this repository's YAIML memory, not as requests for separate prompt choreography.
- Treat "update YAIML", "updated YAIML", or "check new YAIML" as convention-refresh language: in adopting repositories, compare local YAIML scaffolding with a human-provided or workspace-local YAIML reference; in this repository, update the reference guidance itself and then update SoTY if the meaning changed.
- Treat "clean up YAIML", "compress YAIML", "compact project memory", "prune project memory", or "prune SoT" as project-memory cleanup/compression language: rewrite affected YAIML documents to remove stale, repetitive, resolved, or log-like content while preserving current truth, human direction, evidence, uncertainty, active risks, and useful lessons.
- Do not commit machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs into YAIML guidance; those belong in the human prompt, agent/workspace configuration, environment, or ignored local notes.
- Do not introduce implementation libraries, CLIs, SDKs, provider adapters, package manifests, schemas for Markdown memory documents, conformance fixtures, or web applications during the convention-first phase.
- Preserve the MIT License unless the maintainer explicitly approves a license change.
- Update only the affected YAIML documents after material changes, prune stale state, and do not append a work diary.
- Report contradictions rather than smoothing them into confident prose.
- Do not describe planned tooling as implemented tooling.
- Do not revive `SPEC.md`, schema-first language for Markdown memory documents, or formal conformance machinery unless a human explicitly changes the project phase.

When updating YAIML documents:

- Read the stable header first.
- Preserve human directives.
- Preserve multi-agent or multi-contributor conflicts until evidence or human direction resolves them.
- Remove resolved active risks from active sections.
- Mark uncertainty honestly.
- Prune before appending if the relevant document is getting bloated.
