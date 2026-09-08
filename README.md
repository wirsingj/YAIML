# YAIML

Agents forget. Projects shouldn’t.

**Yet Another AI Markup Language** is a project-memory convention for software repositories. It keeps current state, human direction, architecture, and working procedures in ordinary Markdown so the next AI session or contributor has somewhere to start.

YAIML is an early experiment with the ambition to become a widely adopted standard. You can use it today without installing anything; independent evidence of its effectiveness is still needed.

## Try It In A Repo

Open your project in a repository-aware AI chat or coding agent. Copy the contents of [Init YAIML](prompts/init-yaiml.md) into that session. The prompt is self-contained: you do not need to download this repository.

The session needs access to read and edit your project. Init creates a useful first draft from available evidence; it does not require installing the project's dependencies or completing a full code audit.

The agent inspects your project, reuses useful existing documentation, writes the smallest appropriate memory set, and adds a pointer to your agent instructions. Review the diff for invented facts, lost decisions, or sensitive information before accepting it.

Initialization can recover context from available files and supplied decisions. It cannot recover intent that existed only in a vanished chat.

## What Lives In Your Repository

| File | Responsibility |
| --- | --- |
| `SOT.md` | Current state, human direction, risks, uncertainty, and next priorities |
| `ARCHITECTURE.md` | Durable system shape, boundaries, and intended design |
| `MAINTAINER_GUIDE.md` | Setup, checks, diagnostics, release, and recovery procedures |
| `yaiml.yml` | Paths to those documents |

**SoT means “State Of The.”** The project completes the phrase; this repository uses `docs/SoTY.md`. Start with `SOT.md` unless your project already has a useful name.

Each memory document starts with a short header explaining its role and when to update or prune it. Filenames and headings can fit the project. Add supporting documents only when recurring knowledge needs its own home.

See [Minimal Notes](examples/minimal-notes/) for the smallest fictional example and a short paste-and-go demo, or [Canopy Dispatch](examples/canopy-dispatch/) for a larger one.

## Use It Day To Day

After initialization, ask normally: “Fix this bug,” “Audit the project,” or “Implement the next priority.” You should not need to mention YAIML again for routine work. The agent's persistent repository instructions tell it to read memory and maintain affected documents before finishing.

Init must connect the agent you are using and disclose any setup gap. This depends on the tool loading persistent instructions; a new tool needs a supported instruction route too. YAIML cannot force an agent to follow instructions it never receives.

For meaningful work, load the three core documents and only the supporting material relevant to the task. Afterward, update affected memory and remove stale state. Keep decisions and useful lessons; let Git retain the work history.

The key distinction is intent versus evidence. In a fictional example:

```text
Declared (maintainer decision): v1 stays local-only.
Verified by source inspection: settings still expose a cloud-sync option.
Divergence: the interface does not yet match the v1 decision.
```

A test definition is evidence that a check exists. A passing run establishes an outcome only under the conditions actually checked. Missing evidence and unresolved disagreements should stay visible.

YAIML records project understanding alongside code, tests, issues, and agent instructions. Those sources still matter. Memory does not override repository rules, permissions, or current authorized direction.

## Maintenance Helpers

Setup is a one-time starting point; these prompts help when explicit maintenance is useful.

| Need | Prompt |
| --- | --- |
| Orient a fresh session | [Hydrate](prompts/hydrate-agent-session.md) |
| Record material changes | [Update project memory](prompts/update-project-memory.md) |
| Check claims against reality | [Audit](prompts/audit-against-reality.md) |
| Remove repetition and stale state | [Compress](prompts/compress-project-memory.md) |
| Compare with a newer YAIML reference | [Update YAIML](prompts/update-yaiml.md) |
| Apply a human-directed change in project direction | [Realign](prompts/major-project-realignment.md) |

“Update YAIML” means refresh convention guidance from a reference you supply, preserving the project’s own memory. “Compress YAIML” means prune that memory. See [Adoption And Updates](docs/ADOPTION_AND_UPGRADES.md) for existing-document reuse and older discovery layouts.

## Evidence And Limits

[YTMMOCC](docs/case-studies/YTMMOCC.md) records maintainer-owned adoption. [Local adoption exercises](docs/case-studies/ADOPTION_TRIAL.md) record isolated initialization, legacy refresh, and compression with measured document sizes. Neither establishes productivity gains or independent adoption. [The current review](docs/COLD_START_REVIEW.md) records repository findings and remaining gaps.

YAIML needs maintenance and consumes reading context. Stale or overgrown memory can mislead an agent. Whether its benefits outweigh that cost needs trials beyond the maintainer’s projects. Use [Evaluation](docs/EVALUATION.md) to report successes, failures, and neutral results.

## Reference And Participation

- [Concepts](docs/CONCEPTS.md): purpose, vocabulary, and design tradeoffs.
- [Core Document Family](docs/CORE_DOCUMENT_FAMILY.md): where facts belong.
- [Stable Headers](docs/STABLE_HEADERS.md), [Context Loading](docs/CONTEXT_LOADING.md), and [Agent Integration](docs/AGENT_INTEGRATION.md): how sessions find and read memory.
- [Ambiguity And Evidence](docs/AMBIGUITY_AND_EVIDENCE.md) and [Pruning And Lifecycle](docs/PRUNING_AND_LIFECYCLE.md): how memory stays trustworthy.
- [Contributing](CONTRIBUTING.md) and [Roadmap](ROADMAP.md): feedback and future direction.

Licensed under [MIT](LICENSE.md). Maintained with [AI assistance](AI_USAGE.md) as a [personal, independent project](docs/PROJECT_INDEPENDENCE.md). Keep memory appropriate for its repository’s audience; follow [Security And Sensitive Information](SECURITY.md) for handling and reporting concerns.

When redistributing copied YAIML prompts, templates, or other substantial material, retain the applicable copyright and permission notice from [LICENSE.md](LICENSE.md). Adoption does not ask an agent to change your project's license.
