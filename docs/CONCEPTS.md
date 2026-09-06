---
yaiml: 0.2
kind: concept-guide
title: Concepts
purpose: Explain YAIML's conceptual frame and vocabulary for AI Project Engineering.
belongs-here: core philosophy, project-memory concepts, strong-bones/soft-definitions framing, human-agent authority model.
not-here: current project priorities, command procedures, complete template inventory.
durability: durable; update when YAIML's conceptual frame changes materially.
read-with: SoTY; Core Document Family; Ambiguity And Evidence.
update-when: YAIML's meaning, audience, or core conceptual vocabulary changes.
agent-guidance: Preserve the lightweight convention-first frame. Do not turn concepts into schema or conformance language.
---

# Concepts

YAIML means Yet Another AI Markup Language: a convention for keeping shared project understanding in a repository. Its audience includes AI chats, coding agents, and human contributors.

A development conversation mixes decisions, experiments, corrections, and obsolete ideas. YAIML preserves the part that should survive the conversation: what the project currently is, what humans intend, what evidence establishes, and what future work must account for.

## Design Choices

- **Plain files:** ordinary Markdown is editable, searchable, reviewable in Git, and usable without YAIML software. The small discovery file locates the documents.
- **Distinct roles:** SoT holds current state, Architecture holds durable design, and Maintainer Guide holds procedures. [Core Document Family](CORE_DOCUMENT_FAMILY.md) explains placement.
- **Explicit uncertainty:** declared intent and implementation evidence may disagree. Preserve both until evidence or an authorized decision resolves the difference.
- **Synthesis:** replace stale state rather than accumulating a session diary. Keep rejected approaches only while they prevent repeated mistakes.
- **Selective reading:** the core should stay short; supporting documents enter context when relevant to the task.
- **Local fit:** roles and responsibilities remain recognizable while filenames, headings, and supporting topics fit the project.

“AI Project Engineering” describes the combination of technical artifacts and human engineering direction in AI-assisted work. It is background vocabulary, not another process adopters must learn.

“Self-unfolding” means splitting recurring knowledge into a supporting document when it outgrows a core role or needs different retention. It does not mean generating empty documents in advance.

## Relationship To Other Documentation

YAIML does not claim to have invented persistent Markdown context. It brings current-state synthesis, evidence distinctions, role separation, and pruning into one convention.

Agent instructions tell a session how to work. Feature specs define desired changes; issues track work; changelogs record history. YAIML preserves the current understanding that connects these sources and points back to them. Reuse existing documentation that already fills a role.

The code is evidence of implementation, not proof that the implementation reflects approved intent. For example:

```text
Declared (product decision): the desktop host is a player, not the DM.
Verified by source inspection: two UI labels still call the host “DM”.
Divergence: implementation copy conflicts with product direction.
```

Do not rewrite the decision to match the labels or claim the labels have been fixed.

## Shared Ownership

Humans govern direction; agents can maintain the memory. Follow the project’s actual decision and review authority. Multiple contributors can leave contradictions even when Git merges cleanly; preserve the sources and uncertainty instead of silently choosing a story.

Memory should normally travel with its repository, regardless of business or licensing model. Keep it appropriate for that repository’s audience and access rules. Use sanitized evidence references rather than private transcripts or sensitive values. Professional constraints belong here as reviewed decisions and open questions, not agent-invented conclusions.

## Tradeoffs

Memory takes effort to maintain and consumes context. A stale summary can mislead; excessive splitting can make reading harder. A project whose existing documentation already carries this understanding may gain little from additional files.

YAIML’s current phase favors trying the plain-file workflow and recording failures before adding tooling or claiming standard status. The [evaluation guide](EVALUATION.md) describes how to gather evidence.
