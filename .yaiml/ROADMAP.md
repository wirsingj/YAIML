<!-- yaiml-revision: 0.43.65c0797e642cbbde -->
# YAIML Roadmap

YAIML is in an early public convention-first phase. The long-term ambition is industry-standard adoption; maturity claims should follow outside use and evidence.

The immediate route is one [init prompt](../reference/prompts/init-yaiml.md) that starts reference retrieval, project context and embedded methods. Evaluate the full [skills lifecycle](SKILLS_AND_LIFECYCLE.md) from a new user’s perspective, with no prior YAIML knowledge or maintainer-local paths.

## Now

- Validate the published seed-to-resource path, fresh-session ordinary use, named and composed skills, useful growth, offline behavior and refresh with local adaptations. Keep structural checks separate from observed behavior.
- Trial initialization, refresh, and compression in real repositories; keep YAIML’s own core memory short.
- Trial [YAIMLACP coordination](../reference/YAIMLACP.md): verify confirmation, bounded handoffs, cancellation, and actual cost against one-agent work. Add no server or installation.
- Test portability across machines, contributors, and AI providers, including mature adopters with older discovery layouts.
- Gather three kinds of case evidence: a maintainer-owned project, an unfamiliar public repository, and a project owned by someone else. [YTMMOCC](case-studies/YTMMOCC.md) supplies maintainer-owned inspection evidence only.
- Run comparable fresh-session tasks and retain failures and neutral results. Measure context cost as well as useful work.
- Refine headers, prompt length, and supporting-document split decisions from those trials.
- Run the [prepared sanitized demo](examples/minimal-notes/README.md#short-paste-and-go-demo) with new readers and check what a fresh session recovers.
- Keep the [private sensitive-reporting route](../SECURITY.md) available; GitHub's read-only API confirmed it enabled on 2026-10-18. Delivery remains untested.

## Public Pilot

Recruit feedback across multiple AI tools and a local-model workflow without making provider-specific integrations part of YAIML. Test constrained workplace use only with permitted, sanitized material.

Publish a simple adoption-report path and a visible process for resolving proposed convention changes. Contribution guidance, examples, evidence limits, and release criteria should be clear before broader maturity claims.

Add or refine examples and supporting templates only when actual use reveals recurring knowledge they need to hold.

## Maturity Milestones

These are evidence milestones, separate from product release numbers, discovery labels and local revision counters. [RELEASE.md](RELEASE.md) owns the current product identity; publishing 0.3.0 does not claim the public-pilot evidence milestone.

| Milestone | Evidence sought |
| --- | --- |
| Usable experiment | Small core, usable prompts, honest dogfooding and documented gaps |
| Public pilot | Outside feedback and trials across different agent environments |
| Implemented draft | Unrelated adopters, recorded incompatibilities and failures, and a repeatable maintenance workflow |
| 1.0 readiness — stable convention | Stable core expectations, migration guidance, independent adopters and case evidence |

The separate `yaiml.version` field identifies discovery layout. Editing guidance or reaching a project milestone does not itself require changing that field.

## Later

YAIMLACP describes optional serverless coordination for memory maintenance and project workflows. Use trials to establish whether the handoff convention improves on ordinary one-agent work; it makes no claim of standard MCP interoperability.

This reference repository supplies no runtime services, databases, orchestration engine, package dependencies, web apps, SDKs, or provider adapters. Ordinary adoption requires none. Memory-format validation remains limited to `yaiml.yml`; coordination messages impose no Markdown schema.

## Human Decisions

The maintainer decides release labeling, contribution governance, maturity evidence thresholds, the private reporting channel, and whether tooling becomes appropriate. Preserve the [approved license](../LICENSE.md) and earlier grants; further licensing, ownership, trademark or endorsement changes require explicit approval. Obtain professional review of custom terms before publication.
