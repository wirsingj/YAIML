---
yaiml: 0.2
kind: sot
title: SoTY
purpose: Preserve YAIML's current meaning, direction, risks, and immediate priorities.
belongs-here: current project identity, purpose, artifact set, strengths, weaknesses, risks, priorities, divergence, useful lessons.
not-here: complete history, permanent architecture, command reference.
durability: volatile; synthesize and prune aggressively.
read-with: YAIML Architecture; YAIML Maintainer Guide.
update-when: project concept, core artifacts, active risks, or priorities change materially.
agent-guidance: Verify repository shape. Preserve human direction. Mark uncertainty. Surface conflicts. Prune stale rewrite history.
---

# SoTY

## North Star And Human Direction

YAIML means Yet Another AI Markup Language: shared, repository-owned project memory for AI chats, coding agents, and human contributors.

Declared: the ambition is broad adoption as a standard. Current status remains an early public experiment; independent evidence must precede stronger maturity claims.

Declared: keep adoption prompt-first, no-install, and convention-first. Preserve the three core roles, ordinary Markdown, explicit uncertainty, and routine pruning. Do not add tooling or revive formal specification machinery without a human phase change.

Declared: keep this a personally maintained, public MIT-licensed project. Preserve the [maintainer’s independence declaration](PROJECT_INDEPENDENCE.md) and exclude employer-confidential material, secrets, and private transcripts. Record reviewed professional constraints without inventing legal or security conclusions.

Declared (maintainer request, 2026-09-06): use repeated audits and corrections to reduce verbosity, repetition, and issues that unfamiliar agents would reasonably flag. Clarity and defensible claims matter more than suppressing criticism.

## Current State And Evidence

Verified by repository inspection: YAIML consists of reference guides, seven helper prompts, core and optional supporting templates, two fictional examples, policy documents, and its own three core memory documents. There is no YAIML application runtime or build/test suite.

The README provides one adoption path. The init prompt is self-contained and reuses existing project documentation. Detailed guidance is organized by topic; [Architecture](ARCHITECTURE.md) maps the artifact responsibilities and [Maintainer Guide](MAINTAINER_GUIDE.md) describes review procedures.

Current guidance treats headers as reader orientation, `read-with` as a relevance hint, and discovery versions separately from prose revisions. Realignment follows established human direction; repository-local storage does not promise local-only AI processing. Core templates consolidate overlapping sections and permit omission of empty headings.

The [YTMMOCC case study](case-studies/YTMMOCC.md) records maintainer-owned repository inspection and dated public-listing observations. It does not measure productivity or establish independent adoption. External evidence is not revalidated by this documentation audit.

Prior local sampling reported useful project memory alongside legacy discovery maps and committed machine-specific reference paths. That historical report is not a reproducible independent trial. The current [compatibility policy](ADOPTION_AND_UPGRADES.md#discovery-layout-compatibility) preserves layouts during routine refresh and requires explicit migration direction.

## Active Risks And Gaps

- **Effectiveness remains unmeasured:** no controlled fresh-session comparison or independent adoption evidence is recorded.
- **Context and maintenance cost:** even concise instructions can produce overgrown or stale memory; the shortened init path and supporting-document choices need adopter trials.
- **Evidence and authority errors:** agents may still promote old results, inference, or fictional examples into current fact, or flatten contributor disagreements.
- **Portability and sharing:** generated memory must preserve useful constraints without machine-specific paths or sensitive content; legacy-adopter refresh behavior needs trials.
- **Phase drift:** added tools, formal requirements, or empty templates could displace the plain-file convention.
- **Reporting readiness:** a private sensitive-reporting path is not established by the current evidence; resolve this before broader public pilot readiness.

## Immediate Priorities

1. Trial the revised init, refresh, and compression prompts in real repositories; record failures and context cost.
2. Run comparable fresh-session tasks, including an unfamiliar repository and an independently owned project.
3. Exercise older discovery layouts without replacing mature memory or forcing migration.
4. Prepare the short sanitized demo and establish the private reporting path.
5. Keep current review evidence scoped in [Cold Start Review](COLD_START_REVIEW.md); prune affected memory after material changes.

## Open Questions

- Should discovery remain strongly recommended or become essential for every adopter?
- Which supporting roles recur enough to justify additional templates?
- What evidence and participation process justify each proposed [maturity milestone](../ROADMAP.md)?
- If future tooling becomes appropriate, what helper improves continuity without becoming infrastructure?

## Useful Lessons And Retired Directions

A reference repository needs more explanation than an adopter. Do not reproduce its document inventory in every project. Keep the init prompt self-contained, but link detailed guidance elsewhere instead of restating it throughout the reference.

Compression must preserve human directives, evidence scope, unresolved conflicts, and governed retention. Completed work becomes current capability, a useful lesson, or Git history.

Retired for this phase: `SPEC.md` as normative center, schemas and conformance machinery for Markdown, custom memory formats, and runtime/framework adoption. See [Architecture](ARCHITECTURE.md) for boundaries.
