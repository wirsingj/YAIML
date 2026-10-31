---
yaiml-revision: "0.46.42a0394f3a2abb59"
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

YAIML means Yet Another AI Markup Language: a lightweight Markdown convention for project-owned context shared by humans and agents. Preserve that identity as skills and integration evolve; aim for clarity and portability across fields and tools. The maintainer endorses “softerware”: agents read, act, check results and maintain understanding. YAIML is a document standard for memory, change records, skills and init. Semantic-merge tools, gatekeepers and CI validators are external consumers; this repository defines integration contracts, not adopter tooling. Broader-domain usability remains unverified.

Declared: pursue adoption as an early public experiment: no installation, ordinary Markdown, explicit uncertainty and synthesis. Runtime/formal specification remain outside scope.

Declared: [YAIMLACP](../reference/YAIMLACP.md) owns optional serverless coordination: startup consideration, disclosure, limits and scoped affirmative confirmation; no server or installation.

Maintainer direction: one prompt establishes context and discoverable `yaiml-` skills without prior YAIML knowledge or a maintainer checkout. Normal work maintains context without reminders; named skills are optional. All init forms supply only agnostic guidance/templates and notices/provenance. The approved `reference/` distribution is separate from this repository's own `.yaiml/` memory; consumers need no self-use exceptions. Adopter layouts and local adaptations survive. Offline and networked init are peers. Networked acquisition resolves `refs/tags/latest` once to a commit, never a same-named branch; alternate sources require explicit requests. Feature work stays on feature branches; `main` is stable development, and approved main updates advance the public-ready `latest` tag. No GitHub Release is required; numbered tags stay fixed.

Declared: personal public project; require credit, permit commercial/client use, prohibit selling YAIML or charging for forks. Preserve [independence](PROJECT_INDEPENDENCE.md); exclude employer-confidential material, secrets, private transcripts and private-project dependencies. [Licensing](../LICENSE.md) preserves earlier grants. Invent no professional conclusions.

Maintainer direction: [Versioning](../reference/VERSIONING.md) stamps changed YAIML Markdown and audits all affected paths, preserving concurrent lineage through major/local-counter/random-tag revisions. Updaters establish prospective legacy baselines; no-op/read-only work stays unchanged.

Stabilization direction: no new features; check regressions and reading/maintenance overhead before merging. Keep shared mechanics in one owner, one workflow without a mode switch, and existing Git guidance for review preparation. Preserve context, evidence and project-specific constraints. No independent adoption is known; the maintainer's brother's feedback is pending.

## Current State And Evidence

This project develops and uses published experimental [0.5.2](RELEASE.md), separating reusable `reference/` material from source memory and resolving exact public tags. Target releases remain independent of YAIML versions/stamps; 0.4.0 remains the earlier published comparison baseline. The authorized complete commit and merge finished on 2026-10-31. At merge `91c8307120215a499c4e7fd0801c0b5db70f98f5`, the live latest-tag workflow succeeded and all 39 public README/license/reference files matched Git blobs. Fresh-session acceptance of this layout remains incomplete.

[Current review](COLD_START_REVIEW.md) separates published/draft trials and retains corrected failures. One comparison pair found no advantage. [Simulated readers](COLD_START_REVIEW.md#simulated-newcomer-reading) informed README's starting point, recall check and saved-context example; human usability remains unverified. [Upgrade guidance](ADOPTION_AND_UPGRADES.md#existing-yaiml-update) explains repair.

[Current publication review](COLD_START_REVIEW.md#052-publication-review) covers the combined work against actual main. The README foregrounds starting projects, readable documents and included skills, with direct full/offline prompt links. Earlier [0.5.0 stabilization evidence](COLD_START_REVIEW.md#stabilization-against-main) retains its tested scope. Ordinary traces overread versioning despite selective-loading guidance; this publication review adds no fresh-agent trial.

## Active Risks And Gaps

- **Distribution boundary:** an [inspected adopter](COLD_START_REVIEW.md#adopter-distribution-boundary) exposed source-artifact leakage; follow-up found prefilled source revision IDs in offline templates and stale README init. The approved structural separation corrects these; consumer guidance needs no source memory. Prior checks did not catch the full entry surface. Fresh-agent adoption/repair remains unverified; the existing adopter is unchanged. Source review still needs compression.

- **Under-pruning:** local review reported a roughly 22,000-word SoT with an inbox instruction, and architecture accumulating in another project's state document. Causation remains hypothetical; measure recovery and recurrence after instruction updates.
- **Consumer compatibility:** ShepAIrd reads migrated and root-layout memory, but omits the audit role, misses revision-first frontmatter without discovery, and writes continuation notes without advancing revisions/audits. ARCS cleanup still emits an unquoted label. [Portfolio evidence](COLD_START_REVIEW.md#portfolio-compatibility-and-disclosure) separates passing discovery checks from these reproduced gaps; broader consumers remain unverified.
- **Historical disclosure:** targeted current ShepAIrd files are clear of location-pattern matches; a profile path remains retrievable in public registry history. No history repair was authorized or performed. The check is not comprehensive secret detection.
- **Concurrent work:** [unified records](../reference/CHANGE_RECORDS.md) use declared ownership; silent cross-host overlap cannot be excluded. Competing consolidators still conflicted in Git exercises, and clean record merges retained unresolved authority. Revert/interruption repairs were lead-performed. At 10,000 records, receipt/listing output exceeded 537 KB; local comparison avoids reading that output into context but does not establish sustained scalability. Core-only consumers need pending corrections. General code reconciliation remains outside scope.
- **Effectiveness:** effectiveness gains, independent adoption and token savings remain unestablished. Maintainer support here can mask newcomer friction. Maintenance reliability, recurring pruning and coordination safety remain unproven; total cost remains incomplete.
- **Evidence and authority:** agents can promote inference or internally consistent tests into correctness and flatten contributor conflicts. A maintainer-reported depth-order regression motivated stronger independent-check guidance; its cause was not inspected here and prevention remains untested. Preserve sources, intended behavior, and unresolved disagreements.

## Immediate Priorities

1. Verify both published 0.5.2 init forms and existing/adapted-copy repair in fresh sessions. Artifact checks and verified public retrieval do not establish fresh-agent setup or recall.
2. [StateMesh and document trials](EVALUATION.md#statemesh-against-actual-local-main-2026-10-24) cover manual upgrade/writer checks, one live synthetic code candidate and a supplied document merge with rejection controls. Actual-branch testing found both local StateMesh versions blocked by synthetic branch/file contracts; autonomous document merging and repeated reliability remain unverified. Run the [bounded additional-host trial](EVALUATION.md#post-review-cross-host-trial-gate-2026-10-24) for both init variants, ordinary maintenance and fresh recall. Claude Code/Copilot were unavailable here; manual offline file checks establish no new host reliability. Public pinned retrieval passed for 0.5.2; it adds no broader-host behavioral evidence. Retain broader source-selection, interruption/revert and longer-sequence evidence gaps.
3. Repair ShepAIrd's reader/writer revision gaps and decide historical-disclosure handling before broader rollout; distinguish current-file, history and deployment evidence.
4. Repeat the [comparison](EVALUATION.md#ready-to-run-comparison) with equivalent ordinary docs and setup cost; seek [new-reader](examples/minimal-notes/README.md#short-paste-and-go-demo) and independent owner feedback.
5. Measure recurring maintenance and under-pruning in an authorized adopter; change guidance from observed failures.

## Open Questions

Should discovery become essential rather than strongly recommended? Which supporting roles recur enough to warrant templates? What evidence and participation justify the [maturity milestones](ROADMAP.md)? Does YAIMLACP coordination improve outcomes enough to justify its cost over one-agent work? Which external consumers will use the record integration contract? Semantic merging and validation tooling are outside this repository; investigate YAIML-induced friction within document scope.

Retired approaches belong in [Architecture](ARCHITECTURE.md). [changes.md](changes.md) retains revision records; Git holds exact diffs. Current memory retains actionable understanding.
