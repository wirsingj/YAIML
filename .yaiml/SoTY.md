---
yaiml-revision: "0.39.cb85eb31d410d62d"
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

YAIML means Yet Another AI Markup Language: a lightweight Markdown convention for project-owned context shared by humans and agents. Preserve that identity as skills and integration evolve; aim for clarity and portability across fields and tools. The maintainer endorses “softerware”: agents read, act, check results and maintain understanding. YAIML is a document standard for memory, change records, skills and init. Semantic-merge tools, gatekeepers and CI validators are external consumers; this repository defines integration contracts and builds no tooling. Broader-domain usability remains unverified.

Declared: pursue adoption as an early public experiment: no installation, ordinary Markdown, explicit uncertainty and synthesis. Runtime/formal specification remain outside scope.

Declared: [YAIMLACP](YAIMLACP.md) owns optional serverless coordination: startup consideration, disclosure, limits and scoped affirmative confirmation; no server or installation.

Maintainer direction: one prompt establishes context and discoverable `yaiml-` skills without prior YAIML knowledge or a maintainer checkout. Hands-off context maintenance during normal work is the default; users need no YAIML reminders or manual memory upkeep. Named skills are optional controls, not a required interaction model. Grow knowledge/methods while preserving local adaptations. Keep YAIML-owned material in `.yaiml/`, except supported host/public entries. Offline and networked init are first-class peers. Default networked acquisition must use a reviewed release ref; floating `main` is only for explicitly requested testing. Alternatives require explicit requests. Distinguish drafts from published references.

Declared: personal public project; require credit, permit commercial/client use, prohibit selling YAIML or charging for forks. Preserve [independence](PROJECT_INDEPENDENCE.md); exclude employer-confidential material, secrets, private transcripts and private-project dependencies. [Licensing](../LICENSE.md) preserves earlier grants. Invent no professional conclusions.

Maintainer direction: [Versioning](VERSIONING.md) stamps changed YAIML Markdown and audits all affected paths, preserving concurrent lineage through major/local-counter/random-tag revisions. Updaters establish prospective legacy baselines; no-op/read-only work stays unchanged.

Stabilization direction: no new features; check regressions and reading/maintenance overhead before merging. Keep shared mechanics in one owner, one workflow without a mode switch, and existing Git guidance for review preparation. Preserve context, evidence and project-specific constraints. No independent adoption is known; the maintainer's brother's feedback is pending.

## Current State And Evidence

This project develops and uses YAIML; [Architecture](ARCHITECTURE.md) separates product from repository memory. Experimental [0.5.1 candidate](RELEASE.md) hardens offline adoption, pins acquisition and defines an external record contract; 0.4.0 remains the published comparison baseline. Working files are canonical; commits identify provenance, not deployment. The maintainer authorized review-branch commit/push and will integrate through an MR. Ask before subsequent pushes.

[Current review](COLD_START_REVIEW.md) separates published/draft trials and retains corrected failures. One comparison pair found no advantage. [Simulated readers](COLD_START_REVIEW.md#simulated-newcomer-reading) informed README's starting point, recall check and saved-context example; human usability remains unverified. [Upgrade guidance](ADOPTION_AND_UPGRADES.md#existing-yaiml-update) explains repair.

[Stabilization review](COLD_START_REVIEW.md#stabilization-against-main) found no new merge-blocking regression in source/package checks; methods match the corrected security trial. The post-review candidate supersedes default-main acquisition with a release pin; public availability awaits approved publication. Earlier 0.5.0 MR checks do not validate the new candidate. Ordinary traces overread versioning despite selective-loading instructions; no new agent trial accompanied publication preparation.

## Active Risks And Gaps

- **Two audiences:** [adopter trials](COLD_START_REVIEW.md#adopter-path-boundaries-and-partial-updates) exercised path boundaries, permitted external input, ordinary maintenance and updates. A partial-write audit overcount was corrected and replayed; native metadata writes remain host-restricted. These bounded traces do not prove general access enforcement. Source review still needs compression; its evidence is excluded from adopter context.

- **Under-pruning:** local review reported a roughly 22,000-word SoT with an inbox instruction, and architecture accumulating in another project's state document. Causation remains hypothetical; measure recovery and recurrence after instruction updates.
- **Consumer compatibility:** ShepAIrd reads migrated and root-layout memory, but omits the audit role, misses revision-first frontmatter without discovery, and writes continuation notes without advancing revisions/audits. ARCS cleanup still emits an unquoted label. [Portfolio evidence](COLD_START_REVIEW.md#portfolio-compatibility-and-disclosure) separates passing discovery checks from these reproduced gaps; broader consumers remain unverified.
- **Historical disclosure:** targeted current ShepAIrd files are clear of location-pattern matches; a profile path remains retrievable in public registry history. No history repair was authorized or performed. The check is not comprehensive secret detection.
- **Concurrent work:** [unified records](CHANGE_RECORDS.md) use declared ownership; silent cross-host overlap cannot be excluded. Competing consolidators still conflicted in Git exercises, and clean record merges retained unresolved authority. Revert/interruption repairs were lead-performed. At 10,000 records, receipt/listing output exceeded 537 KB; local comparison avoids reading that output into context but does not establish sustained scalability. Core-only consumers need pending corrections. General code reconciliation remains outside scope.
- **Effectiveness:** effectiveness gains, independent adoption and token savings remain unestablished. Maintainer support here can mask newcomer friction. Maintenance reliability, recurring pruning and coordination safety remain unproven; total cost remains incomplete.
- **Evidence and authority:** agents can promote inference or internally consistent tests into correctness and flatten contributor conflicts. A maintainer-reported depth-order regression motivated stronger independent-check guidance; its cause was not inspected here and prevention remains untested. Preserve sources, intended behavior, and unresolved disagreements.

## Immediate Priorities

1. Review the 0.5.1 hardening candidate and its local release ref before approving publication. Offline init, pinned acquisition, enterprise source guidance, reduced base, external record contract and pointer hygiene are implemented; fresh-session acceptance is incomplete. No push or publication without approval.
2. The [StateMesh manual upgrade](EVALUATION.md#statemesh-local-upgrade-trial-2026-10-24) passed bounded pre/post behavior checks and exposed incompatible generated records. An isolated Step 2 writer repair then passed 13/13 contract/behavior tests; original StateMesh remains unmodified. One bounded live Codex CLI candidate then passed 104 fixed gates and 10,000 selected comparisons, without committing; repeated reliability/document trials remain unrun. Run the [bounded additional-host trial](EVALUATION.md#post-review-cross-host-trial-gate-2026-10-24) for both init variants, ordinary maintenance and fresh recall. Claude Code/Copilot were unavailable here; manual offline file checks establish no new host reliability. Public pinned retrieval awaits approved publication. Retain broader source-selection, interruption/revert and longer-sequence evidence gaps.
3. Repair ShepAIrd's reader/writer revision gaps and decide historical-disclosure handling before broader rollout; distinguish current-file, history and deployment evidence.
4. Repeat the [comparison](EVALUATION.md#ready-to-run-comparison) with equivalent ordinary docs and setup cost; seek [new-reader](examples/minimal-notes/README.md#short-paste-and-go-demo) and independent owner feedback.
5. Measure recurring maintenance and under-pruning in an authorized adopter; change guidance from observed failures.

## Open Questions

Should discovery become essential rather than strongly recommended? Which supporting roles recur enough to warrant templates? What evidence and participation justify the [maturity milestones](ROADMAP.md)? Does YAIMLACP coordination improve outcomes enough to justify its cost over one-agent work? Which external consumers will use the record integration contract? Semantic merging and validation tooling are outside this repository; investigate YAIML-induced friction within document scope.

Retired approaches belong in [Architecture](ARCHITECTURE.md). [changes.md](changes.md) retains revision records; Git holds exact diffs. Current memory retains actionable understanding.
