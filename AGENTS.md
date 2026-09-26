# Instructions for Agents Working on YAIML

Before making changes:

1. Read `yaiml.yml`.
2. Read the three core documents below and task-relevant supporting material. For each selected YAIML document, read its stable header before its body; `read-with` is a relevance hint, not a recursive loading requirement.
3. Treat `docs/SoTY.md`, `docs/ARCHITECTURE.md`, and `docs/MAINTAINER_GUIDE.md` as this repository's living project memory.
4. Treat examples, templates, prompts, and guides as supporting artifacts that must stay synchronized with the living-memory concept.

Working rules:

- Preserve the distinction between SoT, architecture, and maintainer procedures.
- Preserve the distinction between declared intent and implementation evidence.
- Treat YAIML as shared project memory for AI chats, coding agents, and human contributors, not private scratch notes for one agent.
- Use "Yet Another AI Markup Language" as YAIML's intended expansion.
- Dogfood YAIML retention and uncertainty rules in this repository.
- Treat natural-language requests such as "continue through the SoT list" or "update our SoT" as instructions to use this repository's YAIML memory, not as requests for separate prompt choreography.
- Treat "update YAIML", "updated YAIML", or "check new YAIML" as convention-refresh language: in adopting repositories, compare local YAIML scaffolding with a human-provided or workspace-local YAIML reference; in this repository, update the reference guidance itself and then update SoTY if the meaning changed.
- Treat "clean up YAIML", "compress YAIML", "compact project memory", "prune project memory", or "prune SoT" as project-memory cleanup/compression language: rewrite affected YAIML documents to remove stale, repetitive, resolved, or log-like content while preserving current truth, human direction, evidence, uncertainty, active risks, and useful lessons.
- Treat older recognizable discovery layouts such as `documents.sot.path` as compatibility inputs to understand before migrating, not as a reason to overwrite mature adopter memory.
- Do not commit machine-specific reference paths, local drive names, user profile paths, `file://` URIs, localhost URLs, or private workspace URLs into YAIML guidance; those belong in the human prompt, agent/workspace configuration, environment, or ignored local notes.
- Do not introduce implementation libraries, CLIs, SDKs, provider adapters, package manifests, schemas for Markdown memory documents, conformance fixtures, or web applications during the convention-first phase.
- Preserve the MIT License unless the maintainer explicitly approves a license change.
- Before finishing material work, update only affected YAIML documents without waiting for a separate request, prune stale state, and do not append a work diary. Respect read-only task scope and leave unchanged memory alone.
- Report contradictions rather than smoothing them into confident prose.
- Do not treat a command, script, workflow, or test existing in source as proof that it passed; successful execution only applies under the recorded conditions.
- Before changing shared behavior, identify affected invariants and authorized changes; ground expected outcomes independently of the candidate. Compare an accepted baseline under equivalent conditions when available, without treating old behavior as inherently correct.
- Separate reported concerns, evidence, and hypotheses. Keep disputed candidates out of shared defaults while investigating; continue independent authorized work. Resolve factual concerns with relevant evidence, not unrelated passing checks or failure to reproduce. Changes to intent or acceptance criteria require established authority. Follow the [evidence guidance](docs/AMBIGUITY_AND_EVIDENCE.md#contradictions-and-regression-checks).
- Do not describe planned tooling as implemented tooling.
- Do not revive `SPEC.md`, schema-first language for Markdown memory documents, or formal conformance machinery unless a human explicitly changes the project phase.

When updating YAIML documents:

- Read the stable header first.
- Preserve human directives.
- Preserve multi-agent or multi-contributor conflicts until evidence or human direction resolves them.
- Remove resolved active risks from active sections.
- Mark uncertainty honestly.
- For affected memory, replace the existing account of changed facts; remove superseded claims and resolved active items. Keep completed work only as current capability, an active constraint, or a lesson that changes future action. Do not relocate history into new supporting files.
- Keep routine edits passage-scoped and unrelated structure stable. Coordinate broad compression separately. Before authorized integration, reconcile affected memory with the actual target and common ancestor; a clean merge does not prove consistent meaning. Preserve independent changes, distinguish branch from deployed facts, and route unresolved decisions to existing review authority. Recheck affected evidence after integration changes.
- Measure affected memory before/after. Report net growth with its reason and any budget overage in the task response, not the memory. Preserve necessary knowledge and governed retention.
