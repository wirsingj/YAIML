---
yaiml-revision: "0.33.73aaa0d992e327de"
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

YAIML keeps shared project context and reusable methods in ordinary files. One pasted init acquires guidance, builds useful memory and connects the active host plus applicable existing instruction routes. Ordinary work then uses context and maintains it without YAIML reminders.

## Version Awareness

`yaiml.yml` locates the core and supporting documents. Its version identifies the discovery layout, not a Markdown revision, roadmap milestone, or conformance claim. Read [RELEASE.md](RELEASE.md) for the product release and record the exact source commit or disclosed snapshot. [VERSIONING.md](VERSIONING.md) defines independent project-local file stamps and the core change audit.

Recommended shape for new adopters:

```yaml
yaiml:
  version: "0.2.0"
  core:
    state: SOT.md
    architecture: ARCHITECTURE.md
    maintainer_guide: MAINTAINER_GUIDE.md
    changes: changes.md
  supporting:
    operating_guide: YAIML_GUIDE.md
    versioning: VERSIONING.md
    release: RELEASE.md
    skills: skills/INDEX.md
    yaimlacp: YAIMLACP.md
```

Paths resolve from the map's directory, `.yaiml/` for new adoption; preserve established map locations. Include only existing files; omit `supporting` when unnecessary. The supporting entries name base resources acquired by init; add specialist memory only when useful. Resolve paths and symlinks before following them; discovery does not authorize access outside the repository.

Keep machine-specific paths, drive names, user-profile paths, `file://` URIs, localhost URLs, and private workspace URLs out of versioned guidance. Supply private reference locations through the human request or non-versioned configuration. A stable, team-approved public reference may be recorded when requested.

No YAIML parser is required or built here. Memory bodies stay free-form Markdown; the [record schema and external validation contract](CHANGE_RECORDS.md#record-schema-and-external-validation-contract) names stable integration points for external tools. Coordination handoffs describe message meaning without requiring a parser.

## Default Placement

For new adoption without an established memory home, use project-root `.yaiml/` for new core memory, operating guidance, templates, YAIMLACP, the copied-material notice and later specialist memory. An unrelated `docs/` folder alone does not establish a memory home. Keep new discovery at `.yaiml/yaiml.yml`; host instruction files remain at their supported entry points.

Preserve useful existing files and locations, including root, `docs/` or mixed layouts, unless relocation is confirmed. Additions follow the established memory home; index actual paths without duplicating owners. Inspect directory/file collisions and symlinks before writing; select a nonconflicting location and report it. The folder default changes neither discovery shape nor version.

On re-init, offer consolidation into `.yaiml/` even when guidance is unchanged. Follow the saved [Relocate Memory procedure](BOOTSTRAP.md#existing-layout-and-repeat-init): inspect ownership and consumers, present exact moves/reference repairs and impacts, then obtain affirmative confirmation. Reuse valid scoped approval; honor explicit standing placement preferences and skip already-consolidated setups. Decline/no answer preserves locations while independent in-place refresh continues. Move only approved files, preserve knowledge and concurrent work, repair references and verify scope. Unrelated documents, discovery layout and host instruction locations do not move with memory.

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

A general init or refresh request does not authorize discovery migration. Migrate only on explicit human request, with actual consumer compatibility checked and every local path and role preserved. Ordinary Markdown edits and path repairs do not require a discovery-version bump. Changed managed Markdown does receive a project revision under the separate revision convention.

### One Shape For New Adoption

Tolerating older layouts is a compatibility rule, not an invitation to add shapes. New adoption uses the recommended shape above. Report an unfamiliar layout rather than inventing a variant of it, and prefer `supporting` over a locally coined key when adding supporting entries to an existing map.

Quote the discovery version value. Written bare, `yaiml: 0.2` parses as a number, so `0.20` and `0.2` become the same value and a future `0.10` sorts below `0.9`. Repair a bare numeric label by quoting its exact source spelling, not a parsed number. If spelling is unavailable or consumer compatibility unclear, report the gap before changing it. This exception preserves the label; it does not authorize layout migration or cosmetic Markdown-header changes.

Compatibility has a cost that falls on readers. Every additional recognized shape is one more thing a cold agent must recognize before it can find anything, and a convention that accepts every layout has stopped locating documents reliably. Keep the recognized set small and the recommended shape single.

Readable YAML is not proof that a particular tool accepts it: indentation, comments, and other valid spellings may expose reader limitations. Check the exact map with its consumers before a requested migration. Do not turn a limited reader into restrictions on Markdown memory.

Future incompatible guidance must explain what changed, what can stay unchanged, and migration implications before recommending adoption.

## First-Time Adoption

Choose one single-paste peer: [networked init](prompts/init-yaiml.md) for the complete method package, or [offline init](prompts/init-yaiml-offline.md) for embedded minimal memory and records with no retrieval. Networked init defaults to reviewed `v0.5.1`, resolved once; floating `main` is only for explicitly requested testing. If that pin is unavailable, report incomplete acquisition without fallback. The prepared candidate is not publicly available until its ref is published. It names https://github.com/wirsingj/YAIML as the default upstream; an unfamiliar agent needs no prior YAIML knowledge or installed skills. It executes [Bootstrap](BOOTSTRAP.md) immediately, acquiring one revision's base resources. A local checkout, snapshot, fork or other source requires an explicit user request within its stated scope, never mere workspace presence or a recorded path. [Acquisition policy](BOOTSTRAP.md#resolve-and-acquire) also governs refresh and missing resources.

Bootstrap preserves useful target documentation, grounds distinct memory roles in evidence, saves a complete local base and connects supported host instructions and native skill discovery. The base supports ordinary offline work; extra reference docs/methods are acquired for concrete needs. Copying files differs from loading their bodies into context. No user-managed downloads, extra workflow pastes or runtime installation are required.

An unpublished development layout cannot be retrieved through the official public URL. Missing access, writes or host support yields explicit partial setup, with working guidance preserved and actionable gaps. Do not silently fall back to another source; a user-requested alternative can resolve missing access. Configuration alone is not fresh-session evidence.

[Agent Integration](AGENT_INTEGRATION.md) owns host routing; [Core Document Family](CORE_DOCUMENT_FAMILY.md) owns facts; [Skills And Project Lifecycle](SKILLS_AND_LIFECYCLE.md) explains ownership and growth. Saving YAIMLACP or skills does not authorize delegation.

## Security Review: Retrieval And Internal Mirrors

**What and when:** networked init and an explicitly requested refresh resolve one ref to one exact commit, retrieve `.yaiml/BOOTSTRAP.md`, then its adoption resource set and required relative dependencies: operating/revision/record guidance, release identity, optional-coordination rules, distributed skills/catalog, core starters and the copied-material license. Missing-guidance acquisition is a separate, scoped action under the same source policy; it is not an ordinary-work poll. Copying resources does not execute every method. No package manager, runtime, service, validator or telemetry is installed by YAIML.

**From where:** the built-in source is `https://github.com/wirsingj/YAIML` at reviewed `v0.5.1`, resolved once for the acquisition. GitHub/raw retrieval endpoints depend on host tools; inspect and permit those tools through your normal controls. An unavailable ref/access fails explicitly without source substitution. Floating `main` requires an explicit testing request. YAIML document instructions cannot enforce a host's network controls.

**Internal hosting:** fork or mirror the repository inside the organization, review the copied content and notices, and create an internally reviewed immutable ref. Supply the complete init prompt through your approved channel with an explicit request such as: “Initialize YAIML from our approved internal mirror at <organization-provided source>, ref <reviewed internal ref>; use no public upstream for this operation.” The existing explicit-source mechanism resolves that source/ref once and uses it for bootstrap and all resources. If an alternative repository has no requested ref, its default branch is resolved once; security-controlled adoption should always specify the reviewed ref. Maintain the mirror through the organization's separate review process; YAIML performs no automatic synchronization. Keep private mirror addresses in the request or unversioned workspace configuration, not public guidance.

**Later work:** ordinary tasks use installed local files and perform no upstream retrieval. A provenance note alone never authorizes another acquisition or makes a mirror the persistent default. To cover later refreshes, explicitly state a standing source/ref restriction in project instructions; otherwise repeat the override on each acquisition request. Installed methods still defer to stricter project/host policies. The [offline init](prompts/init-yaiml-offline.md) retrieves nothing ever: its entire minimal payload and notice are pasted, with no skills fetched. Obtain that prompt before entering an air-gapped environment. A later full upgrade requires a separate request under the applicable policy.

**Data boundary:** YAIML adds no network client. Your selected agent and provider may process project content under their own policies even when YAIML makes no retrieval; approve the host and enforce network/data controls independently. Local memory does not guarantee local inference.

## Existing YAIML Update

For an early installation without skills, paste the complete current [Init YAIML](prompts/init-yaiml.md) into the existing project's agent session. The seed supplies source resolution and bootstrap without depending on an installed refresh skill, catalog or recorded source. It recognizes existing memory and acquires the missing methods from the public reference. Explicitly request an alternative when needed, for example a local snapshot for unpublished development.

Once a usable source and current methods are installed, “update YAIML” selects [yaiml-refresh](skills/yaiml-refresh/SKILL.md). Reapplying init selects the same reconciliation. Updating the project's current facts selects `yaiml-maintain`. Keep these operations distinct.

These are adopter instructions. In the project developing YAIML, its contributor instructions govern editing canonical resources and its own memory. Its roadmap, publication policies and project-specific skills are not adopter defaults; improving them alone does not update the distributed product.

Refresh uses the official upstream unless the user explicitly requests another source. The current Maintainer Guide records applied provenance, override scope when requested, local adaptations and resource exceptions. Retain older source notes for comparison, not as automatic permission to acquire from them. Compare incoming content with the available baseline and local versions; disclose material reference edits. Without a baseline, disclose comparison limits; do not infer historical drift.

Preserve local methods and project knowledge. Apply compatible changes, reconcile meaningful conflicts through established authority, repair catalog/host routes and required references, and advance only the source records actually applied. Renames and removals require checking callers and useful adaptations; retain working resources when an update is incomplete. A healthy repeat refresh leaves files unchanged.

Convention refresh stays within documentation/method scope and preserves project license, notices, privacy and retention. It grants no application work, broad reorganization, branch mutation or delegation. Existing-layout relocation follows its separate scoped authority. Unknown map fields and mature roles remain intact.

Add the fourth core role in place and establish revision tracking prospectively using [the legacy transition](VERSIONING.md#adopt-from-older-yaiml). Preserve existing audit records and legacy version labels, report unknown earlier history, and check consumers before adding a map role. A pointer can expose the role without changing a restrictive discovery format.

Review the upgrade for preserved decisions, open questions, local protections and unfinished work, then check that the catalog, method bodies and host routes are reachable. Existing memory in `docs/` or at the root remains there unless relocation is approved; the new `.yaiml/` default does not require starting over. A new session should discover the installed skills and recover project context. File installation alone does not establish that behavior.

If host permissions block native skill entries, report partial setup and preserve usable instruction/catalog routes. After the user grants the required access through the host's supported controls, rerun init to repair the missing entries. Do not bypass a denied write or describe file-based use as verified native registration.

The optional [update prompt](prompts/update-yaiml.md) routes to the same method. A current bootstrap request supplies acquisition instructions, not embedded copies of every resource.

### Correcting An Incomplete Adoption

Repository access during one session does not establish that later agents received equivalent local guidance. Compare meaning across the installed core roles, evidence/synthesis/retention/branch rules, skill catalog/bodies and required references, shared rules, four core starters (specialist starters only when needed), YAIMLACP, notices, source/adaptation notes and active instruction routes. Classify each as missing, equivalent, intentionally adapted, conflicting, or unverified; different filenames are not defects.

Add missing reusable guidance, repair unreachable bodies and stale instructions, and reconcile conflicting rules through established authority. Preserve project facts, decisions, local protections, and healthy equivalent guidance; do not regenerate mature memory. Report what is present, what is configured to load, and what a fresh session actually used separately. Unknown prior guidance cannot establish historical drift. Record unresolved gaps, not an accumulating scorecard.

## Change Records And Consolidation

Once release ref `v0.5.1` is published, an ordinary networked update or re-pasted init acquires this record workflow; no mode selection is required. Before publication, testing requires an explicitly requested candidate snapshot/ref. Offline init establishes minimal records without retrieval. [Change Records](CHANGE_RECORDS.md#transition-and-recovery) preserves existing paths, inline audit history, records, receipts and stricter local rules, and retires obsolete mode flags after reconciling their meaning. Unknown history remains unknown.

Normal work consolidates when task ownership permits; overlapping or uncertain ownership defers factual snapshot updates while preserving pending corrections and repairing navigation. An ordinary request to prepare changes for review uses the existing Git skill. Core-only consumers must account for pending records before claiming current state. No worker, hook, runtime or publication permission is added.

## Normal Implementation Work

Ask for the work normally. [Connected instructions](AGENT_INTEGRATION.md) carry routine reading and maintenance; refreshing against an external YAIML reference is a separate action.

Refresh existing pointers with [concurrent-branch maintenance](PRUNING_AND_LIFECYCLE.md#concurrent-branches-and-review), preserving the target project's branch and review policy. A convention refresh does not authorize broad memory reorganization or branch operations.

## Refreshing Multiple Repositories

YAIML supplies guidance, not a dispatcher or automatic migration engine. Start with one representative target before expanding a batch.

Each receiving agent needs the original request, selected reference content or accessible location and revision, target scope, and permitted actions. Verify these survive the handoff. Keep private paths and routing metadata in appropriate local configuration, not target memory.

Apply the same preservation and migration rules per repository. Verify paths, links, persistent instructions, and retained knowledge; report applied, unchanged, partial, or blocked outcomes. Dispatched work is not a completed upgrade. Commit and push only where authorized; retain ordinary reviewed diffs for rollback without restoring whole files over newer contributor work.

For an authorized publication pass, record the source revision or snapshot digest, preserved layout and local adaptations, checks actually run and their limits in the upgrade commit message or an established change record. Record each target commit and push outcome in the batch report; a local commit is not a successful push. Verify the requested application's intent and functional checks separately from resource installation. Missing remotes, failed checks and unavailable environments stay explicit. After publishing a development reference, verify its resources at the published revision before replacing adopter snapshot notes. Distinguish working-file byte hashes from Git blobs when line endings normalize; verify the difference before advancing provenance. Keep only current source/evidence in living memory; feed reusable upgrade failures back into this guide or the owning method.

## Maintenance Prompts

Skills own the methods. These optional prompts route to the same skills; ordinary requests and supported native commands need no extra paste. See the [catalog](skills/INDEX.md) for argument-bearing tasks such as `yaiml-to-do 10`.

| Need | Prompt |
| --- | --- |
| Orient a session | [Hydrate](prompts/hydrate-agent-session.md) |
| Record material changes | [Update project memory](prompts/update-project-memory.md) |
| Check claims against reality | [Audit](prompts/audit-against-reality.md) |
| Remove repetition and stale state | [Compress](prompts/compress-project-memory.md) |
| Compare with a newer reference | [Update YAIML](prompts/update-yaiml.md) |
| Apply an approved change in direction | [Realign](prompts/major-project-realignment.md) |
