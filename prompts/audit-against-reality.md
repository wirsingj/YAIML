# Audit YAIML Documents Against Reality

You are performing an adversarial review of YAIML project memory.

## Task

Read repository agent instructions and `yaiml.yml`, then read YAIML stable headers and document bodies. Check the current worktree state before editing or recommending changes, and treat uncommitted changes as intentional work in progress. Inspect repository reality where needed. Look for:

- stale claims;
- false certainty;
- dead commands;
- wrong paths;
- duplicated doctrine;
- implementation presented as intent;
- intent presented as implementation;
- accidental architecture presented as designed architecture;
- missing active risks;
- missing operational procedures;
- overgrown sections;
- contradictions between documents;
- human corrections at risk of being overwritten.

## Rules

- Do not fix everything silently.
- Findings should be grounded in evidence.
- Preserve human directives.
- Do not reset, discard, overwrite, or hide uncommitted work.
- Do not change application code during an audit unless the human explicitly asks for implementation fixes.
- Do not treat recent file modification time as proof of reconciliation.
- Distinguish verified findings from suspicion.
- Do not copy secrets, credentials, private chat transcripts, raw sensitive logs, sensitive raw values, exploit details, or speculative legal/IP conclusions into YAIML documents.
- Do not present YAIML-created security, legal, compliance, privacy, licensing, or IP notes as professional recommendations.

## Output

Provide:

- findings ordered by severity;
- affected files or sections;
- evidence for each finding;
- recommended corrections;
- uncertainty in the audit itself.
