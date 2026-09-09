# Compress YAIML Project Memory

You are cleaning up and compressing YAIML project memory after it has become stale, repetitive, too long, or too much like a work log.

This is not a feature implementation task. Do not change application code unless the human explicitly asks.

## Task

1. Read `yaiml.yml`.
2. Read repository agent instructions such as `AGENTS.md`, `CLAUDE.md`, `GEMINI.md`, `.cursorrules`, `.windsurfrules`, `.cursor/rules/*`, or `.windsurf/rules/*` when present.
3. Check the current worktree state before editing. Treat uncommitted changes as intentional work in progress.
4. Read the stable headers for the core YAIML documents before their bodies.
5. Load supporting YAIML documents only when they appear stale, oversized, duplicated, or relevant to the cleanup request.
6. Identify current project memory that should be preserved: project identity, north star, active risk, active direction, current divergence, important human intent, meaningful capabilities, current procedures, useful lessons, and unresolved uncertainty.
7. Remove or compress completed implementation history, stale priorities, duplicate doctrine, resolved active risks, dead commands, moved paths, obsolete procedures, and details recoverable from Git history that no longer affect current reasoning.
8. Replace stale verification summaries with the latest known verification state instead of appending a new log entry.
9. Preserve observed facts, declared intent, inference, disagreement, unknowns, and obsolete material without upgrading their certainty.
10. Do not promote old successful checks into current verification without evidence.
11. Keep evidence labels and uncertainty intact.
12. Update only affected YAIML documents.

## Rules

- Preserve the distinct jobs of SoT, Architecture, Maintainer Guide, and supporting documents.
- Do not convert uncertain claims into verified facts while compressing.
- Do not add rationale, behavioral detail, or verification absent from the evidence. Preserve the gap or inspect additional evidence before making a stronger claim.
- Do not erase declared intent because current implementation disagrees.
- Do not delete human directives.
- Do not remove unresolved risks, open questions, or known divergence just because they are old.
- Do not store secrets, credentials, private transcripts, raw sensitive logs, sensitive raw values, or speculative legal/IP conclusions.
- Respect governed retention rules. Legal, compliance, audit, contract, agreement, incident, or decision-history material may require human approval before destructive pruning.
- Do not create an archive unless the project asks for one.
- Prefer a coherent rewrite over a patched-down long file.
- Check declared word budgets using their stated method, or whole-document whitespace-delimited counts including headers. Report before/after counts and retained overages. Preserve necessary knowledge and governed retention; do not inflate a budget or delete facts merely to fit.
- Use Git history as the archive for old completed work.
- Confirm detail is committed or otherwise safely retained before relying on history. Re-read concurrently changed files before writing; preserve other contributors' work. Removing sensitive text does not erase prior exposure or Git history.

## Output

Report:

- what was preserved;
- what was removed or compressed;
- which YAIML documents changed;
- whether any archive was created;
- uncertainty or divergence that remains.
