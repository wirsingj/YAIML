# Instructions for Agents Working on YAIML

Before making changes:

1. Read `yaiml.yml`.
2. Read the stable header at the top of each declared YAIML document before reading its body.
3. Treat `docs/SoTY.md`, `docs/ARCHITECTURE.md`, and `docs/MAINTAINER_GUIDE.md` as this repository's living project memory.
4. Treat examples, templates, prompts, and guides as supporting artifacts that must stay synchronized with the living-memory concept.

Working rules:

- Preserve the distinction between SoT, architecture, and maintainer procedures.
- Preserve the distinction between declared intent and implementation evidence.
- Dogfood YAIML retention and uncertainty rules in this repository.
- Treat natural-language requests such as "continue through the SoT list" or "update our SoT" as instructions to use this repository's YAIML memory, not as requests for separate prompt choreography.
- Do not introduce implementation libraries, CLIs, SDKs, provider adapters, package manifests, schemas, conformance fixtures, or web applications during the convention-first phase.
- Do not select a license without explicit human approval.
- Update the repository's YAIML documents after material changes.
- Report contradictions rather than smoothing them into confident prose.
- Do not describe planned tooling as implemented tooling.
- Do not revive `SPEC.md`, schema-first language, or formal conformance machinery unless a human explicitly changes the project phase.

When updating YAIML documents:

- Read the stable header first.
- Preserve human directives.
- Remove resolved active risks from active sections.
- Mark uncertainty honestly.
- Prune before appending if the relevant document is getting bloated.
