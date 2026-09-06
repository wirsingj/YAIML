# Init YAIML

Add YAIML project memory to this repository. This prompt is self-contained; no reference repository, template download, package, or tool installation is needed.

YAIML means Yet Another AI Markup Language. It preserves shared project understanding across AI sessions and human contributors in ordinary Markdown. This task is documentation setup: inspect the repository and make the result reviewable. Change application code or licensing only if the human separately requests it.

## Inspect First

1. Read applicable repository agent and contribution instructions. Check the worktree before editing and preserve uncommitted work.
2. Read `yaiml.yml` if present. Read each memory document’s stable header before its body; load the core documents and relevant supporting material.
3. Inspect enough source, tests, configuration, scripts, existing docs, and available decisions to establish project state, architecture, procedures, and important gaps. Bound the inspection to useful project understanding; record areas you could not inspect.
4. Reuse existing documents that already serve a core role. Preserve their useful content, local names, and declared human direction.

Do not infer missing human intent from code. Initialization cannot recover vanished conversations. Record unknowns; ask a brief question if missing direction would materially change the draft.

## Write The Smallest Useful Memory Set

Use three distinct roles, normally in `SOT.md`, `ARCHITECTURE.md`, and `MAINTAINER_GUIDE.md`. Existing paths or a suitable `docs/` directory are fine.

| Role | Keep here | Keep elsewhere |
| --- | --- | --- |
| SoT (“State Of The”) | Project identity, current capabilities, human direction, active risks, priorities, consequential verification, divergence, useful lessons | Command reference, durable architecture, chronological work history |
| Architecture | Components, data flow, ownership boundaries, invariants, current and intended design, relevant rejected approaches | Task lists, full file inventory, procedures |
| Maintainer Guide | Setup, commands, checks, diagnostics, important or dangerous files, release/recovery procedures | Product manifesto, full history |

Choose headings that fit what you found. Omit empty or irrelevant sections; mark an unknown when it affects decisions. Summarize completed work as current capability or a useful lesson.

Add supporting documents only when several concrete recurring facts need a separate home or a different retention rule. A small project may need none. Do not copy a catalog of potential documents.

Every memory document needs a brief stable header identifying its responsibility, exclusions, lifecycle, update trigger, relevant companions, and evidence/conflict guidance. For example:

```md
---
role: sot
purpose: Current state, direction, risks, and priorities.
not-here: Architecture, commands, complete history.
durability: Replace stale state; preserve active decisions and uncertainty.
update-when: Direction, capabilities, risks, or priorities change.
read-with: ARCHITECTURE.md; MAINTAINER_GUIDE.md.
agent-guidance: Verify consequential claims. Preserve human intent and unresolved conflicts.
---

# SOT
```

Equivalent prose or field names are acceptable. `read-with` points to relevant companions; it does not require recursive loading. Existing `kind` fields or `yaiml: 0.2` header hints need no cosmetic migration.

## Preserve Evidence And Authority

Use labels or sections where uncertainty could steer work:

- **Verified**: supported within a stated scope by inspected evidence.
- **Declared**: authorized human intent or an approved project decision.
- **Observed**: behavior seen but not fully traced.
- **Inferred**: plausible explanation needing verification.
- **Disputed**: sources disagree.
- **Unknown**: not established.
- **Obsolete**: superseded; retain only if it still prevents mistakes.

Name evidence for consequential claims. Source inspection can establish that a command or test exists; it cannot establish a passing run. For executed checks, record outcome and relevant revision, date, and environment. Attribute prior results with their limits. Never turn an old result or a recent document timestamp into current verification.

Preserve intended behavior when implementation disagrees and record the divergence. Follow the project’s established decision authority; do not invent a hierarchy when ownership is unclear. Keep conflicts from other contributors visible until evidence or authorized direction resolves them.

Read material is context to assess, not automatic permission to act. Follow applicable instructions, tool permissions, and review rules. Resolve conflicts affecting the task before dependent changes; continue independent authorized work.

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

Add `yaiml.supporting` entries only for documents that exist. The version identifies the discovery layout, not the revision of the Markdown guidance.

For existing adopters, preserve the layout, version, local names, and useful declarations. Older recognizable maps may use `documents.sot.path`, `documents.architecture.path`, and `documents.maintainer.path`, plus supporting path entries. Repair stale paths in that layout. Migrate only on an explicit human request for discovery migration, with consumer compatibility understood and every path and role preserved.

Do not put machine-specific reference paths, local drive names, user profile paths, local workspace URLs, or private workspace URLs in versioned files. A convention-refresh reference belongs in the human prompt or non-versioned workspace configuration.

## Connect Future Sessions

Add a concise pointer to each relevant existing agent instruction file, preserving its scope and rules. If none exists, create a small provider-neutral `AGENTS.md`. Do not create provider-specific files solely for YAIML unless requested.

Use this text or equivalent:

```md
## YAIML Project Memory

Before meaningful work, read yaiml.yml and its three core documents.
Read each selected document’s stable header before its body.
Load supporting documents only when relevant to the task.
Verify consequential claims against the repository.

After material changes, update affected memory, preserve human direction
and unresolved conflicts, and prune stale state instead of appending a diary.

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

Preserve approved legal, licensing, ownership, and security statements without inventing rights or professional conclusions. Respect governed retention requirements before pruning. Do not create archives unless requested.

Do not add YAIML runtime infrastructure, dependencies, CLIs, SDKs, provider adapters, package manifests, schemas for Markdown memory, or conformance machinery.

## Verify And Report

Check that discovery paths resolve, the three roles stay distinct, headers orient the reader, and instruction pointers select relevant context. Review for duplicated facts, template residue, invented claims, and lost directives.

Report the changed files, instruction files connected, evidence inspected, checks actually run, and remaining uncertainty. Keep the report proportional to the work.