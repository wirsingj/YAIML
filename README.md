# YAIML

Agents forget. Projects shouldn’t.

YAIML keeps a project's current engineering understanding in its repository, so a new AI session or contributor can pick up the work with its decisions, constraints, and open questions intact. The name stands for **Yet Another AI Markup Language**. The files are ordinary Markdown, with a small YAML index.

A fresh session can read the code and still miss why a feature was deliberately limited, which approach was rejected, or whether a test actually passed. YAIML gives that knowledge a maintained home alongside the code.

YAIML is an early experiment with the ambition to become a widely adopted standard. You can use it today without installing anything; independent evidence of its effectiveness is still needed.

## Why Keep Project Memory?

- **For your own work:** preserve decisions and corrections between sessions, including what you still need to verify.
- **For a team:** give contributors a shared starting point and include changes to project understanding in normal code review.
- **For a long-lived project:** keep knowledge available across contributor, machine, and AI-provider changes. Different tools can use the same memory once their repository instructions are connected.

The loop is simple: read the current understanding, check it against the task, do the work, then update and prune affected memory.

## Try It In A Repo

Open your project in a repository-aware AI chat or coding agent. Copy the contents of [Init YAIML](prompts/init-yaiml.md) into that session. The prompt is self-contained: you do not need to download this repository.

The agent needs project read/write access. It inspects the repository, reuses useful documentation, writes a small memory set, and connects your agent instructions. It reports evidence and setup gaps. No dependency installation or full code audit is required. Review the diff for invented facts, lost decisions, or sensitive information before accepting it.

Initialization can recover context from available files and supplied decisions. It cannot recover intent that existed only in a vanished chat.

## What Lives In Your Repository

**SoT means “State Of The.”** It describes the whole project; this repository uses `docs/SoTY.md`. The agent normally starts with `SOT.md` unless your project already has a useful name.

| File | Responsibility |
| --- | --- |
| `SOT.md` | Current state, human direction, risks, uncertainty, and next priorities |
| `ARCHITECTURE.md` | Durable system shape, boundaries, and intended design |
| `MAINTAINER_GUIDE.md` | Setup, checks, diagnostics, release, and recovery procedures |
| `yaiml.yml` | Paths to those documents |

Each memory document has a short header explaining its role and maintenance. Names and headings can fit the project. Add supporting documents only when recurring knowledge needs its own home.

`AGENTS.md` or its equivalent tells the agent how to work, including when to read and update YAIML. The memory documents hold what the project currently understands. These roles can overlap; reuse existing documentation where it fits.

See [Minimal Notes](examples/minimal-notes/) for the smallest fictional example and a short paste-and-go demo, or [Canopy Dispatch](examples/canopy-dispatch/) for a larger one.

## Use It Day To Day

After initialization, ask normally: “Fix this bug,” “Audit the project,” or “Implement the next priority.” Persistent repository instructions tell the agent to read and maintain affected memory without routine YAIML reminders.

Init connects applicable existing agent instructions, such as `AGENTS.md` and `CLAUDE.md`, to the same memory and reports setup gaps. A tool added later needs a supported instruction route too. This depends on each tool loading those instructions.

The key distinction is intent versus evidence. In a fictional example:

```text
Declared (maintainer decision): v1 stays local-only.
Verified by source inspection: settings still expose a cloud-sync option.
Divergence: the interface does not yet match the v1 decision.
```

Code, tests, decisions, and issues remain the sources behind the summaries. Memory does not override repository rules, permissions, or authorized direction.

For teams, include focused memory edits with each change. Coordinate broad cleanup separately and review meaning against the target branch before merging. See [concurrent branches and review](docs/PRUNING_AND_LIFECYCLE.md#concurrent-branches-and-review); no additional tooling is required.

## Maintenance Helpers

Routine work needs no extra prompts. For occasional maintenance, “Update YAIML” means refresh convention guidance from a supplied reference; “Compress YAIML” means prune the project's memory.

See [Adoption And Updates](docs/ADOPTION_AND_UPGRADES.md) for compatibility and the [maintenance prompt catalog](docs/ADOPTION_AND_UPGRADES.md#maintenance-prompts) for explicit orientation, auditing, compression, and realignment.

## Evidence And Limits

[YTMMOCC](docs/case-studies/YTMMOCC.md) records maintainer-owned adoption. [Local adoption exercises](docs/case-studies/ADOPTION_TRIAL.md) record isolated initialization, legacy refresh, and compression with measured document sizes. Neither establishes productivity gains or independent adoption. [The current review](docs/COLD_START_REVIEW.md) records repository findings and remaining gaps.

YAIML needs maintenance and consumes reading context. Agents read the concise core, then supporting material relevant to the task. Stale or overgrown memory can mislead them. If your existing docs already preserve this understanding, adopting another convention may add little.

For a team trial, use one bounded maintenance task and compare fresh sessions with and without YAIML. Track missed constraints, human corrections, useful work, and context cost. [Evaluation](docs/EVALUATION.md) provides the method; benefits beyond the maintainer's projects remain unproven.

YAIML itself runs no service and uploads nothing. The AI tool you use has its own access and data-handling behavior.

## Reference And Participation

- [Concepts](docs/CONCEPTS.md): purpose, vocabulary, and design tradeoffs.
- [Prior Art](docs/PRIOR_ART.md): comparable conventions, and when to use one of them instead.
- [Core Document Family](docs/CORE_DOCUMENT_FAMILY.md): where facts belong.
- [Stable Headers](docs/STABLE_HEADERS.md), [Context Loading](docs/CONTEXT_LOADING.md), and [Agent Integration](docs/AGENT_INTEGRATION.md): how sessions find and read memory.
- [Ambiguity And Evidence](docs/AMBIGUITY_AND_EVIDENCE.md) and [Pruning And Lifecycle](docs/PRUNING_AND_LIFECYCLE.md): how memory stays trustworthy.
- [Contributing](CONTRIBUTING.md) and [Roadmap](ROADMAP.md): feedback and future direction.

Licensed under [MIT](LICENSE.md). Maintained with [AI assistance](AI_USAGE.md) as a [personal, independent project](docs/PROJECT_INDEPENDENCE.md). Keep memory appropriate for its repository’s audience; follow [Security And Sensitive Information](SECURITY.md) for handling and reporting concerns.

When redistributing copied YAIML prompts, templates, or other substantial material, retain the applicable copyright and permission notice from [LICENSE.md](LICENSE.md). Adoption does not ask an agent to change your project's license.
