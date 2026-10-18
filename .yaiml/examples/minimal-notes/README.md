# Minimal Notes YAIML Example

This is a tiny fictional example focused on YAIML's core memory roles.

It has:

- `yaiml.yml` for discovery;
- `AGENTS.md` so future AI sessions know to read YAIML first;
- `SOT.md` for current state;
- `ARCHITECTURE.md` for durable system shape;
- `MAINTAINER_GUIDE.md` for procedures.

It intentionally has no application code or specialist project memory. This core-only illustration omits the reusable operating guide, dormant templates, and YAIMLACP that standalone init saves locally. It is not a complete snapshot of init output.

## Short Paste-And-Go Demo

Use an empty scratch folder outside existing repositories, with a repository-capable agent. This is a fictional documentation exercise, not an app build or adoption trial. The agent retrieves reference files during setup; no runtime installation is needed.

Give the agent this brief, followed by the contents of [Init YAIML](../../prompts/init-yaiml.md):

> This scratch project is Minimal Notes. Its intended v1 lets one person create, edit, search, and delete plain-text notes locally. Keep v1 local-only; sync is deferred. There is no application source yet. Initialize project memory only. Do not build the app, install anything, or commit. Record missing design decisions as unknown.

For a published-source trial, give the agent only that brief and the init prompt. For an unpublished development trial, additionally supply an isolated reference snapshot and label that difference; no maintainer checkout or conversation context is implied. Record any host-injected YAIML instructions or skill descriptions before calling the trial a clean cold start.

Review the result: three useful core documents, discovery, supported persistent instructions, a local skill catalog and bodies, shared rules, dormant starters, YAIMLACP and copied-material notice. Check every required local skill reference. Local-only is declared intent; absent source prevents runtime claims. Init should acquire resources itself, not ask the user to paste more workflows, build the app, install dependencies, start workers or invent test results.

Start a fresh session in that same scratch folder with only this request:

> What is v1 meant to do, what actually exists, what is deferred, and what still needs a human decision? Cite the local documents. Do not implement anything.

Check that the answer recovers local-only intent, deferred sync, and the lack of application code without receiving the original conversation or a YAIML reminder. Then say:

> Change the intended v1 scope: defer search too. Keep create, edit, and delete. Do not build application code.

The agent should update affected memory before finishing without being told to do so. A later fresh session asked “What is deferred from v1?” should recover both search and sync. If reading or writing is missed, record the failure and check the instruction route; do not count manual prompting as successful automatic integration.

For an optional explicit maintenance demonstration, request:

> Compress YAIML if useful. Preserve the local-only decision, deferred search and sync, and unverified implementation status. Leave already-concise memory unchanged.

Explain the value in one sentence: project decisions survive the conversation, while uncertainty stays visible. Save actual failures if you run the demo; this walkthrough is not a measured success result. For real-project comparisons, use [Evaluation](../../EVALUATION.md).

## Optional Skill And Lifecycle Checks

In a separate fresh session, request `yaiml-audit` through the host's supported syntax or natural language, with maintainability as the perspective. Check evidence and read-only behavior. For a bounded documentation task, request “Define the note fields and export expectations, then verify the docs”; check material memory updates without a YAIML reminder. Do not count invented implementation as completion.

A project with at least ten authorized actionable priorities can test `/yaiml-to-do 10`. With fewer, expect an honest partial count. Test a composed request using the same acceptance criteria; separate commands must not be required. Introduce a recurring project method, then verify growth creates a useful reachable skill rather than a competing fact store.

For refresh, preserve a known local skill and an adapted upstream passage, then apply a changed reference. Check both survive compatible updates, overlapping conflicts remain visible, and an unchanged repeat produces no churn. Disconnect the reference for a later session: ordinary local methods should remain usable. These are trial instructions, not recorded passes.
