<!-- yaiml-revision: 0.48.57e622f47b1fbd54 -->
# YAIML Documentation

These pages explain YAIML, how its documents fit together and what we've tested. You do not need to read them all before getting started.

To use YAIML in a project, start with [full init](../reference/prompts/init-yaiml.md) or [offline init](../reference/prompts/init-yaiml-offline.md). To see what project memory looks like, explore the [examples](../examples/README.md).

## Read The Standard

For a fuller picture, these pages fit together in this order:

1. [Concepts](CONCEPTS.md): what YAIML preserves, why it exists and its tradeoffs.
2. [Core document family](CORE_DOCUMENT_FAMILY.md) and [stable headers](STABLE_HEADERS.md): what belongs where and how readers orient themselves.
3. [Evidence and uncertainty](AMBIGUITY_AND_EVIDENCE.md): intent, verified results, disagreement and unknowns.
4. [The working loop](../reference/YAIML_GUIDE.md), [context loading](CONTEXT_LOADING.md) and [pruning](PRUNING_AND_LIFECYCLE.md): keeping memory useful during ordinary work.
5. [Skills and project lifecycle](SKILLS_AND_LIFECYCLE.md): optional methods, composition and growth.
6. [Revision guidance](../reference/VERSIONING.md) and [change records](../reference/CHANGE_RECORDS.md): preserving changes across contributors without confusing memory with a log.

[Prior art](PRIOR_ART.md) puts these choices alongside existing documentation approaches. This reading path connects the maintained documents; it is not a separate specification or a requirement to adopt everything.

## Set Up Or Update

- [Adoption and updates](ADOPTION_AND_UPGRADES.md): discovery, existing projects, source selection and internal mirrors.
- [Agent integration](AGENT_INTEGRATION.md): connecting project instructions to memory.

The actual reusable methods, prompts and templates live in [reference/](../reference/), including the [operating guide](../reference/YAIML_GUIDE.md), [skill catalog](../reference/skills/INDEX.md), [revision guidance](../reference/VERSIONING.md) and [change-record rules](../reference/CHANGE_RECORDS.md). Init acquires that defined reference set, not this documentation tree.

## Evaluate It

- [Evaluation method and trial material](evaluation/EVALUATION.md): a case-study template, cold-start comparisons and recorded trials.
- [Review evidence and limits](evaluation/COLD_START_REVIEW.md): what has actually been checked.
- [Case studies and adoption exercises](evaluation/case-studies/): maintainer-run evidence, not proof of independent adoption.

## Develop YAIML

- [Roadmap](../ROADMAP.md) and [contributing](../CONTRIBUTING.md).
- [YAIML publication guidance](development/RELEASE.md): this repository's release process, not an adopting project's.
- [Historical intent-record prototype](development/INTENT_LOG_PROTOTYPE.md): design exploration, not current setup instructions.
- [AI assistance disclosure](AI_USAGE.md) and [project independence](PROJECT_INDEPENDENCE.md).

This repository also uses YAIML to manage its own development. Its current state, architecture summary, maintainer notes and retained change records live in [.yaiml/](../.yaiml/). That is contributor context, not another place to look for product documentation. Discovery can point to documents here without making them part of the memory folder.
