---
yaiml: 0.2
kind: adoption-update-guide
title: YAIML Adoption And Updates
purpose: Define evidence-based first-time adoption, existing YAIML updates, and discovery-protocol guidance.
belongs-here: adoption workflow, update workflow, discovery-protocol guidance, practical prompts.
not-here: project-specific state, command procedures, implementation tooling, service design.
durability: durable; update when YAIML adoption, update, or version-awareness guidance changes.
read-with: SoTY; YAIML Architecture; YAIML Maintainer Guide; Core Document Family.
update-when: discovery protocol, adoption expectations, or update rules change.
agent-guidance: Preserve repository-specific truth. Do not replace mature documents with generic templates. Treat YAIML as the canonical name.
---

# YAIML Adoption And Updates

YAIML keeps shared project memory in ordinary Markdown. Adoption connects applicable existing agent instructions and the active tool to that memory; routine work then maintains it without YAIML reminders.

## Version Awareness

`yaiml.yml` locates the core and supporting documents. Its version identifies the discovery layout, not a Markdown revision, roadmap milestone, or conformance claim. Use the supplied reference's Git revision or dated snapshot to distinguish guidance revisions.

Recommended shape for new adopters:

```yaml
yaiml:
  version: "0.2.0"
  core:
    state: SOT.md
    architecture: ARCHITECTURE.md
    maintainer_guide: MAINTAINER_GUIDE.md
  supporting:
    risk_review: docs/RISK_REVIEW.md
```

Paths resolve from the map's directory, normally the repository root. Include only existing files; omit `supporting` when unnecessary. The risk-review entry illustrates a mapping, not a file to create automatically. Resolve paths and symlinks before following them; discovery does not authorize access outside the repository.

Keep machine-specific paths, drive names, user-profile paths, `file://` URIs, localhost URLs, and private workspace URLs out of versioned guidance. Supply private reference locations through the human request or non-versioned configuration. A stable, team-approved public reference may be recorded when requested.

No YAIML parser is required. Memory-format validation remains limited to discovery; memory bodies stay free-form Markdown. Coordination handoffs describe message meaning without requiring a parser or schema.

## Discovery Layout Compatibility

Recognizable older layout:

```yaml
yaiml: "0.2"
usage: loose-project-memory
documents:
  sot:
    path: STATE_OF_THE_UNION.md
  architecture:
    path: ARCHITECTURE.md
  maintainer:
    path: MAINTAINER_GUIDE.md
supporting:
  - path: docs/YAIML.md
    role: local-usage-guide
```

Read the target's actual map before editing. Both examples describe roles and paths; neither defines a schema for document bodies.

| Change | Expected behavior |
| --- | --- |
| Clearer prose, shorter templates, or evidence guidance | Apply useful guidance without replacing project facts |
| Local filenames, headings, `role`/`kind` headers, or word budgets | Preserve equivalent local choices; no cosmetic migration |
| Older `documents.*.path` map or a stale path | Understand the layout and repair paths in place |
| Custom fields or tool consumers | Preserve unrelated extensions and working formatting |
| Unfamiliar layout or version | Retain unknown entries and marker; report ambiguous mappings rather than guessing or downgrading |

A general init or refresh request does not authorize discovery migration. Migrate only on explicit human request, with actual consumer compatibility checked and every local path and role preserved. Ordinary Markdown edits and path repairs do not require a version bump.

### One Shape For New Adoption

Tolerating older layouts is a compatibility rule, not an invitation to add shapes. New adoption uses the recommended shape above. Report an unfamiliar layout rather than inventing a variant of it, and prefer `supporting` over a locally coined key when adding supporting entries to an existing map.

Quote the discovery version value. Written bare, `yaiml: 0.2` parses as a number, so `0.20` and `0.2` become the same value and a future `0.10` sorts below `0.9`. Repair a bare numeric label by quoting its exact source spelling, not a parsed number. If spelling is unavailable or consumer compatibility unclear, report the gap before changing it. This exception preserves the label; it does not authorize layout migration or cosmetic Markdown-header changes.

Compatibility has a cost that falls on readers. Every additional recognized shape is one more thing a cold agent must recognize before it can find anything, and a convention that accepts every layout has stopped locating documents reliably. Keep the recognized set small and the recommended shape single.

Readable YAML is not proof that a particular tool accepts it: indentation, comments, and other valid spellings may expose reader limitations. Check the exact map with its consumers before a requested migration. Do not turn a limited reader into restrictions on Markdown memory.

Future incompatible guidance must explain what changed, what can stay unchanged, and migration implications before recommending adoption.

## First-Time Adoption

Paste the complete standalone [Init YAIML](../prompts/init-yaiml.md), including its embedded texts, into the target repository's agent session. It covers bounded inspection, reuse, filename collisions, and verification without downloads or installation. The agent creates or updates supported instruction files locally from the prompt; users do not obtain them separately.

Completeness takes priority over seed length. Keep a human-readable opening; optimize embedded text for agents using concise directives, useful headers, minimal whitespace, valid Markdown/YAML. Preserve every obligation, trigger, exception, permission, retention rule, notice, and context route. Human readability remains necessary; ambiguous shorthand is not compression.

Review the result for preserved project knowledge and honest setup gaps. [Agent Integration](AGENT_INTEGRATION.md) explains persistent activation; [Core Document Family](CORE_DOCUMENT_FAMILY.md) explains fact placement.

Init is the seed; the adopting project owns the evolving memory. Its embedded operating guide preserves everyday maintenance procedures, its dormant template collection preserves the three core and seven specialist starters, and its complete [YAIMLACP](YAIMLACP.md) text preserves optional handoffs. Save these locally or reconcile them with equivalent existing owners, index actual paths, and retain the embedded notice with copied material. Do not report complete setup with missing bodies or remote-only pointers.

The startup/context reminder considers coordination without extra calls. Explain the option, cost, access, and limits and obtain affirmative confirmation before first use or changed scope/cost. Saving guidance does not authorize workers. Runtime support still belongs to the host.

The seed carries procedures and writing aids, not this reference project's facts or policies. Instantiate specialist memory only for useful project knowledge; keep unused starters dormant and out of routine context. A new project needs no source-repository access to use them. Future convention refreshes use a supplied snapshot and preserve local adaptations; there is no automatic upstream dependency.

## Existing YAIML Update

A convention refresh applies useful reference changes to local guidance while preserving the project's own memory. It is distinct from updating SoT after ordinary work.

Paste the complete current init to perform this refresh. The prompt supplies both the request and reference; no separate upgrade wording, source-repository access, or URL is needed. Existing adoption triggers reconciliation rather than regeneration, even when discovery versions match.

1. Check local instructions, discovery, worktree state, and relevant memory, reading headers first. Preserve uncommitted and concurrent work.
2. Identify the supplied reference revision or snapshot, including material uncommitted reference edits. If no reference is available, request one rather than guessing.
3. Start with reference init/adoption guidance and local instruction pointers or maintenance notes. Use relevant differences from a previous reference when known; inspect other topics only for material differences or local copies.
4. Refresh useful local prompts, templates, or instructions, remove obsolete template residue, and repair links or stale paths within the existing layout. Retain meaningful local headings, facts, commands, decisions, risks, supporting knowledge, and uncertainty.
5. Update project memory only where its meaning changed. Report convention changes separately from any independently verified project drift.

Do not import this reference repository's own facts, personal policies, license, or permissions. Preserve applicable notices on copied material and the target's license. Respect the target's privacy, retention, and review rules; do not change application code, install dependencies, or run expensive checks solely for a refresh.

Remove obsolete machine-specific reference entries only when their purpose is understood, and repair dependent instructions. Re-read concurrent changes before writing; keep contributor conflicts visible. An unchanged reference still warrants checking local drift, but a repeat refresh with no material difference leaves files unchanged.

The optional [update prompt](../prompts/update-yaiml.md) carries this workflow into another repository.

Refresh persistent instructions and their local operating, template, and coordination content together. A complete pasted init can be the reference; use its embedded texts to repair missing guides without downloads. Preserve scoped decisions and distinguish revised instructions from observed behavior. A documentation refresh does not approve delegation, server creation, or configuration changes.

### Correcting An Incomplete Adoption

Repository access during one session does not establish that later agents received equivalent local guidance. Compare meaning across the installed core roles, evidence/synthesis/retention/branch rules, maintenance procedures, ten starters, YAIMLACP, notices, and active instruction routes. Classify each as missing, equivalent, intentionally adapted, conflicting, or unverified; different filenames are not defects.

Add missing reusable guidance, repair unreachable bodies and stale instructions, and reconcile conflicting rules through established authority. Preserve project facts, decisions, local protections, and healthy equivalent guidance; do not regenerate mature memory. Report what is present, what is configured to load, and what a fresh session actually used separately. Unknown prior guidance cannot establish historical drift. Record unresolved gaps, not an accumulating scorecard.

## Normal Implementation Work

Ask for the work normally. [Connected instructions](AGENT_INTEGRATION.md) carry routine reading and maintenance; refreshing against an external YAIML reference is a separate action.

Refresh existing pointers with [concurrent-branch maintenance](PRUNING_AND_LIFECYCLE.md#concurrent-branches-and-review), preserving the target project's branch and review policy. A convention refresh does not authorize broad memory reorganization or branch operations.

## Refreshing Multiple Repositories

YAIML supplies guidance, not a dispatcher or automatic migration engine. Start with one representative target before expanding a batch.

Each receiving agent needs the original request, selected reference content or accessible location and revision, target scope, and permitted actions. Verify these survive the handoff. Keep private paths and routing metadata in appropriate local configuration, not target memory.

Apply the same preservation and migration rules per repository. Verify paths, links, persistent instructions, and retained knowledge; report applied, unchanged, partial, or blocked outcomes. Dispatched work is not a completed upgrade. Commit and push only where authorized; retain ordinary reviewed diffs for rollback without restoring whole files over newer contributor work.

## Maintenance Prompts

These optional prompts are for explicit maintenance, not steps required during routine work.

| Need | Prompt |
| --- | --- |
| Orient a session | [Hydrate](../prompts/hydrate-agent-session.md) |
| Record material changes | [Update project memory](../prompts/update-project-memory.md) |
| Check claims against reality | [Audit](../prompts/audit-against-reality.md) |
| Remove repetition and stale state | [Compress](../prompts/compress-project-memory.md) |
| Compare with a newer reference | [Update YAIML](../prompts/update-yaiml.md) |
| Apply an approved change in direction | [Realign](../prompts/major-project-realignment.md) |
