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

YAIML keeps shared project memory in ordinary Markdown. Adoption establishes that memory and the active agent's persistent instructions; routine work then maintains it without YAIML reminders.

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

No YAIML parser is required. Any future validation remains limited to discovery; memory bodies stay free-form Markdown.

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

Quote the version value. Written bare, `yaiml: 0.2` parses as a number, so `0.20` and `0.2` become the same value and a future `0.10` sorts below `0.9`. Quoted, it stays the label it was meant to be. This is the one discovery detail worth repairing in place when encountered, because it changes meaning rather than style.

Compatibility has a cost that falls on readers. Every additional recognized shape is one more thing a cold agent must recognize before it can find anything, and a convention that accepts every layout has stopped locating documents reliably. Keep the recognized set small and the recommended shape single.

Readable YAML is not proof that a particular tool accepts it: indentation, comments, and other valid spellings may expose reader limitations. Check the exact map with its consumers before a requested migration. Do not turn a limited reader into restrictions on Markdown memory.

Future incompatible guidance must explain what changed, what can stay unchanged, and migration implications before recommending adoption.

## First-Time Adoption

Paste the standalone [Init YAIML](../prompts/init-yaiml.md) prompt into the target repository's agent session. It covers bounded inspection, reuse of existing documents, filename collisions, and verification without downloads or installation.

Review the result for preserved project knowledge and honest setup gaps. [Agent Integration](AGENT_INTEGRATION.md) explains persistent activation; [Core Document Family](CORE_DOCUMENT_FAMILY.md) explains fact placement.

## Existing YAIML Update

A convention refresh applies useful reference changes to local guidance while preserving the project's own memory. It is distinct from updating SoT after ordinary work.

1. Check local instructions, discovery, worktree state, and relevant memory, reading headers first. Preserve uncommitted and concurrent work.
2. Identify the supplied reference revision or snapshot, including material uncommitted reference edits. If no reference is available, request one rather than guessing.
3. Start with reference init/adoption guidance and local instruction pointers or maintenance notes. Use relevant differences from a previous reference when known; inspect other topics only for material differences or local copies.
4. Refresh useful local prompts, templates, or instructions, remove obsolete template residue, and repair links or stale paths within the existing layout. Retain meaningful local headings, facts, commands, decisions, risks, supporting knowledge, and uncertainty.
5. Update project memory only where its meaning changed. Report convention changes separately from any independently verified project drift.

Do not import this reference repository's own facts, personal policies, license, or permissions. Preserve applicable notices on copied material and the target's license. Respect the target's privacy, retention, and review rules; do not change application code, install dependencies, or run expensive checks solely for a refresh.

Remove obsolete machine-specific reference entries only when their purpose is understood, and repair dependent instructions. Re-read concurrent changes before writing; keep contributor conflicts visible. An unchanged reference still warrants checking local drift, but a repeat refresh with no material difference leaves files unchanged.

The optional [update prompt](../prompts/update-yaiml.md) carries this workflow into another repository.

## Normal Implementation Work

Ask for the work normally. [Connected instructions](AGENT_INTEGRATION.md) carry routine reading and maintenance; refreshing against an external YAIML reference is a separate action.

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
