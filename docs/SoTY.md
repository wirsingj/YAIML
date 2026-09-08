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

Declared: the standalone init prompt is the primary integration point. A user should paste it into a repository-capable agent and obtain useful memory without additional downloads, libraries, installs, or coordinator dependencies. Routine reading and writing must then follow ordinary task requests without further YAIML reminders. Init must connect the active agent's persistent instructions and disclose setup gaps. Preserve human readability while controlling inspection and output cost.

Declared: keep this a personally maintained, public MIT-licensed project. Preserve the [maintainer’s independence declaration](PROJECT_INDEPENDENCE.md) and exclude employer-confidential material, secrets, and private transcripts. Record reviewed professional constraints without inventing legal or security conclusions.

Declared (maintainer request, 2026-09-06): use repeated audits and corrections to reduce verbosity, repetition, and issues that unfamiliar agents would reasonably flag.

## Current State And Evidence

Verified by repository inspection: YAIML consists of reference guides, seven helper prompts, core and optional supporting templates, two fictional examples, policy documents, and its own three core memory documents. There is no YAIML application runtime or build/test suite.

The README provides one adoption path. The init prompt is self-contained and reuses existing project documentation. Detailed guidance is organized by topic; [Architecture](ARCHITECTURE.md) maps the artifact responsibilities and [Maintainer Guide](MAINTAINER_GUIDE.md) describes review procedures.

Current guidance distinguishes headers from discovery versions, bounds initial inspection, avoids sensitive-file collection and unnecessary command execution, and preserves concurrent work. Repeated init/refresh should leave healthy memory unchanged. Existing layouts and custom fields survive compatible guidance refreshes; actual consumers must be checked before requested migrations.

The [YTMMOCC case study](case-studies/YTMMOCC.md) records maintainer-owned inspection and dated listing observations. [Local adoption exercises](case-studies/ADOPTION_TRIAL.md) add actual isolated document edits: initialization on a public source snapshot, unchanged repeat setup, and a legacy guide refresh/compression with the discovery map and core memory preserved. These are same-session exercises, not independent adoption or runtime validation.

The [minimal example](../examples/minimal-notes/README.md#short-paste-and-go-demo) now includes a short fictional demo. [Evaluation](EVALUATION.md#ready-to-run-comparison) provides concrete matched tasks and reviewer criteria; fresh comparison sessions have not run. GitHub private vulnerability reporting was enabled and verified on 2026-09-06; [Security](../SECURITY.md) links the reporting route.

## Active Risks And Gaps

- **Effectiveness remains unmeasured:** no controlled fresh-session comparison or independent adoption evidence is recorded.
- **Context and maintenance cost:** even concise instructions can produce overgrown or stale memory; the shortened init path and supporting-document choices need adopter trials.
- **Evidence and authority errors:** agents may still promote old results, inference, or fictional examples into current fact, or flatten contributor disagreements.
- **Portability and sharing:** one preserved legacy map does not establish compatibility with every consumer, layout, or concurrent editing workflow.
- **Phase drift:** added tools, formal requirements, or empty templates could displace the plain-file convention.

## Immediate Priorities

1. Run the prepared fresh-session comparison; record total context cost and failures without sharing answers between conditions.
2. Obtain a permitted owner-led trial and feedback from outside the maintainer's projects; a public checkout alone is not independent adoption.
3. Repeat adoption and refresh in another agent environment, including an unfamiliar layout and concurrent edits; preserve failed and neutral outcomes.
4. Run the prepared demo with a new reader and record what they misunderstood or could not recover.
5. Refine only the guidance those trials show needs changing; keep [current review evidence](COLD_START_REVIEW.md) scoped and core memory concise.

## Open Questions

- Should discovery remain strongly recommended or become essential for every adopter?
- Which supporting roles recur enough to justify additional templates?
- What evidence and participation process justify each proposed [maturity milestone](../ROADMAP.md)?
- If future tooling becomes appropriate, what helper improves continuity without becoming infrastructure?

## Useful Lessons And Retired Directions

A reference repository needs more explanation than an adopter. Do not reproduce its document inventory in every project. Keep the init prompt self-contained, but link detailed guidance elsewhere instead of restating it throughout the reference.

Compression must preserve human directives, evidence scope, unresolved conflicts, and governed retention. Completed work becomes current capability, a useful lesson, or Git history.

Retired for this phase: `SPEC.md` as normative center, schemas and conformance machinery for Markdown, custom memory formats, and runtime/framework adoption. See [Architecture](ARCHITECTURE.md) for boundaries.
