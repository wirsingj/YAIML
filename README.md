<!-- yaiml-revision: 0.48.57e622f47b1fbd54 -->
# YAIML

**Yet Another AI Markup Language (YAIML)** is a lightweight document standard for starting, organizing and maintaining projects with AI.

Paste one prompt into your agent to set up shared project memory. The full setup also adds reusable skills. Everything lives alongside your work in readable Markdown files; there is no separate YAIML app or service to install.

Start with an idea, a few notes or an existing project. Your agent establishes useful context: goals, constraints, decisions and next steps. As you work, it uses that context, checks results and saves meaningful updates. That understanding stays with the project for later sessions.

Use it for software, research, writing, event planning or team procedures. You and your agent can read and edit the same documents.

Want to look around first? Start with the [documentation guide](docs/README.md) or [examples](examples/README.md).

## Start With One Prompt

| Prompt | What your agent does |
| --- | --- |
| [Full setup: skill-based, networked](reference/prompts/init-yaiml.md) | Starts with a short prompt; the agent follows its instructions to retrieve the full guidance, templates and reusable skills. Requires access to the approved source (this repo) during setup. |
| [Self-contained setup (offline)](reference/prompts/init-yaiml-offline.md) | Uses instructions and templates embedded in one document to create project memory and working rules. Makes no network calls and does not include the reusable skill package. |

The self-contained option suits restricted networks and organizations that need to review the complete prompt before use. Obtain it through an approved channel before entering a restricted environment. A later, separately requested full setup can add the skill package.

1. **Open a project folder in your agent.** It needs permission to read and edit the files and revisit them in later sessions. Start with your notes, plans, drafts or code; for a new idea, create a folder and describe what you want to do.
2. **Open one prompt file above, copy its entire contents, then paste and send it to your agent.** Include the complete text and notice. The technical instructions are for the agent; you do not need to learn their terminology.
3. **Review the setup summary, then work normally.** The agent reports what it created or connected and any gaps. Ask it to draft a plan, review your work or take the next step.

Published setup has been exercised with [Codex CLI](https://learn.chatgpt.com/docs/codex/cli) on Windows. Other agents need equivalent file access and instruction support; their behavior remains to be verified. A chat without persistent access to your project files cannot maintain this context. Your agent's normal usage costs apply.

<details>
<summary>Existing projects, upgrades and source selection</summary>

Setup preserves existing knowledge and local rules. The full prompt can also update an older YAIML setup; moving established memory into `.yaiml/` requires your approval. Once connected, "Update YAIML" requests a refresh that preserves project-specific skills and adaptations. The offline prompt never retrieves anything, including on repeat use.

Networked setup and requested updates use the public-ready `latest` tag from the [official repository](https://github.com/wirsingj/YAIML). The agent resolves it once and uses that exact commit throughout acquisition, recording the version and source locally. A missing tag stops acquisition; it never silently substitutes a branch or local draft. Ordinary work uses local guidance without checking upstream.

</details>

## Work Normally; Keep Context Current

Ask for a plan, revise a draft, discuss a decision or build a feature. You do not need to mention YAIML. Its guidance asks your agent to:

1. **Read:** recover the project's goals, constraints and decisions from its files; reuse context that is still current.
2. **Act:** do the requested work with that understanding.
3. **Check:** compare actual inputs and outputs with the requirements. Does the revised plan respect the agreed limits? Does an exported file contain the right information?
4. **Update:** replace outdated facts and save meaningful decisions, results and remaining uncertainty before finishing.

For example, while planning a community workshop, you might say:

> “We've decided to cap attendance at 30 and keep the afternoon free of scheduled activities.”

The agent should save those constraints and use them when you ask it to draft the schedule. Unchanged knowledge needs no rewrite; tentative ideas stay tentative and read-only requests stay read-only.

<details>
<summary>Try a fresh-session recall check</summary>

State a real decision for your project, then start a fresh session in the same folder and ask about it without repeating the answer. For the workshop above, ask “What constraints should the schedule follow?” It should recover the cap of 30 and the free afternoon. If it misses either, ask the agent to check its project instructions and saved context. No YAIML command is needed.

Follow-through depends on your agent and its host; one recall check does not establish lasting reliability.

</details>

## Optional Skills When You Want More Control

Full setup adds reusable skills for reviews, priorities, verification and memory upkeep. Calling them by name is optional: ordinary requests already use the same guidance. For more focused work, ask in plain language:

| Request | Skill and outcome |
| --- | --- |
| “Review this plan for gaps, risks and accessibility” | `yaiml-audit`: findings from the requested perspectives, ranked by evidence |
| “Do the next ten priorities” | `yaiml-to-do`: up to ten feasible priorities completed, checked and recorded |
| “Clean up project memory” | `yaiml-compress`: stale or repetitive detail removed while preserving useful knowledge |
| “Update YAIML” | `yaiml-refresh`: guidance updated while preserving project memory and custom instructions |

You can combine requests: “Review this draft as an editor, do the next three priorities, then check the result.” You can also ask the agent to create a project-specific skill for a recurring procedure.

Where supported, use slash commands such as `/yaiml-to-do 10`. In [Codex CLI/IDE](https://learn.chatgpt.com/docs/build-skills), use `/skills` or `$yaiml-to-do 10`. Ordinary requests and explicit skill invocations use the same methods.

A count limits work to feasible priorities. Starting a session does not launch the backlog.

## Working With A Team

**Experimental 0.5.2:** one workflow supports one contributor or many. Each meaningful change gets a short record of intent, outcome and checks. With sole ownership, the agent updates current memory; during overlap, separate records preserve changes until reconciliation. No team-mode switch is required.

Before a commit or merge request, “Prepare these changes for review” selects the existing Git method. It reviews changes and evidence and consolidates memory when ownership permits; conflicting decisions still require project authority. The request does not commit or publish. The [record guide](reference/CHANGE_RECORDS.md) explains the limits: hidden overlap can go undetected, and YAIML supplies no automatic code merger or hook.

## What Lives In Your Project

New projects keep YAIML material in `.yaiml/`: current state and priorities, project structure, working procedures, a `changes.md` audit, and reusable methods. Existing projects can keep their layout. Agent instructions, such as `AGENTS.md`, point later sessions to the documents.

An illustrative excerpt after workshop planning and verification could read:

```markdown
- Confirmed: Attendance is capped at 30; afternoons stay free.
- Tentative: A second workshop date has been suggested, not approved.
- Checked: The draft schedule respects the attendance and timing limits.
- Open: The venue booking is still unconfirmed.
```

The actual documents retain relevant sources and uncertainty; the audit records what changed, why, affected files and actual checks. They preserve useful understanding rather than whole conversations. You can inspect or edit the text, or correct a decision in ordinary conversation and let the agent maintain it.

YAIML calls this “softerware”: the documents carry context and methods; your agent supplies the execution. Maintenance happens during agent sessions.

<details>
<summary>How revisions and change records work</summary>

Changed YAIML Markdown receives a revision stamp, with the iteration recorded in a retained record located through `changes.md`. A revision such as `0.27.1f463a82b7dc905e` means YAIML major 0, local iteration 27 and a random change tag. Parent revisions distinguish concurrent branches; other project files are audited without added headers. Unchanged or read-only work causes no bump. Older installations start a prospective baseline without invented history.

This repository's `reference/` folder contains what other projects adopt. Our own `.yaiml/` project memory is not part of setup.

</details>

**Privacy:** memory follows the project's access, sharing and retention rules. Keep authorized context and sanitized evidence references; exclude credentials and private transcripts. Confidential material must stay out of public repositories and examples. Your agent's data-handling rules apply when it reads files, including private project memory. Local storage does not guarantee local processing.

For organizational security review, [retrieval and internal mirrors](docs/ADOPTION_AND_UPGRADES.md#security-review-retrieval-and-internal-mirrors) explains what is fetched, when, source/ref controls and self-hosting.

## Evidence And Limits

YAIML is an early public experiment. Fresh Codex CLI sessions on Windows have exercised published setup, upgrades and ordinary work. A fictional workshop trial used published 0.4.0 across five sessions: decisions persisted, schedules and costs were checked, and changed venue information reached memory without reminders or repairs. Earlier software trials exposed stale verification notes needing correction. The [current review](docs/evaluation/COLD_START_REVIEW.md) separates published evidence from 0.5.0 draft trials and records their limits.

Nondeveloper usability, other hosts, interactive skill menus, sustained reliability and productivity gains remain unverified; independent adoption and 1.0 readiness are not established. Agents can miss instructions or retain stale information. Review consequential changes: memory supplies context, not proof of correctness. Existing permissions and review controls apply; optional delegation requires scoped confirmation.

<details>
<summary>Detailed trial evidence</summary>

The [0.5.1 check](docs/evaluation/EVALUATION.md#post-review-cross-host-trial-gate-2026-10-24) adds source/package checks and a manual offline fixture. Later [isolated StateMesh trials](docs/evaluation/EVALUATION.md#statemesh-local-upgrade-trial-2026-10-24) exercised a manual upgrade, external writer repair and one live Codex CLI synthesis under bounded synthetic gates; a separate [supplied document trial](docs/evaluation/EVALUATION.md#yaiml-document-reconciliation-trial-2026-10-24) checked retained decisions/history and rejecting controls. These do not establish general reliability, autonomous semantic document merging or fresh memory recall. The requested additional-host trials remain blocked: neither Claude Code nor Copilot was available on this host. No fresh-session or enforced-network-disabled result is claimed for the new offline prompt.

The [0.5.2 structural correction](docs/evaluation/COLD_START_REVIEW.md#structural-distribution-check) separates reusable material from our own project memory. File/link checks and both prompt payloads have been checked; fresh-agent setup and upgrade trials for this layout are still pending.

</details>

## Find Your Way Around

| Location | What's there |
| --- | --- |
| [reference/](reference/) | The reusable product: init prompts, skills, templates and operating guidance. |
| [docs/](docs/README.md) | Explanations, design notes, evaluation evidence and contributor guidance. |
| [examples/](examples/README.md) | Fictional projects you can explore. |
| [ROADMAP.md](ROADMAP.md) | Where YAIML is headed and what still needs evidence. |
| [.yaiml/](.yaiml/) | This repository's own project memory, change records and local methods. |

The last folder is YAIML being used to develop YAIML. You do not need it to adopt the convention or understand the product. Our agent instructions point there for contributor context; public documentation and examples live outside it.

## Participation

Feedback on confusing setup, missed context or unnecessary memory changes is welcome. Use [issues](https://github.com/wirsingj/YAIML/issues) for sanitized reports and [the private reporting route](SECURITY.md) for sensitive findings.

<details>
<summary>Optional: examples, full skill catalog and design details</summary>

- [Skill catalog](reference/skills/INDEX.md) and [project lifecycle](docs/SKILLS_AND_LIFECYCLE.md).
- [Minimal Notes](examples/minimal-notes/) and [Canopy Dispatch](examples/canopy-dispatch/): fictional legacy layouts suitable for upgrade exercises; they predate revision tracking.
- [Upgrade guidance](docs/ADOPTION_AND_UPGRADES.md#existing-yaiml-update), [agent integration](docs/AGENT_INTEGRATION.md) and [memory roles](docs/CORE_DOCUMENT_FAMILY.md).
- [Evaluation](docs/evaluation/EVALUATION.md), [case study](docs/evaluation/case-studies/YTMMOCC.md) and [adoption exercises](docs/evaluation/case-studies/ADOPTION_TRIAL.md).
- [Prior art](docs/PRIOR_ART.md), [contributing](CONTRIBUTING.md) and [roadmap](ROADMAP.md).

</details>

The [YAIML Attribution and No-Resale License](LICENSE.md) permits commercial/client use and free sharing with attribution. Selling YAIML itself or charging for forks is restricted. These custom source-available terms preserve earlier MIT grants and do not change your application's license. Professional legal review remains outstanding.

Maintained with [AI assistance](docs/AI_USAGE.md) as a [personal, independent project](docs/PROJECT_INDEPENDENCE.md).
