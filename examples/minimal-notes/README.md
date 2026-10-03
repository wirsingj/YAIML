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

Use an empty scratch folder outside existing repositories, with a repository-capable agent. This is a fictional documentation exercise, not an app build or adoption trial. No downloads or installs are needed.

Give the agent this brief, followed by the contents of [Init YAIML](../../prompts/init-yaiml.md):

> This scratch project is Minimal Notes. Its intended v1 lets one person create, edit, search, and delete plain-text notes locally. Keep v1 local-only; sync is deferred. There is no application source yet. Initialize project memory only. Do not build the app, install anything, or commit. Record missing design decisions as unknown.

Review the result: three concise core documents, discovery, a supported agent-instruction pointer, and local operating guidance, templates, and YAIMLACP from the embedded text, with its copied-material notice. Local-only is declared intent; absent source prevents runtime claims. There should be no empty specialist documents, downloads, workers, or invented test results. Existing equivalent guidance may be reused.

Start a fresh session in that same scratch folder with only this request:

> What is v1 meant to do, what actually exists, what is deferred, and what still needs a human decision? Cite the local documents. Do not implement anything.

Check that the answer recovers local-only intent, deferred sync, and the lack of application code without receiving the original conversation or a YAIML reminder. Then say:

> Change the intended v1 scope: defer search too. Keep create, edit, and delete. Do not build application code.

The agent should update affected memory before finishing without being told to do so. A later fresh session asked “What is deferred from v1?” should recover both search and sync. If reading or writing is missed, record the failure and check the instruction route; do not count manual prompting as successful automatic integration.

For an optional explicit maintenance demonstration, request:

> Compress YAIML if useful. Preserve the local-only decision, deferred search and sync, and unverified implementation status. Leave already-concise memory unchanged.

Explain the value in one sentence: project decisions survive the conversation, while uncertainty stays visible. Save actual failures if you run the demo; this walkthrough is not a measured success result. For real-project comparisons, use [Evaluation](../../docs/EVALUATION.md).
