---
yaiml: 0.1
kind: maintainer
title: YAIML Maintainer Guide
purpose: Preserve current procedures for evolving YAIML without drifting from the living-memory concept.
belongs-here: current commands, review procedures, artifact maintenance, failure playbooks.
not-here: project identity, conceptual architecture, complete history.
durability: current-only; remove dead commands and obsolete paths.
read-with: SoTY; YAIML Architecture.
update-when: repository structure, prompts, templates, or procedures change.
agent-guidance: Verify command claims when practical. Surface conflicts. Preserve human direction.
---

# YAIML Maintainer Guide

## Quick Start

This is a plain-file standard repository. There is no build step, package install, runtime service, or validator.

## Common Commands

Inspect files:

```powershell
rg --files
```

Check Git state:

```powershell
git status --short --branch
```

Search for old formal-standard or contract-system drift:

```powershell
rg "SPEC|schema|conformance|MUST|SHOULD|validator|parser|Document Contract|soft contract"
```

Search for stale SoT naming:

```powershell
rg "StateOfThe|STATE_OF_THE|State of the|State document"
```

These search terms intentionally include older draft language. Hits should either be removed or explicitly contextualized as legacy drift checks.

## Focused Reviews

Run these manually after meaningful edits:

- Compare `README.md` with `docs/SoTY.md` for concept drift.
- Compare `templates/core/` with `docs/CORE_DOCUMENT_FAMILY.md`.
- Compare prompt instructions with `docs/STABLE_HEADERS.md`, `docs/AMBIGUITY_AND_EVIDENCE.md`, and `docs/PRUNING_AND_LIFECYCLE.md`.
- Check examples for believable, compact project memory rather than generic filler; they should be fictional but detailed enough to feel shaped by real engineering pressure.
- Confirm no license has been introduced without explicit human approval.

## Important Files

- `README.md`: public entry point and immediate-use path.
- `yaiml.yml`: discovers this repository's YAIML documents.
- `docs/SoTY.md`: current direction, risks, and open questions.
- `docs/ARCHITECTURE.md`: durable conceptual model and artifact boundaries.
- `docs/MAINTAINER_GUIDE.md`: this procedural guide.
- `templates/core/`: starter documents users copy into projects.
- `prompts/`: pasteable agent workflows.

## Danger Files

- `README.md`: easy place to overclaim maturity or tooling.
- `templates/core/SOT.md`: neutral starter template; easy place to normalize append-only memory.
- `docs/STABLE_HEADERS.md`: easy place to drift into schema design.
- `prompts/initialize-yaiml.md`: easy place to accidentally authorize code changes during initialization.

## Failure Playbooks

### The Repository Starts Looking Like A Formal Standard

Symptoms:

- new `SPEC.md`;
- schema or conformance directories;
- RFC-style requirement language;
- validator, parser, or contract-system roadmap becoming central;
- README leading with YAML syntax.

Begin here:

1. Read `docs/SoTY.md`.
2. Read `docs/ARCHITECTURE.md` Retired Approaches.
3. Remove or rewrite the formal-standard artifact unless a human explicitly changed the phase.

### The SoT Template Becomes A Work Log

Symptoms:

- long chronological completion lists;
- old solved risks still active;
- repeated principles;
- no current priorities visible near the top.

Begin here:

1. Use `prompts/prune-sot.md`.
2. Preserve active risk, current direction, divergence, and human directives.
3. Delete completed implementation history that Git can recover.

### A Prompt Turns Vague

Symptoms:

- prompt says "update docs" without naming SoT, Architecture, and Maintainer responsibilities;
- prompt allows confident inference;
- prompt does not mention pruning;
- prompt does not protect human corrections.

Begin here:

1. Compare the prompt to `docs/CORE_DOCUMENT_FAMILY.md`.
2. Add explicit evidence, ambiguity, conflict, and pruning behavior.
3. Keep it provider-neutral.
