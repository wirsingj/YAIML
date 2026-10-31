<!-- yaiml-revision: 0.47.a709c1ceed90c210 -->
# Contributing to YAIML

YAIML is an early public context and project management convention: one prompt establishes project memory and reusable skills, ordinary work maintains that context, and optional named workflows provide more control.

Contributions should make the convention clearer, more useful, easier to apply, or harder for agents to misuse.

This repository both develops YAIML and uses it. [reference/](reference/) contains the reusable product; [docs/](docs/README.md) explains it and records evaluation evidence; [examples/](examples/README.md) illustrates it. The [roadmap](ROADMAP.md) is public project direction. Only our working context, change records and project-local methods belong in `.yaiml/`. An agent-readable header does not make a product document project memory. [Architecture](.yaiml/ARCHITECTURE.md) owns that boundary; [Bootstrap](reference/BOOTSTRAP.md#resolve-and-acquire) identifies the adoption set. Our policies, release process and completed examples do not become adopter defaults.

The value of YAIML is the convention for preserving project understanding, not the volume of documents around it. Favor refinement over expansion.

## Ground Rules

- Keep the center on living project memory, not schema design for Markdown documents.
- [YAIMLACP](reference/YAIMLACP.md) supplies optional coordination guidance using existing host capabilities, without a server or installation. Adding a runtime, CLI, SDK, package manifest, provider adapter, web app, or parser here requires an authorized implementation scope; ordinary adoption remains usable without them.
- Do not add conformance fixtures or formal validation machinery for Markdown memory documents unless the project explicitly changes phase.
- Preserve the distinction between human intent and implementation evidence.
- Preserve the distinction between SoT, durable Architecture, and procedural Maintainer guidance.
- Preserve the self-unfolding document model: add supporting documents when they clarify recurring project memory, definitions, risks, preferences, or doctrine; avoid empty ceremony.
- Keep distributed skills, prompts, templates and examples aligned; keep source-project-only facts and skills outside the adoption package.
- Improve owning methods and their entry points together; avoid competing copies.
- Use ordinary engineering language before introducing YAIML-specific terms.
- Keep `yaiml.yml` as a tiny discovery protocol, not a schema for Markdown memory documents or a local-reference store.
- Preserve mature repository-specific YAIML documents during upgrades; do not replace them with generic templates.
- Report contradictions instead of smoothing them into confident prose.

## Licensing

YAIML uses the [YAIML Attribution and No-Resale License](LICENSE.md): commercial products and client work may use it, but selling YAIML or charging for its forks requires separate permission. Keep the license, copyright, author/project credit and change notices with copied material. Professional legal review of these published custom source-available terms remains outstanding. Earlier MIT grants remain unaffected; preserve applicable third-party notices. Do not apply YAIML's license to an adopting project's own material by default.

By submitting a new contribution under these terms, you agree that it is provided under this repository's license; you retain ownership of your contribution. This does not change earlier contribution grants. Submit only material you have the right to contribute. Do not include employer-confidential material, third-party material without permission, secrets, private transcripts, raw sensitive logs, customer or personal data, unreleased vulnerability details, or proprietary project text from another repository.

Do not change the license, add license headers, or make new trademark, ownership, or endorsement claims without explicit maintainer approval.

## Review Checklist

Before changing YAIML, ask:

- Does this improve a new AI chat, coding agent, or contributor's ability to reconstruct the project's current engineering understanding?
- Does an adopter receive only reusable guidance, with its own facts and authority preserved?
- Have product behavior and this repository's own memory/procedures been checked separately, including both when shared methods change?
- Does this protect explicit human corrections?
- Does this keep uncertainty visible?
- Does this help agents prune instead of append forever?
- Does this help the document family self-unfold where useful without creating empty files?
- Does this preserve the current convention-first phase without introducing formal specification or tooling requirements?
- Can a newcomer start with one prompt, work normally and select skills without maintainer context or corrective reminders? Record any extra help as assistance, not an unassisted pass.

## Feedback And Adoption Reports

Open a GitHub issue or pull request with a concrete unclear passage, contradiction, or proposed correction. For adoption feedback, include the YAIML reference revision, repository context you may share, agent environment, task, observed result, and what required correction. Use [Evaluation](docs/evaluation/EVALUATION.md) for comparisons; small failure reports are welcome too.

Use the private-contact guidance in [SECURITY.md](SECURITY.md) for sensitive reports. Do not publish private project memory or transcripts to make a report reproducible.

Use [revision guidance](reference/VERSIONING.md) to finish material changes: stamp affected managed Markdown and record intent, parents, all affected project paths and actual checks in the core [changes.md](.yaiml/changes.md). Preserve audit records while pruning current memory. Product releases and discovery labels are separate from local iteration counters.
