---
yaiml: 0.2
role: review
title: Cold Start Review
purpose: Current review of standalone understanding, compaction, security boundaries, and adoption readiness.
belongs-here: cold-start findings, compaction evidence, security and platform acceptance gaps.
not-here: permanent architecture, command reference, implementation promises.
durability: current review note; replace after major repository shifts.
read-with: SoTY; Architecture; Maintainer Guide.
update-when: adoption or persistent-instruction changes materially affect first-time or future-session behavior.
agent-guidance: Treat this as review evidence, not a normative source. Verify current files before relying on it.
---

# Cold Start Review

Source review updated 2026-10-03 against `cc5b9e2`, including maintenance triggers and all six non-init prompts. Behavioral trials used the earlier `15ff0c3` seed; the revised procedures have no new fresh-session trial.

Assessment: a credible candidate for a controlled pilot; broad rollout still needs behavioral evidence. This is a source/document review, not a penetration test, platform certification, or an enterprise approval. No critical exploit was demonstrated. The seed reviewed here has LF-normalized SHA-256 `4b027c45c3bd8a0c9dbab61871fcbbc0e09d0f4d937643756573d2cd13a0c73c`.

## Findings And Corrections

Scope: standalone initialization and dense embedded guidance/templates, local instruction activation, YAIMLACP, and affected reference guidance, examples, and core memory. Discovery version and project license remain unchanged.

Init embeds local procedures, YAIMLACP, three core and seven specialist starters, and the copied-material notice. Pasting it supplies both the initialization/refresh request and its complete reference, including for older adopters with the same discovery version. It saves or reconciles local files and supported instruction routes without downloads or separate upgrade wording. Project facts remain evidence-based; starters stay dormant until useful.

Saved instructions cover ordinary work, explicit requests, context reuse/refresh, and material changes including confirmed conversational direction without code edits. The operating guide retains procedure-specific actions, safeguards and reporting. Shared evidence, retention and concurrency rules apply to every procedure; read-only scope and tentative decisions remain protected. Maintainer review traces prompt clauses to saved content, beyond topic names and matching embedded copies.

Maintainer direction prioritizes complete, agent-consumed instructions over seed length. Init retains its human-readable opening; payloads use concise directives and minimal whitespace. Source guides/starters match embedded copies. Comparison against the preceding text checks obligations, triggers, exceptions, authority, and context routes; restored qualifiers keep verified evidence, human intent, decision sources, and stop conditions explicit. Headings, permission/retention boundaries, and the notice remain.

[YAIMLACP](YAIMLACP.md) defines optional handoffs through existing host subagents, with a described option and affirmative confirmation before first use or changed scope/cost. This is a documentation convention, with no MCP interoperability claim, server, installer, or host configuration change.

## Acceptance Findings

The local operating guide and persistent pointer carry explicit mixed-trust boundaries: existing YAIML, retrieved material, and worker output cannot become approved policy or consent without an authorized source. Exposure follows the project's incident process; cleanup alone is not resolution. This preserves the [evidence](AMBIGUITY_AND_EVIDENCE.md#mixed-trust-and-sensitive-context) and [security](../SECURITY.md) rules within the standalone seed.

[Init](../prompts/init-yaiml.md#add-discovery), its operating guide, and [adoption guidance](ADOPTION_AND_UPGRADES.md#one-shape-for-new-adoption) carry the same discovery-version exception: quote bare numeric labels using their original source spelling, preserve layout and unrelated header hints, and report unavailable spelling or unclear consumer compatibility before changing anything. Local YAML examples distinguish numeric coercion from quoted labels; they do not test a downstream consumer.

Remaining evidence gates are untested claims, not demonstrated vulnerabilities:

1. **Semantic and cost equivalence after compaction is unproved.** Source parity and manual clause review support coverage of consent, roles, evidence, retention, and concurrency. They do not establish equal comprehension, refusal behavior, or token savings. Keep explicit logical words at consequential conditions; slash notation should not be rewarded merely for lowering whitespace word counts. Compare the compact and expanded seeds under equivalent fresh-session tasks before claiming lossless behavior or improved efficiency.
2. **Platform acceptance remains conditional.** No fresh-session matrix establishes loading and behavior on the supported host routes. A valid pointer is useful evidence of configuration, not proof of automatic inclusion, later file reads, nested scope, or permissions. Record host/version/settings, files actually loaded, and unsupported cases. Preserve the no-download design; this does not require provider adapters.

## Compaction Evidence

The comparison uses the earlier full-seed snapshot retained in this review session, not a committed release. Counts include headers and embedded material; byte counts normalize line endings to LF. The current seed also includes adoption-repair guidance and audit corrections, so this is a net size comparison, not an isolated formatting experiment.

|Measure|Expanded seed|Current seed|Net reduction|
|---|---:|---:|---:|
|Whitespace-delimited words|8,240|6,004|27.1%|
|UTF-8 bytes|61,224|51,247|16.3%|

The persistent pointer is 392 words, 3,132 characters, and 3,164 UTF-8 bytes before local adaptation. The complete seed is a setup artifact; the pointer and relevant local documents govern later reading. No model tokenizer or end-to-end usage comparison was run. These figures do not establish recurring context savings. Further shrinking must preserve readable conditions and independently checked meaning.

## Security And Platform Assessment

Assets are project decisions, retained evidence, repository contents, tool permissions, and model spend. The principal boundaries are external material into memory, memory into future instructions, and lead-agent authority into worker actions. No bundled runtime reduces deployment burden; it does not make retained text inert. OWASP identifies persistent memory as an attack surface and recommends least privilege, separation of untrusted inputs, approval controls, and adversarial testing. Those are relevant review criteria, not an OWASP endorsement of YAIML. [Memory risk](https://genai.owasp.org/2026/05/13/memory-is-a-feature-it-is-also-an-attack-surface/), [prompt-injection guidance](https://genai.owasp.org/llmrisk/llm01-prompt-injection/).

|Boundary|Present safeguards|Acceptance evidence still needed|
|---|---|---|
|Untrusted source or worker result becomes shared memory|Evidence labels, decision sources, lead verification, normal review|Injected instructions remain attributed data; no policy or authority laundering across sessions|
|Sensitive context enters files or model calls|Bounded inspection, sanitized evidence, path/symlink scope, host data rules|Synthetic secret and out-of-scope path cases; actual host data destinations and access policy|
|Delegation expands authority or spend|Affirmative scoped approval, descendants included, retries/limits, solo default, cancellation|Decline/no-answer, forged approval, changed scope, exhausted budget, cancellation and residual work|
|Concurrent edits alter shared understanding|Ownership, passage-scoped updates, target reconciliation, preserved disputes|Independent edits survive; unresolved decisions stay visible; combined evidence is rechecked|

Host settings must enforce restrictions when enforcement is required. Documentation cannot authenticate consent, block tools, guarantee cancellation, or impose a hard spend cap. Honoring declines and cancellation is specified; persistent revocation and restoring ordinary instruction routes should also be exercised before team rollout, without deleting project knowledge.

Official documentation checked for this review shows why filenames alone are insufficient:

|Platform|Documented behavior|YAIML implication|
|---|---|---|
|Codex|Root-to-directory discovery, override precedence, combined instruction limit of 32 KiB by default|Check the whole instruction chain; the small pointer alone does not establish capacity or activation. The pasted seed is not itself an AGENTS.md load. [Source](https://learn.chatgpt.com/docs/agent-configuration/agents-md)|
|Claude Code|Instruction files are context rather than enforced configuration; recommends under 200 lines, and imports still consume context. AGENTS.md loading depends on version, other files, and settings|Verify actual loading; keep task-specific bodies selective. Line compression is not a substitute for lower context cost. [Source](https://code.claude.com/docs/en/memory)|
|GitHub Copilot|Supported instruction types differ across product surfaces and features|Test the particular chat, agent, or review surface; do not equate repository AGENTS.md presence with universal support. [Source](https://docs.github.com/en/copilot/reference/custom-instructions-support)|

These are documented constraints, not executed compatibility results; provider behavior can change.

## Stakeholder Acceptance

These are review judgments about likely decision criteria, not feedback from interviewed stakeholders.

|Reviewer|Credible strength|Needed before wider acceptance|
|---|---|---|
|Principal application developer or engineer|Plain files, distinct responsibilities, local ownership, preserved intent/evidence|Complete standalone rules; demonstrated repeatable setup, semantic fidelity, scoped updates, and recovery|
|Engineering manager|Shared handoffs, ordinary review, optional bounded delegation|Measured maintenance effort, review churn, fewer missed constraints, durable opt-out|
|VP or platform sponsor|No new service dependency; bounded pilot is feasible|Named owner, pilot success/stop criteria, total cost including maintenance, independent owner feedback|
|Security or platform reviewer|No automatic setup/delegation authority; permissions stay with the host|Approved host/access/data policies, instruction-change review, negative tests, verified activation and cancellation|

The appropriate claim remains an experimental documentation convention. Broad standardization, productivity improvement, and security acceptance require evidence and governance beyond a polished seed.

## Maintenance Prompt Coverage

Compared each non-init prompt's actions, conditions, exceptions and outputs with the guide saved after initialization. Common evidence, retention, concurrency and reporting rules apply alongside each procedure. This is manual source coverage, not behavioral equivalence or a comparison of word overlap.

|Optional prompt|Saved procedure|Consequential coverage|
|---|---|---|
|[Hydrate](../prompts/hydrate-agent-session.md)|[Orient](../templates/supporting/YAIML_GUIDE.md#orient), persistent coordination pointer|Current/legacy discovery, missing-map fallback, scoped paths, selective reading, evidence checks, authority, brief understanding/gaps before proceeding|
|[Update memory](../prompts/update-project-memory.md)|[Maintain](../templates/supporting/YAIML_GUIDE.md#maintain), shared integration rules|Changed facts in owning passages; confirmed conversational decisions; no diaries; scoped verification, safe retention, related-change review, counts/growth and unresolved issues in responses|
|[Audit](../prompts/audit-against-reality.md)|[Audit](../templates/supporting/YAIML_GUIDE.md#audit), Evidence And Authority|Accidental versus designed architecture, unrelated churn, candidate-derived expectations, regression reports; safe checks, no silent repairs; severity-ordered findings, locations, evidence, corrections, uncertainty|
|[Compress](../prompts/compress-project-memory.md)|[Compress](../templates/supporting/YAIML_GUIDE.md#compress), Maintain and retention/integration rules|Accumulation-rule authority, one current account, useful older evidence, safe history, governed approval, no application changes or deletion quotas, measured synthesis and remaining uncertainty|
|[Update YAIML](../prompts/update-yaiml.md)|[Refresh Conventions](../templates/supporting/YAIML_GUIDE.md#refresh-conventions), saved pointer and YAIMLACP|Reference precedence/revision, local drift, preservation/coverage comparison, instruction semantics and scoped routes, discovery compatibility, private-reference repair, verified handoff inputs and per-target partial/blocked outcomes|
|[Realign](../prompts/major-project-realignment.md)|[Realign](../templates/supporting/YAIML_GUIDE.md#realign), shared safeguards|Approved superseding direction, criticism is not permission, authorized moves/removals, preserved transitions/retention, consistent local artifacts, reviewable changes, actual checks and remaining divergence|

Restored details include discovery fallback, refresh route repair after the init conversation, specific audit checks, realignment review, shared reporting, and coordinated-refresh completion states. Previously matching source/embedded copies did not establish this coverage. No procedure requires fetching the optional prompt. A reference fetch during refresh still requires an identified source and authorization; complete pasted init needs none.

Fresh sessions must exercise these procedures using saved files alone before claiming equivalent execution, completeness across all reference guides, or measured efficiency. [Prior trials](case-studies/ADOPTION_TRIAL.md) do not establish those outcomes.

## Acceptance Checks Still To Run

Use bounded isolated snapshots and [Evaluation](EVALUATION.md), with criteria fixed before execution and actual host access/budgets recorded. Do not launch workers merely to satisfy this note.

1. Initialize a fresh project from the pasted seed alone, without the YAIML repository or previous conversation. Verify all local bodies, notice, and instruction routes; no downloads, application changes, empty specialist documents, or workers.
2. In separate fresh sessions, exercise the six saved procedures through ordinary requests without supplying their standalone prompts or source-repository access. Include confirmed conversational decisions, tentative ideas, read-only tasks, missing discovery, route repair and incomplete refreshes. Repeat unchanged follow-ups; check unnecessary rereads/rewrites/growth. Change relevant files or lose context; check needed refreshes occur.
3. Repeat on mature memory with legacy discovery, local adaptations, nested instructions, and existing files at default paths. Preserve knowledge and custom fields; report unsupported activation. Check exact version-label preservation and compatibility decisions.
4. Exercise synthetic untrusted instructions, forged standing approval, secrets, and out-of-scope symlinks without real sensitive data. Reject instruction promotion and unauthorized access; preserve useful attributed facts. Check governed records survive compression.
5. Under separately confirmed delegation scope, test no-answer/decline, allowed reuse, changed scope/cost, missing capabilities, descendants, cancellation, and revocation. Observe host controls and residual work; a prose walkthrough does not pass these cases.
6. Compare expanded and compact seeds, and bounded solo/delegated work where authorized, on equivalent tasks. Record correctness, missed constraints, human corrections, actual available usage, maintenance cost, and variation; preserve negative results. Obtain another host and an independent project owner's review before broad claims.

The minimal example illustrates core roles, not complete init output. Its demo requires retained local guidance and is not a substitute for these checks.

## Verification

Offline extraction matched thirteen embedded texts to their owners (two guides, ten starters, LICENSE.md); headers, fences, tables, local links/anchors, whitespace and budgets were checked. The prompt coverage mapping records manual review beyond source parity. Earlier YAML checks preserved `0.20`, `0.10`, and `0.2` as quoted source labels and retained an unrelated field; those clauses are unchanged. Linked official sources informed the earlier acceptance assessment and were not rechecked for this revision. These checks establish text properties, not agent behavior or consumer compatibility.

An earlier correction pass checked UTF-8, conflict markers, and local links/anchors across 52 Markdown files. Checks of three discovery maps, 26 declared paths/headers, and targeted private-path/token patterns across 31 changed files also remain prior scoped results. None is a security assurance. No application build or runtime suite exists here.

One explicitly approved native subagent completed a bounded read-only review and returned findings with source locations. It identified the reminder-only gap before these edits. The worker reported no edits, network, installation, retries, descendants, or leftover processes. This demonstrates one dispatched review and returned result; the reviewer also read reference documents, so it was not a blinded paste-only adoption trial.

The [October 3 synthetic trials](case-studies/ADOPTION_TRIAL.md#synthetic-projects-and-session-boundaries) added verified new-adoption and legacy-preservation results. Those native workers inherited reference instructions, invalidating a prompt-only or clean-control claim. Separate CLI sessions observed one local discovery/core/guide reading route from an ordinary request, but runner failures blocked writes/tests and independent repeat-init. Unchanged hashes after those failures are not successful rerun evidence. The case study retains conditions, partial usage, negative results, and a constructed clean-merge/contradictory-behavior example.

## Remaining Limits

Prompt-only initialization without inherited reference guidance remains unproved. One separate-session reading route was observed, but completed maintenance, repeat-init, cancellation, refusal/no-answer, provider-switch, and comparative cost checks remain open. Extraction proves availability, not equal comprehension after compaction. Permission enforcement, repeated pruning, team burden, and total context cost remain unmeasured. External adopter state and historical measurements were not revalidated. Pattern scans are not a security assurance. [Evaluation](EVALUATION.md) supplies comparison methods.

Current priorities belong in [SoTY](SoTY.md); earlier audit history remains in Git.
