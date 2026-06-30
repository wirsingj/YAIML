# Initialize YAIML In An Existing Project

You are a coding agent adding YAIML living project memory to an existing repository.

Do not change application code during initialization unless the human explicitly asks for code changes.

## Task

1. Inspect the repository broadly: source, tests, configuration, docs, scripts, package files, existing agent instructions, and visible project history.
2. Identify the project type, current shape, intent, risks, and uncertainty.
3. Create or update `yaiml.yml` so it declares the three core YAIML documents. Prefer `documents.sot`, `documents.architecture`, and `documents.maintainer`.
4. Create or update the SoT document. Use `SOT.md` only as a neutral fallback; when the project has an obvious larger thing, prefer a project-specific filename such as `SoTC.md` for captions, `SoTT.md` for table, or `SoTP.md` for project/product. Do not name SoT after a narrow subsystem or the current task.
5. Create or update Architecture.
6. Create or update Maintainer Guide.
7. Add concise stable headers at the top of each YAIML document.
8. Distinguish verified current implementation from declared intent, inference, unknowns, and divergence.
9. Keep the initial SoT bounded. Do not create a permanent history.

## Rules

- Human instructions and explicit decisions define intent.
- Code, tests, commands, and runtime behavior define implementation evidence.
- Do not describe desired behavior as already implemented.
- Do not turn guesses into project canon.
- Do not add generic filler.
- Do not create a CLI, SDK, parser, provider adapter, package manifest, or web app.
- Preserve existing human directives.

## Output

Report:

- files created or changed;
- evidence inspected;
- project model summary;
- verified facts;
- declared intent;
- inferred or unknown areas;
- known divergence;
- recommended next steps.
