# Minimal Notes YAIML Example

This is a tiny fictional example that shows the smallest useful YAIML shape.

It has:

- `yaiml.yml` for discovery;
- `AGENTS.md` so future AI sessions know to read YAIML first;
- `SOT.md` for current state;
- `ARCHITECTURE.md` for durable system shape;
- `MAINTAINER_GUIDE.md` for procedures.

It intentionally has no application code and no supporting YAIML documents. The point is to show that YAIML can start small.

## Short Paste-And-Go Demo

Use an empty scratch folder outside existing repositories, with a repository-capable agent. This is a fictional documentation exercise, not an app build or adoption trial. No downloads or installs are needed.

Give the agent this brief, followed by the contents of [Init YAIML](../../prompts/init-yaiml.md):

> This scratch project is Minimal Notes. Its intended v1 lets one person create, edit, search, and delete plain-text notes locally. Keep v1 local-only; sync is deferred. There is no application source yet. Initialize project memory only. Do not build the app, install anything, or commit. Record missing design decisions as unknown.

Review the result: three concise core documents, a discovery map, and one agent-instruction pointer. Local-only is declared intent; the absence of application source prevents runtime claims. There should be no empty supporting documents or invented test results. The files in this example illustrate a possible shape, not exact required output.

Start a fresh session in that same scratch folder with only this request:

> Read this project's YAIML memory. What is v1 meant to do, what actually exists, what is deferred, and what still needs a human decision? Cite the local documents. Do not implement anything.

Check that the answer recovers local-only intent, deferred sync, and the lack of application code without receiving the original conversation. Then request:

> Compress YAIML if useful. Preserve the local-only decision, deferred sync, and unverified implementation status. Leave already-concise memory unchanged.

Explain the value in one sentence: project decisions survive the conversation, while uncertainty stays visible. Save actual failures if you run the demo; this walkthrough is not a measured success result. For real-project comparisons, use [Evaluation](../../docs/EVALUATION.md).
