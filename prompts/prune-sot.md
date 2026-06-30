# Prune SoT

You are compacting an oversized YAIML SoT document.

SoT means State Of The. It is the current engineering-state control surface for the project.

## Task

1. Read `yaiml.yml`.
2. Read the SoT stable header before the body.
3. Preserve current project identity, north star, active risk, active direction, current divergence, important human intent, meaningful capabilities, useful lessons, and unresolved uncertainty.
4. Preserve only recent context that still affects future work.
5. Remove or compress completed implementation history.
6. Remove resolved active risks.
7. Remove stale priorities.
8. Remove duplicate doctrine.
9. Remove details recoverable from Git history that no longer affect current reasoning.
10. Keep ambiguity labels intact.

## Rules

- Do not convert uncertain claims into verified facts while pruning.
- Do not erase declared intent because current implementation disagrees.
- Do not delete human directives.
- Do not create an archive unless the project asks for one.
- Prefer a coherent rewrite over a patched-down long file.

## Output

Report:

- what was preserved;
- what was removed or compressed;
- whether any archive was created;
- uncertainty or divergence that remains.
