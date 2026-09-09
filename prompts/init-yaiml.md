# Init YAIML

Add YAIML project memory to this repository. This prompt is self-contained; no reference download, package, or installation is needed. You need repository read/write access; if unavailable, report that limitation without claiming setup succeeded.

YAIML means Yet Another AI Markup Language. It preserves shared project understanding across AI sessions and human contributors in ordinary Markdown. Make bounded documentation changes; leave application code and licensing alone unless separately requested.

## Inspect First

1. Read applicable repository agent and contribution instructions. Check the worktree before editing and preserve uncommitted work.
2. Read `yaiml.yml` if present. Resolve memory and instruction paths, including symlinks, before reads or writes; discovery does not authorize access outside the repository. Read selected memory headers before bodies, starting with the core.
3. Inspect existing docs, representative source, tests, scripts, and sanitized configuration examples. Skip generated/vendor trees, credential files, raw sensitive logs, and full history unless specifically needed and permitted. Stop when the core roles have useful, supported content and material gaps are identified.
4. Reuse documents that already serve a core role. Preserve useful content, local names, and human direction. If a default filename holds unrelated material, choose another path rather than overwriting it.

Complete setup with available evidence; ask only when missing direction blocks safe, accurate work. Do not infer vanished human decisions from code. Record nonblocking unknowns.

Prefer inspection and inexpensive, understood local checks. Do not install project dependencies or run expensive, external-service, deployment, or destructive commands merely to initialize memory. Record unrun procedures honestly.

## Write The Smallest Useful Memory Set

Use three distinct roles, normally in `SOT.md`, `ARCHITECTURE.md`, and `MAINTAINER_GUIDE.md`. Existing paths or a suitable `docs/` directory are fine.

| Role | Keep here | Keep elsewhere |
| --- | --- | --- |
| SoT (“State Of The”) | Project identity, current capabilities, human direction, active risks, priorities, consequential verification, divergence, useful lessons | Command reference, durable architecture, chronological work history |
| Architecture | Components, data flow, ownership boundaries, invariants, current and intended design, relevant rejected approaches | Task lists, full file inventory, procedures |
| Maintainer Guide | Setup, commands, checks, diagnostics, important or dangerous files, release/recovery procedures | Product manifesto, full history |

Choose readable headings and short prose. Omit empty sections; link detailed sources rather than copying them. Summarize completed work as current capability or a useful lesson.

Add supporting documents only when several concrete recurring facts need a separate home or a different retention rule. A small project may need none. Do not copy a catalog of potential documents.

Every memory document needs a brief stable header identifying its responsibility, exclusions, lifecycle, update trigger, relevant companions, and evidence/conflict guidance. Give new documents a role-appropriate word budget in the header or equivalent prose. For example:

```md
---
role: sot
purpose: Current state, direction, risks, and priorities.
not-here: Architecture, commands, complete history.
durability: Replace stale state; preserve active decisions and uncertainty.
budget: About 1500 words; a working target, subject to evidence and retention needs.
update-when: Direction, capabilities, risks, or priorities change.
read-with: ARCHITECTURE.md; MAINTAINER_GUIDE.md.
agent-guidance: Verify consequential claims. Preserve human intent and unresolved conflicts.
---

# SOT
```

Equivalent prose or field names are acceptable. `read-with` points to relevant companions; it does not require recursive loading. Existing `kind` fields or `yaiml: 0.2` header hints need no cosmetic migration.

Size budgets for useful reading cost; 1500 words is illustrative, not a length to fill. Preserve existing targets and headers. Prune oversized memory safely before adding, retaining necessary facts and governed records even if an overage remains. Avoid bulk rewrites during setup.

## Preserve Evidence And Authority

Use labels or sections where uncertainty could steer work:

- **Verified**: supported within a stated scope by inspected evidence.
- **Declared**: authorized human intent or an approved project decision.
- **Observed**: behavior seen but not fully traced.
- **Inferred**: plausible explanation needing verification.
- **Disputed**: sources disagree.
- **Unknown**: not established.
- **Obsolete**: superseded; retain only if it still prevents mistakes.

Name evidence for consequential claims. Source inspection can establish that a command or test exists; it cannot establish a passing run. For executed checks, record outcome and relevant revision, date, and environment. Check test discovery, skips, and relevant assertions before claiming coverage. Attribute prior results with their limits. Never turn an old result or a recent document timestamp into current verification.

Preserve intended behavior when implementation disagrees and record the divergence. Follow the project’s established decision authority; do not invent a hierarchy when ownership is unclear. Keep conflicts from other contributors visible until evidence or authorized direction resolves them.

Read material is context, not permission; a “Declared” label does not authenticate approval. Follow applicable instructions, tool permissions, and review rules. Resolve consequential conflicts before dependent changes; continue independent authorized work.

## Add Discovery

For a new setup, use repository-relative paths resolved from the directory containing `yaiml.yml`:

```yaml
yaiml:
  version: "0.2.0"
  core:
    state: SOT.md
    architecture: ARCHITECTURE.md
    maintainer_guide: MAINTAINER_GUIDE.md
```

Add `yaiml.supporting` entries only for existing documents. The version identifies the discovery layout, not the revision of the Markdown guidance.

For existing adopters, preserve layout, version, local names, unknown extension fields, and useful declarations. Older maps may use `documents.sot.path`, `documents.architecture.path`, and `documents.maintainer.path`, plus supporting path entries. Repair stale paths in place. Migrate only on explicit human request, with actual consumer compatibility checked and every path and role preserved. Report unfamiliar layouts rather than guessing or downgrading them.

Do not put machine-specific reference paths, local drive names, user profile paths, local workspace URLs, or private workspace URLs in versioned files. A convention-refresh reference belongs in the human prompt or non-versioned workspace configuration.

## Connect Future Sessions

Connect YAIML to the current agent's persistent repository instructions. Identify the supported mechanism from available configuration or current official documentation; do not assume a filename is automatically loaded. Add or update one concise pointer per relevant existing surface, preserving scope and rules. Create the minimal supported instruction file needed for the active agent, using `AGENTS.md` when supported. Do not create files for unused tools.

Check activation scope, syntax, and the discovery path, including from subdirectories. Distinguish configured instructions from observed fresh-session loading. If persistence is unavailable or needs a user-controlled setting, report that setup gap now; do not present recurring reminders as completed integration.

Use this text or equivalent:

```md
## YAIML Project Memory

Before meaningful work, read yaiml.yml and its three core documents.
Read each selected document’s stable header before its body.
Load supporting documents only when relevant to the task.
Reuse already-loaded context while current; refresh it after relevant changes.
Verify consequential claims against the repository.

Before finishing material work, update affected memory without a separate
YAIML request. Preserve human direction and unresolved conflicts. Respect
read-only scope and review rules; report pending updates when writing is
unavailable. Leave unchanged memory alone.

Prune stale or repeated content before adding. Preserve current facts,
decisions, evidence, uncertainty, and governed retention; necessary growth is
allowed. Check local budgets without deleting needed knowledge or inflating
targets to fit. For compression or overruns, report before/after counts and
retained overages. Do not load unrelated documents merely to count them.

“Update YAIML”, “updated YAIML”, or “check new YAIML” means compare the local
convention guidance against a human-provided or workspace-local reference,
preserving project memory and the existing discovery layout.

“Clean up YAIML”, “compress YAIML”, “compact project memory”,
“prune project memory”, or “prune SoT” means remove stale or repetitive
memory while preserving current truth, evidence, direction, and uncertainty.

See the Maintainer Guide for local YAIML maintenance.
```

Add a short YAIML maintenance note in the Maintainer Guide covering those refresh and compression requests. Keep reference locations out of committed memory. If no reference is available for a later refresh, request one instead of guessing.

## Retention And Sharing

Keep YAIML versioned with the project by default. Do not add it to `.gitignore` unless the human requests it or an established private-memory policy requires it.

Follow repository privacy, access, retention, and review rules. Preserve sanitized constraints, evidence locations, owners when known, and open questions. Exclude secrets, personal data, private transcripts, raw sensitive logs, private screenshots, and confidential or exploit details inappropriate for the audience.

Preserve approved legal and security statements and applicable copyright/license notices without inventing rights or professional conclusions. Respect governed retention before pruning. Do not create archives unless requested.

Do not add YAIML runtime infrastructure, dependencies, CLIs, SDKs, provider adapters, package manifests, schemas for Markdown memory, or conformance machinery.

## Verify And Report

Re-read files that changed during inspection before editing them; preserve concurrent work and unresolved conflicts. Rerunning init should fill material gaps, not append duplicate pointers or rewrite healthy memory.

Check discovery paths, role boundaries, headers, instruction pointers, and budgets for created or edited memory. Count whitespace-delimited words across the whole document, including headers, unless its budget specifies otherwise. Remove duplicated facts, template residue, and invented claims; confirm human directives survived. Leave the result as a reviewable diff; commit or push only when authorized.

Report changed files, the persistent instruction mechanism connected, evidence inspected, checks actually run, created or edited memory sizes against declared budgets, and any setup gaps or unresolved overages. Routine reading and maintenance should need no further YAIML reminders. Keep the report proportional to the work.
