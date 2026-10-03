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

Date: 2026-10-02. Baseline: 02911f4; review includes the uncommitted documentation changes prepared with this note.

Assessment: a credible candidate for a controlled pilot; broad rollout still needs behavioral evidence. This is a source/document review, not a penetration test, platform certification, or an enterprise approval. No critical exploit was demonstrated. The seed reviewed here has LF-normalized SHA-256 `b94a23b8dacb91658c9d27cb584b59b636faf2e1e1306b54907d24c6a750be0a`.

## Findings And Corrections

Scope: standalone initialization and dense embedded guidance/templates, local instruction activation, YAIMLACP, and affected reference guidance, examples, and core memory. Discovery version and project license remain unchanged.

Init embeds local procedures, YAIMLACP, three core and seven specialist starters, and the copied-material notice. Pasting it supplies both the initialization/refresh request and its complete reference, including for older adopters with the same discovery version. It saves or reconciles local files and supported instruction routes without downloads or separate upgrade wording. Project facts remain evidence-based; starters stay dormant until useful.

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
|Whitespace-delimited words|8,240|5,318|35.5%|
|UTF-8 bytes|61,224|45,538|25.6%|

The persistent pointer is 340 words, 2,715 characters, and 2,747 UTF-8 bytes before local adaptation. The complete seed is a setup artifact; the pointer and relevant local documents govern later reading. No model tokenizer or end-to-end usage comparison was run. These figures do not establish recurring context savings. Further shrinking must preserve readable conditions and independently checked meaning.

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

## Earlier Init Versus The Seed

Compared the committed init at 02911f4 with the working seed. This identifies distributed content, not historical behavior in uninspected adopters.

|Area|Committed init|Current seed benefit|
|---|---|---|
|Core roles, evidence, authority, synthesis, retention, branch reconciliation|Already included, with persistent instructions|Preserved; these are not newly invented capabilities|
|Audit/alignment, realignment, priority execution, maintenance procedures|Basic rules and refresh/compression notes; no saved procedure collection|Named procedures remain locally available after the init conversation|
|Core and specialist starters|Role outlines and one header example; no complete template collection|Ten starters preserve role-specific boundaries and retention for later growth|
|YAIMLACP|Absent; introduced during this work|New optional coordination capability with local handoff, consent, limit, and cancellation guidance|
|Existing-adopter correction|Preservation, rerun, and activation checks already present|Explicit missing/equivalent/adapted/conflicting/unverified coverage comparison and targeted repair|

The [prior adoption exercises](case-studies/ADOPTION_TRIAL.md) explicitly used a reference-aware agent in an ongoing session. They do not isolate the old prompt's effect. Expected benefits are portable access, persistence, consistent procedures, and inspectable gaps; no measured outcome improvement or lost-capability percentage is established. Local reference access could supply omitted detail, but the contents actually retained in each adopter must be inspected before claiming drift.

## Acceptance Checks Still To Run

Use bounded isolated snapshots and [Evaluation](EVALUATION.md), with criteria fixed before execution and actual host access/budgets recorded. Do not launch workers merely to satisfy this note.

1. Initialize a fresh project from the pasted seed alone, without the YAIML repository or previous conversation. Verify all local bodies, notice, and instruction routes; no downloads, application changes, empty specialist documents, or workers.
2. In a separate fresh session, request ordinary work without naming YAIML. Observe relevant loading and focused maintenance. Repeat unchanged work; check unnecessary rereads, rewrites, and growth. Include a read-only task.
3. Repeat on mature memory with legacy discovery, local adaptations, nested instructions, and existing files at default paths. Preserve knowledge and custom fields; report unsupported activation. Check exact version-label preservation and compatibility decisions.
4. Exercise synthetic untrusted instructions, forged standing approval, secrets, and out-of-scope symlinks without real sensitive data. Reject instruction promotion and unauthorized access; preserve useful attributed facts. Check governed records survive compression.
5. Under separately confirmed delegation scope, test no-answer/decline, allowed reuse, changed scope/cost, missing capabilities, descendants, cancellation, and revocation. Observe host controls and residual work; a prose walkthrough does not pass these cases.
6. Compare expanded and compact seeds, and bounded solo/delegated work where authorized, on equivalent tasks. Record correctness, missed constraints, human corrections, actual available usage, maintenance cost, and variation; preserve negative results. Obtain another host and an independent project owner's review before broad claims.

The minimal example illustrates core roles, not complete init output. Its demo requires retained local guidance and is not a substitute for these checks.

## Verification

Offline extraction of the identified seed matched thirteen embedded texts to their owners (two guides, ten starters, LICENSE.md); payload metadata and six tables parsed. Extracted guides and template collection fit their budgets. Review checked standalone adoption/refresh, trust boundaries, exact version-label preservation, consent, retention, and unchanged local adaptations. YAML examples preserved `0.20`, `0.10`, and `0.2` as quoted source labels and retained an unrelated field. The linked official sources informed the acceptance assessment. These checks establish text and YAML properties, not agent behavior or consumer compatibility.

The correction pass checked UTF-8, conflict markers, and local links/anchors across 52 Markdown files; Git whitespace checks passed. Earlier checks of three discovery maps, 26 declared paths/headers, and targeted private-path/token patterns across 31 changed files remain prior scoped results. None is a security assurance. No application build or runtime suite exists here.

One explicitly approved native subagent completed a bounded read-only review and returned findings with source locations. It identified the reminder-only gap before these edits. The worker reported no edits, network, installation, retries, descendants, or leftover processes. This demonstrates one dispatched review and returned result; the reviewer also read reference documents, so it was not a blinded paste-only adoption trial.

## Remaining Limits

No agent-driven initialization from the revised prompt alone, fresh-session activation, cancellation, refusal/no-answer, provider-switch, or comparative cost trial was run. Extraction proves text availability, not adherence or equal comprehension after compaction. Permission enforcement, repeated pruning, team burden, and total context cost remain unmeasured. External adopter state and historical measurements were not revalidated. Pattern scans are not a security assurance. [Evaluation](EVALUATION.md) supplies comparison methods.

Current priorities belong in [SoTY](SoTY.md); earlier audit history remains in Git.
