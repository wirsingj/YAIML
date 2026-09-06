# YAIML Roadmap

YAIML is in an early public convention-first phase. The long-term ambition is industry-standard adoption; maturity claims should follow outside use and evidence.

The immediate route is the self-contained [init prompt](prompts/init-yaiml.md). Improve the plain-file workflow before adding tools.

## Now

- Trial initialization, refresh, and compression in real repositories; keep YAIML’s own core memory short.
- Test portability across machines, contributors, and AI providers, including mature adopters with older discovery layouts.
- Gather three kinds of case evidence: a maintainer-owned project, an unfamiliar public repository, and a project owned by someone else. [YTMMOCC](docs/case-studies/YTMMOCC.md) supplies maintainer-owned inspection evidence only.
- Run comparable fresh-session tasks and retain failures and neutral results. Measure context cost as well as useful work.
- Refine headers, prompt length, and supporting-document split decisions from those trials.
- Prepare a short sanitized demo for developers, managers, and senior engineers: initialize memory, then show what a fresh session can recover.
- Establish a maintainer-approved private sensitive-reporting path before broader public pilot readiness.

## Public Pilot

Recruit feedback across multiple AI tools and a local-model workflow without making provider-specific integrations part of YAIML. Test constrained workplace use only with permitted, sanitized material.

Publish a simple adoption-report path and a visible process for resolving proposed convention changes. Contribution guidance, examples, evidence limits, and release criteria should be clear before broader maturity claims.

Add or refine examples and supporting templates only when actual use reveals recurring knowledge they need to hold.

## Maturity Milestones

These are proposed project milestones, not discovery-format versions or release promises.

| Milestone | Evidence sought |
| --- | --- |
| 0.2 — usable experiment | Small core, usable prompts, honest dogfooding and documented gaps |
| 0.3 — public pilot | Outside feedback and trials across different agent environments |
| 0.5 — implemented draft | Unrelated adopters, recorded incompatibilities and failures; a separately maintained helper or workflow |
| 1.0 — stable convention | Stable core expectations, migration guidance, independent adopters and case evidence |

The separate `yaiml.version` field identifies discovery layout. Editing guidance or reaching a project milestone does not itself require changing that field.

## Later

Possible helpers include initialization, stale-claim review, pruning, context assembly, editor snippets, and team review workflows. They remain deferred until the plain-file approach has enough use to justify them.

No runtime services, databases, orchestration, package dependencies, web apps, SDKs, provider adapters, or Markdown validators are planned during this phase. Any future validation would be limited to `yaiml.yml`.

## Human Decisions

The maintainer decides release labeling, contribution governance, maturity evidence thresholds, the private reporting channel, and whether tooling becomes appropriate. Preserve the MIT License; license changes and new ownership, trademark, or endorsement claims require explicit approval.
