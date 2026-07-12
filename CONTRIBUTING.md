# Contributing to YAIML

YAIML is an incubating convention and reusable template docset for living project memory, project definition, project management, and AI-chat, agent, and contributor continuity in AI-assisted development.

YAIML is the canonical project and standard name. Do not reintroduce ARCS branding except in narrowly scoped migration notes.

Contributions should make the convention clearer, more useful, easier to apply, or harder for agents to misuse.

The value of YAIML is the convention for preserving project understanding, not the volume of documents around it. Favor refinement over expansion.

## Ground Rules

- Keep the center on living project memory, not schema design.
- Do not add CLIs, SDKs, package manifests, provider adapters, web apps, or parser implementations during the convention-first phase.
- Do not add conformance fixtures or formal validation machinery unless the project explicitly changes phase.
- Preserve the distinction between human intent and implementation evidence.
- Preserve the distinction between SoT, durable Architecture, and procedural Maintainer guidance.
- Preserve the self-unfolding document model: add supporting documents when they clarify recurring project memory, definitions, risks, preferences, or doctrine; avoid empty ceremony.
- Treat examples and templates as supporting artifacts that must stay aligned with the concepts.
- Prefer one strong template or prompt over several weak variants.
- Use ordinary engineering language before introducing YAIML-specific terms.
- Keep `yaiml.yml` as a lightweight discovery/version marker, not a schema or local-reference store.
- Preserve mature repository-specific YAIML documents during upgrades; do not replace them with generic templates.
- Report contradictions instead of smoothing them into confident prose.

## Licensing

This repository currently uses a restrictive all-rights-reserved notice during incubation. Do not replace it with an open-source license, license header, or broader public reuse claim without explicit human approval.

The maintainer intends to choose an open license before broad public reuse, but no license or release date has been selected.

## Review Checklist

Before changing YAIML, ask:

- Does this help a fresh agent understand a project faster and better?
- Does this improve a new AI chat, coding agent, or contributor's ability to reconstruct the project's current engineering understanding?
- Does this protect explicit human corrections?
- Does this keep uncertainty visible?
- Does this help agents prune instead of append forever?
- Does this help the document family self-unfold where useful without creating empty files?
- Does this avoid turning YAIML into a classical technical standard?
- Could a developer use this tonight with ordinary Markdown files, with prompts only as setup or maintenance helpers?
