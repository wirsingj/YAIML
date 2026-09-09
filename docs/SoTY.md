---
yaiml: 0.2
kind: sot
title: SoTY
purpose: Preserve YAIML's current meaning, direction, risks, and immediate priorities.
belongs-here: current project identity, purpose, artifact set, strengths, weaknesses, risks, priorities, divergence, useful lessons.
not-here: complete history, permanent architecture, command reference.
durability: volatile; synthesize and prune aggressively.
budget: About 1000 words; preserve necessary evidence and direction if exceeded.
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

Repository inspection confirms reference guides, seven prompts, core/supporting templates, two fictional examples, policy files, and YAIML's own core memory. There is no application runtime or build/test suite.

The self-contained init establishes useful memory and persistent agent instructions. It preserves existing files, discovery layouts, and local choices; meaningful changes trigger routine updates. Role-appropriate budgets guide pruning without requiring deletion, padding, or removal of necessary evidence. [Architecture](ARCHITECTURE.md) owns the artifact boundaries; [Maintainer Guide](MAINTAINER_GUIDE.md) owns review procedures.

The [YTMMOCC case](case-studies/YTMMOCC.md) records maintainer-owned inspection and dated listings. [Local adoption exercises](case-studies/ADOPTION_TRIAL.md) record isolated init, repeat setup, and legacy guide refresh/compression. These are same-session evidence, not independent adoption or runtime validation. The [current audit](COLD_START_REVIEW.md) records corrections and verification limits.

The [fictional demo](../examples/minimal-notes/README.md#short-paste-and-go-demo) and [matched comparison tasks](EVALUATION.md#ready-to-run-comparison) are prepared; fresh sessions have not run. Private vulnerability reporting was enabled on 2026-09-06 and rechecked on 2026-09-08; [Security](../SECURITY.md) links the route.

## Active Risks And Gaps

- **Silent adoption failure (verified 2026-09-08, 13 deployments):** seven carry memory and no agent instruction file, so nothing loads it. Documents look correct and no step reports the gap. Init now treats the pointer as pass or fail; the seven remain unfixed.
- **Pruning loses to preservation (verified 2026-09-08, lorekeeper):** across 267 revisions of a declared-volatile SoT, 260 grew it and 7 shrank it, the largest reduction 131 bytes, reaching ~22,000 words under a header reading "prune aggressively." Budget guidance is untested against this.
- **Discovery has forked (verified 2026-09-08):** twelve deployments use the legacy `documents.*.path` layout, one the recommended shape. Non-migration is deliberate, but no deployment demonstrates the layout the README teaches.
- **Memory leaks environment detail (verified 2026-09-08, ShepAIrd):** a maintainer profile path reached a public repository through memory. Written after reading a whole project, memory carries higher disclosure risk than ordinary docs. Init now requires a scan; history is unaffected.
- **Effectiveness and cost:** no controlled fresh-session comparison, independent adoption evidence, or measured total token savings. Growth, stale memory, and missed automatic updates need adopter trials.
- **Evidence and authority:** agents may promote old results, inference, fictional examples, or unauthenticated approval claims into current fact, or flatten contributor disagreements.
- **Portability:** a preserved legacy map does not establish compatibility with every reader, layout, instruction mechanism, or concurrent workflow.
- **Phase drift:** extra tooling, formal requirements, or empty templates could displace the plain-file convention.

## Immediate Priorities

1. Repair the seven deployments with no instruction pointer, and remove the leaked profile path from ShepAIrd's memory. Until the pointer exists, those repositories measure nothing.
2. Publish the portfolio drift measurement: per repository, SoT size at every revision, growth and shrink counts, and the SoT-to-Architecture ratio. The data is already in Git, costs nothing, and reports negatively on the convention's central mechanism. Publish it before any further adoption claim.
3. Run the prepared fresh-session comparison; record total context cost and failures without sharing answers between conditions.
4. Obtain a permitted owner-led trial and feedback from outside the maintainer's projects; a public checkout alone is not independent adoption.
5. Repeat adoption and refresh in another agent environment, including an unfamiliar layout and concurrent edits; preserve failed and neutral outcomes.
6. Run the prepared demo with a new reader and record what they misunderstood or could not recover.
7. Refine only the guidance those trials show needs changing; keep [current review evidence](COLD_START_REVIEW.md) scoped and core memory concise.

## Open Questions

- Should discovery remain strongly recommended or become essential for every adopter?
- Which supporting roles recur enough to justify additional templates?
- What evidence and participation process justify each proposed [maturity milestone](../ROADMAP.md)?
- If future tooling becomes appropriate, what helper improves continuity without becoming infrastructure?

## Useful Lessons And Retired Directions

A reference repository needs more explanation than an adopter. Do not reproduce its document inventory in every project. Keep the init prompt self-contained, but link detailed guidance elsewhere instead of restating it throughout the reference.

Compression must preserve human directives, evidence scope, unresolved conflicts, and governed retention. Completed work becomes current capability, a useful lesson, or Git history.

Retired for this phase: `SPEC.md` as normative center, schemas and conformance machinery for Markdown, custom memory formats, and runtime/framework adoption. See [Architecture](ARCHITECTURE.md) for boundaries.
