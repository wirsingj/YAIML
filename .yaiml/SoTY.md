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

YAIML means Yet Another AI Markup Language: shared, repository-owned project memory for humans and AI agents. Declared scope spans domains; source code is optional. Current guidance/examples emphasize software, with broader-domain behavior unverified.

Declared: the ambition is broad adoption as a standard; current status is an early public experiment. Keep ordinary adoption convention-first and no-install, with three distinct roles, ordinary Markdown, explicit uncertainty, and synthesis. A bundled runtime or formal specification remains outside the current scope.

Declared (maintainer direction, October 2026): [YAIMLACP](YAIMLACP.md) is optional serverless coordination through existing subagents, with no server or installation. At startup and on context loading or refresh, consider usefulness without extra scans or calls. For a concrete benefit, describe the option, access, limits, cost, and one-agent alternative; obtain affirmative confirmation before first use and again if scope or cost changes. Reuse valid scoped approval; silence is not consent.

Declared (maintainer direction, October 2026): YAIML is context/project management with a one-prompt minimum interaction. Assume a new user and agent have no YAIML context or maintainer checkout. The small seed immediately retrieves guidance, establishes memory and embeds discoverable `yaiml-` skills. Ordinary work uses and maintains context automatically; optional commands such as `yaiml-to-do 10` and `yaiml-audit` select the same methods. Compose requested work without command choreography. Grow useful knowledge and methods, preserving local adaptations during refresh. Keep YAIML-owned material in `.yaiml/`, with supported host/public entry points outside. Distinguish local development snapshots from published references.

Declared: personal public project; require credit, permit commercial/client use, prohibit selling YAIML or charging for forks. Preserve [independence](PROJECT_INDEPENDENCE.md); exclude employer-confidential material, secrets, private transcripts and private-project dependencies. [Licensing](../LICENSE.md) preserves earlier grants. Invent no professional conclusions.

Declared (maintainer requests, September 2026): reduce repetition by audience and address under-pruning across adopters, not only this reference repository. Preserve useful workflow specificity across entry points and owning methods. Team use must keep routine edits local to affected passages and reconcile branch changes through existing review, without mandatory CI or subagents.

## Current State And Evidence

The reference supplies eleven workflow skills plus an alias, seven optional prompts, ten starters, guides, examples and memory. `yaiml-git` covers requested Git actions while preserving current work and local authority. The maintainer identifies these projects as works in progress; latest working files, including uncommitted edits, are canonical. Commits identify provenance, not deployment. [Architecture](ARCHITECTURE.md) owns responsibilities; [Maintainer Guide](MAINTAINER_GUIDE.md) owns review procedures.

[Bootstrap](BOOTSTRAP.md) connects hosts; fifteen local adopters have twelve entries. CLI trials cover public-only setup, ordinary requests, conversational recall, verification updates, custom growth, composition, unchanged refresh and pending license approval. Structural/discovery/repeat checks passed; native-write cases remained partial. A matched trial supports correcting stale activation notes. Replaying the original AIWIKI request with the corrected method updated affected headers and activation evidence; fresh reuse left files unchanged. [Current review](COLD_START_REVIEW.md) scopes evidence; [upgrade guidance](ADOPTION_AND_UPGRADES.md#existing-yaiml-update) explains repair.

The [YTMMOCC case](case-studies/YTMMOCC.md) and [local adoption exercises](case-studies/ADOPTION_TRIAL.md) contain dated maintainer-owned evidence. The [current review](COLD_START_REVIEW.md) describes this repository's latest changes and verification limits. Neither establishes independent adoption or productivity gains.

## Active Risks And Gaps

- **Under-pruning:** earlier local review reported a roughly 22,000-word SoT with an inbox instruction and architecture accumulating in another project's state document. The causal explanation is a hypothesis, not a controlled result. Recovery and recurrence must be measured after updating adopter instructions.
- **Consumer compatibility:** ShepAIrd's local repair reads migrated YAIML/Chaitroom memory and retains root-layout support. Its ARCS migration still emits an unquoted version. [Current portfolio evidence](COLD_START_REVIEW.md#portfolio-compatibility-and-disclosure) scopes verified compatibility; broader consumers, deployment and historical aggregates remain unverified.
- **Historical disclosure:** selected current ShepAIrd memory and registry values contain no actual machine-specific locations under the targeted check. Earlier exposure/history remains unassessed; this is not comprehensive secret detection or proof of safety.
- **Concurrent work:** team-scale merge burden and agent adherence remain unmeasured. Textual conflict resolution does not establish consistent meaning or combined verification.
- **Effectiveness:** no completed controlled comparison, independent adoption, or measured token savings. General maintenance reliability, recurring pruning, wider lifecycle behavior and coordination safety remain unproven. Total experiment cost remains incomplete.
- **Evidence and authority:** agents can promote inference or internally consistent tests into correctness and flatten contributor conflicts. A maintainer-reported depth-order regression motivated stronger independent-check guidance; its cause was not inspected here and prevention remains untested. Preserve sources, intended behavior, and unresolved disagreements.

## Immediate Priorities

1. Broaden maintenance trials and cover conflicting adaptations, interrupted acquisition, accepted license changes and native-route repair. Public bootstrap and the original header-miss replay have scoped CLI passes; other hosts remain untested.
2. Assess remaining migration/version compatibility and historical disclosure before broader rollout. Keep current working-copy measurements separate from historical deployment claims.
3. Use a working isolated runner for the [prepared comparison](EVALUATION.md#ready-to-run-comparison) and [new-reader demo](examples/minimal-notes/README.md#short-paste-and-go-demo). Measure total context cost, missed reads/writes, and misunderstandings.
4. Run the [concurrent-contributor check](EVALUATION.md#concurrent-contributor-check), then obtain an owner-led trial outside the maintainer's projects and another agent environment. Measure unrelated diff churn and lost constraints.
5. Measure recurring maintenance and under-pruning in an authorized adopter. Change guidance from observed failures; avoid accumulating speculative rules.

## Open Questions

Should discovery become essential rather than strongly recommended? Which supporting roles recur enough to warrant templates? What evidence and participation justify the [maturity milestones](ROADMAP.md)? Does YAIMLACP coordination improve outcomes enough to justify its cost over one-agent work? Could `yaiml-git` inform the maintainer's semantic merge tool for conflicting branch memory? That connection is exploratory; no tool integration is established.

Retired approaches and phase boundaries belong in [Architecture](ARCHITECTURE.md). Completed audit history remains in Git; current memory keeps only findings that still affect decisions.
