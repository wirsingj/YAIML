# Contributing to YAIML

YAIML is an early public convention and reusable template docset for living project memory, project definition, project management, and AI-chat, agent, and contributor continuity in AI-assisted development.

Contributions should make the convention clearer, more useful, easier to apply, or harder for agents to misuse.

The value of YAIML is the convention for preserving project understanding, not the volume of documents around it. Favor refinement over expansion.

## Ground Rules

- Keep the center on living project memory, not schema design for Markdown documents.
- Do not add CLIs, SDKs, package manifests, provider adapters, web apps, or parser implementations during the convention-first phase.
- Do not add conformance fixtures or formal validation machinery for Markdown memory documents unless the project explicitly changes phase.
- Preserve the distinction between human intent and implementation evidence.
- Preserve the distinction between SoT, durable Architecture, and procedural Maintainer guidance.
- Preserve the self-unfolding document model: add supporting documents when they clarify recurring project memory, definitions, risks, preferences, or doctrine; avoid empty ceremony.
- Treat examples and templates as supporting artifacts that must stay aligned with the concepts.
- Prefer one strong template or prompt over several weak variants.
- Use ordinary engineering language before introducing YAIML-specific terms.
- Keep `yaiml.yml` as a tiny discovery protocol, not a schema for Markdown memory documents or a local-reference store.
- Preserve mature repository-specific YAIML documents during upgrades; do not replace them with generic templates.
- Report contradictions instead of smoothing them into confident prose.

## Licensing

YAIML is licensed under the [MIT License](LICENSE.md), which names Jeff Wirsing as copyright holder. Copies or substantial portions must retain its copyright and permission notice; see the [OSI MIT text](https://opensource.org/license/mit). Keep those notices when redistributing copied prompts or templates. Do not apply YAIML's license to an adopting project's own material by default.

By submitting a contribution, you agree that your contribution is provided under the MIT License used by this repository. Submit only material you have the right to contribute. Do not include employer-confidential material, third-party material without permission, secrets, private transcripts, raw sensitive logs, customer or personal data, unreleased vulnerability details, or proprietary project text from another repository.

Do not change the license, add license headers, or make new trademark, ownership, or endorsement claims without explicit maintainer approval.

## Review Checklist

Before changing YAIML, ask:

- Does this improve a new AI chat, coding agent, or contributor's ability to reconstruct the project's current engineering understanding?
- Does this protect explicit human corrections?
- Does this keep uncertainty visible?
- Does this help agents prune instead of append forever?
- Does this help the document family self-unfold where useful without creating empty files?
- Does this preserve the current convention-first phase without introducing formal specification or tooling requirements?
- Could a developer use this tonight with ordinary Markdown files, with prompts only as setup or maintenance helpers?

## Feedback And Adoption Reports

Open a GitHub issue or pull request with a concrete unclear passage, contradiction, or proposed correction. For adoption feedback, include the YAIML reference revision, repository context you may share, agent environment, task, observed result, and what required correction. Use [Evaluation](docs/EVALUATION.md) for comparisons; small failure reports are welcome too.

Use the private-contact guidance in [SECURITY.md](SECURITY.md) for sensitive reports. Do not publish private project memory or transcripts to make a report reproducible.
