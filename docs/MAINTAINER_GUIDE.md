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

This is a plain-file convention repository. There is no build step, package install, runtime service, or validator.

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
rg "StateOfThe|STATE_OF_THE|State of the|State document|preferred real filenames|usually expand"
```

Search for accidental custom-format drift:

```powershell
rg "\\.yaiml|custom file extension|custom document format"
```

Search for unsafe memory hygiene drift:

```powershell
rg "gitignore|\\.gitignore|secret|token|password|private key|credential|copyright|trademark|patent|ownership|IP|license"
```

Search for maturity overclaiming:

```powershell
rg "standard|industry|adoption|proven|benchmark|metrics|case study"
```

These search terms intentionally include older draft language. Hits should either be removed or explicitly contextualized as legacy drift checks.

## Focused Reviews

Run these manually after meaningful edits:

- Compare `README.md` with `docs/SoTY.md` for concept drift.
- Check README from a human adoption stance: problem, value, safety, and first use should be clearer than internal framework vocabulary.
- Check that the README leads with the minimum useful setup before the full initialization path.
- Check that the README presents init as a one-time setup move and does not imply humans should paste workflow prompts after every routine step.
- Compare `templates/core/` and `templates/supporting/` with `docs/CORE_DOCUMENT_FAMILY.md`.
- Compare `CONTRIBUTING.md` and `ROADMAP.md` with `docs/SoTY.md` for stale licensing, phase, or tooling claims.
- Confirm every document declared in `yaiml.yml` has a stable header before its body.
- Compare prompt instructions with `docs/STABLE_HEADERS.md`, `docs/AMBIGUITY_AND_EVIDENCE.md`, and `docs/PRUNING_AND_LIFECYCLE.md`.
- Compare `prompts/hydrate-agent-session.md` with `docs/CONTEXT_LOADING.md`.
- Compare `prompts/init-yaiml.md` with the README minimum useful setup.
- Check that `prompts/initialize-yaiml.md` remains self-contained enough to use in an unrelated repository without assuming this repo's docs are attached.
- Check that generic initialization examples recommend `SOT.md`, `ARCHITECTURE.md`, and `MAINTAINER_GUIDE.md` by default while allowing project-specific SoT names.
- Check that `docs/AGENT_INTEGRATION.md` keeps YAIML distinct from agent behavior instructions.
- Check that `docs/EVALUATION.md` requests real evidence without inventing adoption claims, metrics, or proof.
- Check that guidance keeps YAIML documents as ordinary Markdown by default rather than introducing a `.yaiml` extension.
- Check that initialization guidance does not add YAIML files to `.gitignore` by default.
- Check that prompts and templates warn against storing secrets, sensitive raw values, or AI-invented legal/IP conclusions in YAIML documents.
- Check that `SECURITY.md` still matches README, prompts, templates, and public-repo sensitive-reporting expectations.
- Check that self-unfolding document guidance encourages useful project-specific extension without normalizing empty document ceremony.
- Check examples for believable, compact project memory rather than generic filler; they should be fictional but detailed enough to feel shaped by real engineering pressure.
- For every proposed addition, ask whether it improves a fresh coding agent's ability to reconstruct current engineering understanding. If not, remove or defer it.
- Confirm the restrictive incubation license remains intact and is not misrepresented as open source.
- Confirm no broader license, license header, or public reuse grant has been introduced without explicit human approval.

## Important Files

- `README.md`: public entry point and immediate-use path.
- `LICENSE.md`: restrictive all-rights-reserved notice; do not replace with an open-source license without explicit human approval.
- `SECURITY.md`: sensitive-reporting and memory-hygiene policy for the public repository.
- `CONTRIBUTING.md`: contribution rules and licensing guardrails.
- `ROADMAP.md`: near-term priorities and deferred future-tooling boundary.
- `yaiml.yml`: discovers this repository's YAIML documents.
- `docs/SoTY.md`: current direction, risks, and open questions.
- `docs/ARCHITECTURE.md`: durable conceptual model and artifact boundaries.
- `docs/MAINTAINER_GUIDE.md`: this procedural guide.
- `docs/AGENT_INTEGRATION.md`: boundary between agent instruction files and YAIML project memory.
- `docs/CONTEXT_LOADING.md`: bounded loading model for YAIML context.
- `docs/EVALUATION.md`: case-study template and cold-start comparison method.
- `templates/core/`: starter documents users copy into projects.
- `prompts/`: fallback and maintenance workflows; `init-yaiml.md` should stay small and usable as a one-time adoption prompt, while `initialize-yaiml.md` should carry deeper context for a no-prior-YAIML agent.

## Danger Files

- `README.md`: easy place to overclaim maturity or tooling.
- `LICENSE.md`: easy place to accidentally grant reuse rights before the project is ready.
- `SECURITY.md`: easy place to overpromise professional security process or drift away from YAIML's memory-hygiene rules.
- `CONTRIBUTING.md` and `ROADMAP.md`: easy places for stale licensing or future-tooling claims to survive after concept changes.
- `templates/core/SOT.md`: default SoT starter template; easy place to normalize append-only memory or make project-specific naming feel required.
- `templates/supporting/`: easy place to imply every possible supporting document should exist in every project.
- `prompts/hydrate-agent-session.md`: easy place to accidentally load every supporting document for every task.
- `prompts/initialize-yaiml.md`: easy place to accidentally authorize code changes during initialization, make YAIML private-by-default, or allow unsafe legal/IP claims.
- `prompts/init-yaiml.md`: easy place to become too large or to omit evidence discipline.
- `docs/EVALUATION.md`: easy place to accidentally fabricate proof or imply a benchmark suite exists.
- `docs/STABLE_HEADERS.md`: easy place to drift into schema design.

## Failure Playbooks

### The Repository Starts Looking Like A Formal Standard

Symptoms:

- new `SPEC.md`;
- schema or conformance directories;
- RFC-style requirement language;
- validator, parser, or contract-system roadmap becoming central;
- README leading with YAML syntax.
- README leading with the full doctrine before the minimum adoption path.

Begin here:

1. Read `docs/SoTY.md`.
2. Read `docs/ARCHITECTURE.md` Retired Approaches.
3. Remove or rewrite the formal-standard artifact unless a human explicitly changed the phase.

### The Front Door Gets Heavy Again

Symptoms:

- README first asks users to understand every supporting document role;
- minimum setup is hidden below the full initializer;
- users must invent a project-specific SoT filename before trying YAIML;
- quick start makes ongoing YAIML use sound like repeated prompt-pasting instead of repository-carried guidance;
- licensing or maturity caveats bury the actual first-use path.

Begin here:

1. Preserve the one-sentence definition.
2. Keep the minimum flow visible before the full initialization path.
3. Link deeper doctrine instead of repeating all of it in the README.
4. Keep `SOT.md` as the generic default.
5. Frame prompt files as optional support for initialization, repair, audit, pruning, and realignment.

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
- initialization prompt assumes the agent has already read this repository;
- prompt allows confident inference;
- prompt does not mention pruning;
- prompt does not protect human corrections;
- prompt names self-unfolded documents but does not explain when to split them out;
- prompt tells agents to hide YAIML files by default;
- prompt allows raw secrets or speculative legal/IP statements into project memory.

Begin here:

1. Compare the prompt to `docs/CORE_DOCUMENT_FAMILY.md`.
2. Add explicit evidence, ambiguity, conflict, and pruning behavior.
3. Keep it provider-neutral.

### Hydration Loads Too Much

Symptoms:

- hydrate prompt tells agents to read all supporting documents for every task;
- stable headers recursively require unrelated domains;
- `yaiml.yml` is treated as a mandatory loading list instead of a discovery index;
- routine tasks become whole-project audits.

Begin here:

1. Read `docs/CONTEXT_LOADING.md`.
2. Restore the discovery, core, task-relevant, and deep-reference layers.
3. Make the agent report what it skipped and why.

### The Repository Gets Bigger But Not Clearer

Symptoms:

- new terms are introduced without removing older equivalent terms;
- new templates exist without concrete recurring knowledge they would hold;
- README explains internal YAIML vocabulary before the adoption problem;
- additions do not help a fresh agent reconstruct current project understanding.

Begin here:

1. Read `docs/SoTY.md` North Star and Immediate Priorities.
2. Remove or simplify the addition unless it improves project-memory continuity.
3. Prefer refining an existing document, prompt, or template over adding another artifact.
