---
yaiml-revision: "0.3.e5a6701538b64592"
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

Declared: pursue broad adoption while remaining an early public experiment: no installation, ordinary Markdown, explicit uncertainty and synthesis. A runtime or formal specification remains outside scope.

Declared: [YAIMLACP](YAIMLACP.md) supplies optional serverless coordination with scoped affirmative approval. Its owner preserves startup consideration, disclosure, limits and confirmation rules; no server or installation is authorized.

Declared (maintainer direction, October 2026): YAIML is context/project management with a one-prompt minimum interaction. Assume a new user and agent have no YAIML context or maintainer checkout. The small seed immediately retrieves guidance, establishes memory and embeds discoverable `yaiml-` skills. Ordinary work uses and maintains context automatically; optional commands such as `yaiml-to-do 10` and `yaiml-audit` select the same methods. Compose requested work without command choreography. Grow useful knowledge and methods, preserving local adaptations during refresh. Keep YAIML-owned material in `.yaiml/`, with supported host/public entry points outside. Distinguish local development snapshots from published references.

Declared: personal public project; require credit, permit commercial/client use, prohibit selling YAIML or charging for forks. Preserve [independence](PROJECT_INDEPENDENCE.md); exclude employer-confidential material, secrets, private transcripts and private-project dependencies. [Licensing](../LICENSE.md) preserves earlier grants. Invent no professional conclusions.

Declared (maintainer direction, October 2026): stamp YAIML-managed Markdown per material iteration; audit all affected project paths in core `changes.md`. Use YAIML major, local counter and random tag, preserving concurrent lineage. Updaters must establish prospective legacy baselines. [Versioning](VERSIONING.md) owns the method; no-op/read-only work stays unchanged.

Declared (maintainer direction, October 2026): reduce repeated rules and normal-work overhead without losing context, evidence or maintenance. Put shared mechanics in one owner and test an unfamiliar adopter. The maintainer reports no known independent adoption; internal installations/trials do not establish outside use. Preserve project-specific constraints during consolidation.

## Current State And Evidence

This project develops and uses YAIML; [Architecture](ARCHITECTURE.md) separates product resources from repository memory. Experimental [0.4.0](RELEASE.md) supplies eleven methods plus an alias, seven optional prompts, eleven starters and four core roles. Latest working files remain canonical; commits identify provenance, not deployment. The [Maintainer Guide](MAINTAINER_GUIDE.md) covers source and adopter reviews.

[Bootstrap](BOOTSTRAP.md) connects hosts; fifteen internal installations have twelve entries. Earlier CLI trials cover published setup, ordinary work, custom growth, composition, refresh and header repair. The new ShelfList draft trial used the shared loop without ritual skill-body reads: feature work and a conversational decision updated memory, revisions and path audits; fresh recall preserved files. It exposed a stale activation note; one corrected replay replaced it while retaining untested scope. [Current review](COLD_START_REVIEW.md) records conditions, assistance and remaining gaps; [upgrade guidance](ADOPTION_AND_UPGRADES.md#existing-yaiml-update) explains repair.

The [YTMMOCC case](case-studies/YTMMOCC.md) and [local adoption exercises](case-studies/ADOPTION_TRIAL.md) contain dated maintainer-owned evidence. The [current review](COLD_START_REVIEW.md) describes this repository's latest changes and verification limits. Neither establishes independent adoption or productivity gains.

## Active Risks And Gaps

- **Under-pruning:** earlier local review reported a roughly 22,000-word SoT with an inbox instruction and architecture accumulating in another project's state document. The causal explanation is a hypothesis, not a controlled result. Recovery and recurrence must be measured after updating adopter instructions.
- **Consumer compatibility:** ShepAIrd's local repair reads migrated YAIML/Chaitroom memory and retains root-layout support. It does not ingest changes.md yet. Its ARCS migration still emits an unquoted version. [Current portfolio evidence](COLD_START_REVIEW.md#portfolio-compatibility-and-disclosure) scopes verified compatibility; broader consumers, deployment and historical aggregates remain unverified.
- **Historical disclosure:** selected current ShepAIrd memory and registry values contain no actual machine-specific locations under the targeted check. Earlier exposure/history remains unassessed; this is not comprehensive secret detection or proof of safety.
- **Concurrent work:** team-scale merge burden and agent adherence remain unmeasured. Textual conflict resolution does not establish consistent meaning or combined verification.
- **Effectiveness:** controlled effectiveness comparison, independent adoption and token savings remain unestablished. Maintainer support here can mask newcomer friction. Maintenance reliability, recurring pruning and coordination safety remain unproven; total cost remains incomplete.
- **Evidence and authority:** agents can promote inference or internally consistent tests into correctness and flatten contributor conflicts. A maintainer-reported depth-order regression motivated stronger independent-check guidance; its cause was not inspected here and prevention remains untested. Preserve sources, intended behavior, and unresolved disagreements.

## Immediate Priorities

1. Broaden fresh-session revision/audit coverage to legacy baselines, interruption and concurrent reconciliation. Repeat ordinary maintenance across longer sequences and other hosts; one corrected replay cannot establish reliability. Extend non-code and partial-update trials.
2. Assess remaining migration/version compatibility and historical disclosure before broader rollout. Keep current working-copy measurements separate from historical deployment claims.
3. Use a working isolated runner for the [prepared comparison](EVALUATION.md#ready-to-run-comparison) and [new-reader demo](examples/minimal-notes/README.md#short-paste-and-go-demo). Measure total context cost, missed reads/writes, and misunderstandings.
4. Run the [concurrent-contributor check](EVALUATION.md#concurrent-contributor-check), then obtain an owner-led trial outside the maintainer's projects and another agent environment. Measure unrelated diff churn and lost constraints.
5. Measure recurring maintenance and under-pruning in an authorized adopter. Change guidance from observed failures; avoid accumulating speculative rules.

## Open Questions

Should discovery become essential rather than strongly recommended? Which supporting roles recur enough to warrant templates? What evidence and participation justify the [maturity milestones](ROADMAP.md)? Does YAIMLACP coordination improve outcomes enough to justify its cost over one-agent work? Could `yaiml-git` inform the maintainer's semantic merge tool for conflicting branch memory? That connection is exploratory; no tool integration is established.

Retired approaches belong in [Architecture](ARCHITECTURE.md). [changes.md](changes.md) retains revision records; Git holds exact diffs. Current memory retains actionable understanding.
