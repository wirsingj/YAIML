---
yaiml-revision: "0.56.7665a059b603a2d9"
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

Include any [pending corrections](changes.md).

## North Star And Human Direction

YAIML means Yet Another AI Markup Language: project-owned understanding in ordinary Markdown files, shared by humans and agents. Maintainer direction: lead with file-based memory, independent of a chat/model; explain missing concepts and remove redundancy. Preserve portability across fields/tools. “Softerware” means agents read, act, check and maintain understanding. Memory, records, skills and init serve that purpose. Semantic-merge tools, gatekeepers and CI validators are external consumers; this repository defines integration contracts, not adopter tooling. Broader-domain usability remains unverified.

Declared: pursue adoption as an early public experiment: no installation, ordinary Markdown, explicit uncertainty and synthesis. Runtime/formal specification remain outside scope.

Declared: [YAIMLACP](../reference/YAIMLACP.md) owns optional serverless coordination: startup consideration, disclosure, limits and scoped affirmative confirmation; no server or installation.

Maintainer direction: one prompt establishes context and discoverable `yaiml-` skills without prior YAIML knowledge or a maintainer checkout. Normal work maintains context without reminders; named skills are optional. Init supplies only agnostic guidance/templates and notices/provenance. Product navigation comes first: `reference/` is reusable material, `docs/` explains and evaluates it, `examples/` illustrates it, and root `ROADMAP.md` exposes direction. Our `.yaiml/` is ordinary project usage: current context, audit and local methods, not product documentation storage. Discovery links outward without relocating artifacts. Adopter layouts/adaptations survive; offline and networked init are peers. Networked acquisition resolves `refs/tags/latest` once to a commit; alternatives require explicit requests. Work batches use revision-cycle branches, reviewed when ready; product-version bumps are separate decisions. Approved stable-main updates advance public-ready `latest`, without a GitHub Release; numbered tags stay fixed.

Declared: personal public project; require credit, permit commercial/client use, prohibit selling YAIML or charging for forks. Preserve [independence](../docs/PROJECT_INDEPENDENCE.md); exclude employer-confidential material, secrets, private transcripts and private-project dependencies. [Licensing](../LICENSE.md) preserves earlier grants. Invent no professional conclusions.

Maintainer direction: [Versioning](../reference/VERSIONING.md) stamps changed YAIML Markdown and audits all affected paths, preserving concurrent lineage through major/local-counter/random-tag revisions. Updaters establish prospective legacy baselines; no-op/read-only work stays unchanged.

Stabilization remains the default; the maintainer approved optional diagram output as a bounded addition, then requested a whole-project alignment and complexity review, not another feature-only check. Preserve one workflow without a mode switch and existing Git review guidance. Evaluate additions by whether they help recover and maintain project understanding, including their reading/maintenance cost. No independent adoption is known; the maintainer's brother's feedback is pending.

## Current State And Evidence

The optional [diagram method](../reference/skills/yaiml-diagram/SKILL.md) adds editable draw.io views, portable notes and a native route. [Checks](../docs/evaluation/COLD_START_REVIEW.md#diagram-skill-review) cover package closure, rendering, valid relative geometry and a controlled update fixture; fresh-session behavior remains unverified.

The maintainer approved experimental [0.6.0](../docs/development/RELEASE.md) for the diagram/clarity batch after its merge. Bootstrap and offline provenance use that label; record semantics, discovery and local revision major are unchanged. [Publication evidence](../docs/evaluation/COLD_START_REVIEW.md#revision-batch-audit) verifies the pre-label batch at `0273501`, not fresh-session acceptance. The earlier 0.4.0 comparison remains separately scoped; target releases stay independent.

Product-first navigation was verified in `main` at `7b4bee8`. Keep the public tone approachable, professional and prompt-first. Supporting project context still belongs in memory when useful; no fixed file limit is implied. The [pre-merge audit](../docs/evaluation/COLD_START_REVIEW.md#revision-batch-audit) tightened offline route coverage and decision checks; its artifact results do not establish publication or fresh-agent acceptance.

[Current review](../docs/evaluation/COLD_START_REVIEW.md) distinguishes published/draft trials and corrected failures. One comparison pair found no advantage; simulated readers informed README, not human usability proof. [StateMesh trials](../docs/evaluation/EVALUATION.md#statemesh-against-actual-local-main-2026-10-24) retain bounded synthetic/manual evidence; both inspected CLIs failed actual-branch inputs. External consumers are not adoption dependencies.

## Active Risks And Gaps

- **Process weight:** mandatory stamps, exact-path records and incorporation receipts add work beyond the memory loop. [Ordinary trials](../docs/evaluation/COLD_START_REVIEW.md#stabilization-against-main) overread versioning despite selective-loading guidance. Review assessment: simplify the ordinary path before expanding it; benefit over equivalent ordinary docs and total overhead remain unestablished. The approved record contract is not silently optional.
- **Presentation gaps:** both teaching families are labeled legacy, leaving no completed current-init example. Current wording now distinguishes file storage, agent execution, host routing and normal team review; clearer prose alone establishes no new behavior.
- **Distribution boundary:** [inspected leakage](../docs/evaluation/COLD_START_REVIEW.md#adopter-distribution-boundary), offline source IDs and stale README init motivated structural separation. Earlier checks missed the full entry surface. Fresh-agent adoption/[repair](../docs/ADOPTION_AND_UPGRADES.md#existing-yaiml-update) remains unverified; the existing adopter is unchanged.

- **Under-pruning:** local review reported a roughly 22,000-word SoT with an inbox instruction, and architecture accumulating in another project's state document. Causation remains hypothetical; measure recovery and recurrence after instruction updates.
- **Consumer compatibility:** ShepAIrd reads migrated and root-layout memory, but omits the audit role, misses revision-first frontmatter without discovery, and writes continuation notes without advancing revisions/audits. ARCS cleanup still emits an unquoted label. [Portfolio evidence](../docs/evaluation/COLD_START_REVIEW.md#portfolio-compatibility-and-disclosure) separates passing discovery checks from these reproduced gaps; broader consumers remain unverified.
- **Historical disclosure:** targeted current ShepAIrd files are clear of location-pattern matches; a profile path remains retrievable in public registry history. No history repair was authorized or performed. The check is not comprehensive secret detection.
- **Concurrent work:** [unified records](../reference/CHANGE_RECORDS.md) cannot detect silent overlap. Competing consolidators conflicted; clean merges retained authority disputes. Revert/interruption repairs were lead-performed. [Receipt-growth checks](../docs/evaluation/COLD_START_REVIEW.md#concurrency-edge-cases-and-receipt-growth) do not establish sustained scalability. Core-only readers miss pending corrections; general code reconciliation stays outside scope.
- **Effectiveness:** effectiveness gains, independent adoption and token savings remain unestablished. Maintainer support here can mask newcomer friction. Maintenance reliability, recurring pruning and coordination safety remain unproven; total cost remains incomplete.
- **Evidence and authority:** agents can promote inference or internally consistent tests into correctness and flatten contributor conflicts. A maintainer-reported depth-order regression motivated stronger independent-check guidance; its cause was not inspected here and prevention remains untested. Preserve sources, intended behavior, and unresolved disagreements.

## Immediate Priorities

1. Verify both current init forms and existing/adapted-copy repair in fresh sessions, recording the exact tested source. Artifact checks and verified public retrieval do not establish fresh-agent setup or recall.
2. Run the [additional-host trial](../docs/evaluation/EVALUATION.md#post-review-cross-host-trial-gate-2026-10-24) for both init forms, ordinary maintenance and fresh recall. Claude Code/Copilot were unavailable; artifact/manual checks establish no host reliability. Retain source-selection, interruption/revert and longer-sequence gaps.
3. Track separately authorized ShepAIrd reader/writer repairs and the historical-disclosure decision before broader portfolio rollout; distinguish current-file, history and deployment evidence. These are external work, not prerequisites for independent YAIML use.
4. Repeat the [comparison](../docs/evaluation/EVALUATION.md#ready-to-run-comparison) with equivalent ordinary docs and setup cost; seek [new-reader](../examples/minimal-notes/README.md#short-paste-and-go-demo) and independent owner feedback.
5. Measure recurring maintenance cost and under-pruning in an authorized adopter. Apply the complexity review through focused clarification, current examples and source-memory synthesis; contract changes require an explicit decision, not another layer of rules.

## Open Questions

Should discovery become essential rather than strongly recommended? Which supporting roles recur enough to warrant templates? What evidence and participation justify the [maturity milestones](../ROADMAP.md)? Does YAIMLACP coordination improve outcomes enough to justify its cost over one-agent work? Which external consumers will use the record integration contract? Semantic merging and validation tooling are outside this repository; investigate YAIML-induced friction within document scope.

Retired approaches belong in [Architecture](ARCHITECTURE.md). [changes.md](changes.md) retains revision records; Git holds exact diffs. Current memory retains actionable understanding.
