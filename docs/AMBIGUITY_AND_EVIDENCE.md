# Ambiguity And Evidence

YAIML documents should resist false certainty.

Generated prose naturally turns partial evidence into a confident story. A project-memory document is useful only if it keeps uncertainty visible where it matters.

## Truth Sources

YAIML separates different kinds of truth:

- human direction is authoritative about intended meaning and product direction;
- repository files, tests, commands, and runtime behavior are authoritative about current implementation reality;
- agent inference may guide work, but it is not project canon;
- future direction belongs in declared or planned sections, not verified current-state sections.

When these sources conflict, record the conflict. Do not silently merge them.

## Shared Vocabulary

Use these labels when a claim could steer future work:

- **Verified**: supported by named code, tests, runtime behavior, commands, or documents.
- **Declared**: stated as intent, policy, direction, or decision by a human or authoritative project document.
- **Observed**: seen in behavior but not fully traced.
- **Inferred**: plausible from available evidence but not verified.
- **Disputed**: sources disagree.
- **Unknown**: not currently established.
- **Obsolete**: previously relevant but no longer current.

Do not label every sentence. Use labels, sections, or short notes when ambiguity matters.

## Common Separations

SoT often separates:

- Verified Current State;
- Declared Direction;
- Active Risks;
- Known Divergence;
- Unverified Assumptions;
- Open Questions.

Architecture documents often separate:

- Current Architecture;
- Intended Architecture;
- Transitional Paths;
- Known Violations;
- Inferred Ownership;
- Retired Approaches;
- Open Architecture Questions.

Maintainer guides often separate:

- Verified Commands;
- Environment-Dependent Commands;
- Unverified Procedures;
- Failure Playbooks.

## Divergence

Divergence is not automatically a bug. It is often the most important thing to preserve.

```text
Declared: Authentication should be provider-neutral.
Verified: The request layer imports one provider SDK directly.
Divergence: Current implementation conflicts with intended architecture.
```

The agent should report the divergence, not rewrite the intended architecture to match accidental implementation.

## Evidence Notes

When practical, name evidence:

- files inspected;
- tests run;
- commands run;
- runtime behavior observed;
- human instruction or decision source.

When evidence is missing, say so.
