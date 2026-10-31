<!-- yaiml-revision: 0.55.e4878e79e2960300 -->
# YAIML

**Yet Another AI Markup Language (YAIML)** is a document standard that keeps your project's memory in ordinary files in your repository or project folder on your computer. Goals, decisions, constraints and current understanding live in readable Markdown, not just in an AI conversation.

You and your agents read and update the same files. They can travel with the project in Git, so a new chat, another contributor or a different AI tool can read the saved context without inheriting the previous conversation. There is no separate YAIML app or hosted memory service.

Paste one prompt to set it up, then work normally. Start with an idea, a few notes or an existing project; your agent creates or connects the documents, reads relevant context and saves meaningful updates as you work.

Use it for software, research, writing, event planning or team procedures.

Want to look around first? Start with the [documentation guide](docs/README.md) or [examples](examples/README.md).

## Start With One Prompt

| Prompt | What your agent does |
| --- | --- |
| [Full setup (networked)](reference/prompts/init-yaiml.md) | Fetches reusable guidance and templates from this repo, including skills: Markdown instructions for recurring work. |
| [Self-contained setup (offline)](reference/prompts/init-yaiml-offline.md) | Creates memory from the embedded guidance and templates. Retrieves nothing and adds no skill package. |

The self-contained option lets you review the entire setup before use. Obtain it before entering a restricted environment. "Offline" describes setup retrieval, not where your chosen AI runs. You can request full setup later to add skills.

1. **Open your project folder in an agent with file access.** Use your existing work, or an empty folder and a description of your idea.
2. **Copy a complete prompt above, including its notice, and send it to your agent.** The setup instructions are for the agent; you do not need to learn their terminology.
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

The skills included with full setup guide the agent; they are not extra agents or background jobs. Calling them by name is optional; ordinary requests use the same guidance. For focused work, ask in plain language:

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

Individuals and teams use the same document workflow. Contributors share changes through the project's normal version-control and review process; YAIML does not synchronize chats or resolve disagreements for them. Each meaningful change gets a short record of intent, outcome and checks. With sole ownership, the agent updates current memory; during overlap, separate records preserve changes until reconciliation.

Before a commit or merge request, “Prepare these changes for review” selects the existing Git method. It reviews changes and evidence and consolidates memory when ownership permits; conflicting decisions still require project authority. The request does not commit or publish. The [record guide](reference/CHANGE_RECORDS.md) explains the limits: hidden overlap can go undetected, and YAIML supplies no automatic code merger or hook.

## What Lives In Your Project

New setups keep these files in `.yaiml/`; existing projects can keep their layout. The SoT (State Of The) holds current understanding and priorities, Architecture explains lasting structure, and the Maintainer Guide holds working procedures. `changes.md` retains the audit. Supporting documents appear only when actual project knowledge needs a separate home.

Instruction files such as `AGENTS.md` or `CLAUDE.md` tell an agent how to work and where to read this memory. They point to the same project knowledge rather than duplicating it for each tool.

An illustrative excerpt after workshop planning and verification could read:

```markdown
- Confirmed: Attendance is capped at 30; afternoons stay free.
- Tentative: A second workshop date has been suggested, not approved.
- Checked: The draft schedule respects the attendance and timing limits.
- Open: The venue booking is still unconfirmed.
```

These are curated summaries, not chat transcripts. Human corrections replace stale claims rather than accumulating beneath them; sources and unresolved questions stay visible.

YAIML calls this “softerware”: the documents carry context and methods; your agent supplies the execution. Maintenance happens during agent sessions.

<details>
<summary>How revisions and change records work</summary>

Changed YAIML Markdown receives a revision stamp, with the iteration recorded in a retained record located through `changes.md`. A revision such as `0.27.1f463a82b7dc905e` means YAIML major 0, local iteration 27 and a random change tag. Parent revisions distinguish concurrent branches; other project files are audited without added headers. Unchanged or read-only work causes no bump. Older installations start a prospective baseline without invented history.

</details>

**Privacy:** memory follows the project's access, sharing and retention rules. Keep authorized context and sanitized evidence references; exclude credentials and private transcripts. Confidential material must stay out of public repositories and examples. Your agent's data-handling rules apply when it reads files, including private project memory. Local storage does not guarantee local processing.

For organizational security review, [retrieval and internal mirrors](docs/ADOPTION_AND_UPGRADES.md#security-review-retrieval-and-internal-mirrors) explains what is fetched, when, and how to use a reviewed internal copy of the guidance.

## Evidence And Limits

YAIML is an early public experiment. Maintainer-run Codex CLI trials on Windows have recovered decisions in fresh sessions and maintained memory during ordinary work. They also exposed stale verification notes and unnecessary reading. The [current review](docs/evaluation/COLD_START_REVIEW.md) separates published and draft trials, successes and failures.

The layout introduced in 0.5.2 passed source/package checks and public retrieval. Later guidance changes have their own scoped checks; fresh-session setup and upgrade acceptance remain pending. File checks do not establish agent behavior.

Nondeveloper usability, other hosts, interactive skill menus, sustained reliability and productivity gains remain unverified; independent adoption and 1.0 readiness are not established. Agents can miss instructions or retain stale information. Review consequential changes: memory supplies context, not proof of correctness. Existing permissions and review controls apply; optional delegation requires scoped confirmation.

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
