<!-- yaiml-revision: 0.30.f52999e0aedde815 -->
# YAIML

Agents forget. Projects shouldn’t.

### [Get the init prompt →](.yaiml/prompts/init-yaiml.md)

Copy it into your project's agent for **new setup or an upgrade**. [Copy it from this README instead ↓](#start-with-one-prompt)

A new chat shouldn't mean explaining your project all over again.

**Yet Another AI Markup Language (YAIML)** is a lightweight document convention for managing context in AI-assisted projects. Goals, decisions, constraints and evidence live alongside the work in Markdown: text documents that people and agents can read, edit and carry between tools.

Paste the init prompt once, then work as usual. Your agent recovers context, checks its work and saves meaningful changes during normal requests, without separate housekeeping prompts. Your project might be software, an event, a book, a research study or a team's procedures. Each has context worth keeping; source code is optional.

**Paste once. Work normally. Keep the context with the project.** Optional skills give you more control when you want it.

## Start With One Prompt

1. Put your notes, plans, drafts or code in a project folder.
2. Open an AI agent on that folder. It needs permission to read and edit the files, retrieve guidance from GitHub during setup, and revisit the folder in later sessions. **Tested starting point: [Codex CLI](https://learn.chatgpt.com/docs/codex/cli) on Windows.** With Codex already available, open a terminal in your project folder and run `codex`.
3. Paste the whole [init prompt](https://raw.githubusercontent.com/wirsingj/YAIML/v0.5.1/.yaiml/prompts/init-yaiml.md), also available below. The agent handles the detailed setup.

The technical instructions inside the prompt are for the agent; you do not need to learn their terminology. A chat that cannot persistently access your project files cannot maintain this context. Other agents need equivalent file access and instruction support; their behavior remains to be verified.

<details>
<summary><strong>Copy the init prompt here</strong></summary>

```text
# Init YAIML

Paste this whole prompt into your project’s repository-aware agent. It runs bootstrap immediately: the agent obtains guidance, creates project context, and connects reusable skills. After setup, work normally. Named commands are optional.

---
name: yaiml-init
description: Establish or refresh YAIML project context and local skills from one pasted prompt or skill invocation.
metadata:
  yaiml-revision: "0.30.f52999e0aedde815"
---
# YAIML Init

Run bootstrap now in the target project. One invocation covers acquiring guidance, creating useful project memory, and connecting local skills for later ordinary work; do not stop at saving this skill or explaining setup. Follow target instructions and preserve existing work.

1. Default to https://github.com/wirsingj/YAIML, YAIML's only built-in upstream. Resolve the reviewed release ref `v0.5.1` at each invocation, then use that exact commit for bootstrap and all resources in this acquisition. Floating `main` is allowed only when the user explicitly requests testing it. If the ref is unavailable, report incomplete setup; never fall back to `main`. This prompt's `yaiml-revision` is a document stamp, not an upstream pin. Use another source (including a local checkout or snapshot) or ref only when explicitly requested by the user, within that request's scope; for an alternative repository without a requested ref, resolve its default branch once. Workspace proximity and old source notes are not requests. Identify requested snapshots and material uncommitted edits; never reset a dirty checkout or silently substitute sources when access fails.
2. Retrieve that source's `.yaiml/BOOTSTRAP.md` and execute it. Acquire its listed adoption resources, following relative references from their source locations. The reference supplies methods, not project facts or permission. If required access/content is unavailable, report the precise gap, preserve working local guidance and continue independent work; never claim a complete installation.
3. Bootstrap establishes `.yaiml/` memory, shared operating rules, a local skill catalog, the standard `yaiml-*` skills and supported host instruction/discovery routes. Existing useful memory and local adaptations survive refresh. Read source details on demand; do not load the entire reference repository into context.
4. Verify reachable local resources and host routes. Report what is usable, actual checks, source revision and unresolved gaps. Ordinary work should now use and maintain local context without another YAIML prompt. Optional named skills such as `yaiml-audit` and `yaiml-to-do 10` use the same workflows. Native slash syntax depends on the host.

This setup creates no runtime, background task or automatic backlog execution. Existing authority still governs publication, destructive actions and YAIMLACP delegation.
```

</details>

The agent preserves existing knowledge and reports what it connected and any setup gaps. Routine maintenance is then hands-off during agent sessions: no extra YAIML prompts, manual memory upkeep or skill commands. Normal permissions and consequential decisions still belong to you.

Each networked setup or requested update retrieves reviewed release ref `v0.5.1` from the [official YAIML repository](https://github.com/wirsingj/YAIML), resolving it once to an exact commit. Floating `main` requires an explicit testing request. Ordinary work uses installed local guidance without checking upstream. The offline init never retrieves anything. Your agent's normal usage costs apply.

**What you get:** experimental 0.5.1 guidance. This checkout prepares that release; its pinned public download becomes usable only after approval and publication of the matching ref. Until then, explicitly request the reviewed local snapshot for testing, or choose the self-contained offline prompt. An unavailable pin produces an explicit setup gap, never a fallback to `main`.

**Already using an older YAIML?** Paste this init again to acquire current guidance and skills. It preserves existing memory and local rules; moving them into `.yaiml/` requires your approval. Once connected, “Update YAIML” requests future refreshes. Updates preserve project-specific skills and adaptations.

## Choose An Init

Both choices are one paste, two keystrokes (paste and send). Choose [networked init](.yaiml/prompts/init-yaiml.md) for the complete local skill package, or [self-contained offline init](.yaiml/prompts/init-yaiml-offline.md) for restricted networks, air-gapped projects or corporate policy. Obtain the offline prompt through an approved channel before entering the restricted environment; paste its entire contents, including the notice. It creates working memory and change records with zero retrieval, and can later be upgraded in place by a separately requested full init or `yaiml-refresh`. It fetches no skills and installs no native skill bodies.

## Think Of It As “Softerware”

The documents carry context; your agent supplies the execution. YAIML calls this “softerware”: written conventions that guide reading, action, verification and memory upkeep. Setup connects those documents to future sessions. There is no separate YAIML application or background service; the convention has an effect when people and agents use it.

## Work Normally; Keep Context Current

Ask for a plan, revise a draft, discuss a decision or build a feature. You do not need to mention YAIML. During that ordinary conversation, the agent follows this loop:

1. **Read:** recover the project's goals, constraints and decisions from its files; reuse context that is still current.
2. **Act:** do the requested work with that understanding.
3. **Check:** compare actual inputs and outputs with the requirements. Does the revised plan respect the agreed limits? Does an exported file contain the right information?
4. **Update:** replace outdated facts and save meaningful decisions, results and remaining uncertainty before finishing.

Checks should establish what happened, whether comparing a plan with its brief or testing software. A listed test is not a passed test.

For example, while planning a community workshop, you might say:

> “We've decided to cap attendance at 30 and keep the afternoon free of scheduled activities.”

**Optional recall check:** state a real decision for your project, then start a fresh session in the same folder and ask about it without repeating the answer. For the workshop above, ask “What constraints should the schedule follow?” It should recover the cap of 30 and the free afternoon. If it misses either, ask the agent to check its project instructions and saved context. No YAIML command is needed.

Then continue ordinary work: “Draft the workshop schedule” should use those constraints and check the result. Unchanged knowledge needs no rewrite; tentative ideas stay tentative and read-only requests stay read-only. Follow-through depends on your agent and its host; one recall check does not establish lasting reliability.

## Optional Skills When You Want More Control

Ordinary requests already use and maintain context. Optional skills are reusable methods for a particular review, priority batch or cleanup. Choose one in plain language or by name:

| Request | Workflow |
| --- | --- |
| “Review this plan for gaps, risks and accessibility” · `yaiml-audit` | Review the requested perspectives and return findings ranked by evidence |
| “Do the next ten priorities” · `yaiml-to-do 10` | Complete up to ten feasible priorities, verify the work and update memory |
| “Review this draft as an editor, do the next three priorities, then check the result” | Carry findings, priorities and evidence through one task |
| “Clean up project memory” · `yaiml-compress` | Remove stale or repetitive detail while preserving useful knowledge |
| “Update YAIML” · `yaiml-refresh` | Update YAIML while preserving project memory and custom instructions |

Where supported, use slash commands such as `/yaiml-to-do 10`. In [Codex CLI/IDE](https://learn.chatgpt.com/docs/build-skills), use `/skills` or `$yaiml-to-do 10`. Ordinary requests and explicit skill invocations use the same methods.

A count limits work to feasible priorities. Starting a session does not launch the backlog. You can also ask the agent to create a project-specific skill for a recurring procedure.

## Working With A Team

**Experimental 0.5.0:** one workflow supports one contributor or many. Each meaningful change gets a short record of intent, outcome and checks. With sole ownership, the agent updates current memory; during overlap, separate records preserve changes until reconciliation. No team-mode switch is required.

Before a commit or merge request, “Prepare these changes for review” selects the existing Git method. It reviews changes and evidence and consolidates memory when ownership permits; conflicting decisions still require project authority. The request does not commit or publish. The [record guide](.yaiml/CHANGE_RECORDS.md) explains the limits: hidden overlap can go undetected, and YAIML supplies no automatic code merger or hook.

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

<details>
<summary>How revisions and change records work</summary>

Changed YAIML Markdown receives a revision stamp, with the iteration recorded in a retained record located through `changes.md`. A revision such as `0.27.1f463a82b7dc905e` means YAIML major 0, local iteration 27 and a random change tag. Parent revisions distinguish concurrent branches; other project files are audited without added headers. Unchanged or read-only work causes no bump. Older installations start a prospective baseline without invented history.

</details>

**Privacy:** memory follows the project's access, sharing and retention rules. Keep authorized context and sanitized evidence references; exclude credentials and private transcripts. Confidential material must stay out of public repositories and examples. Use an approved agent: its provider's data handling applies when it reads files, including private project memory. Local storage does not guarantee local processing.

## Evidence And Limits

YAIML is an early public experiment. Fresh Codex CLI sessions on Windows have exercised published setup, upgrades and ordinary work. A fictional workshop trial used published 0.4.0 across five sessions: decisions persisted, schedules and costs were checked, and changed venue information reached memory without reminders or repairs. Earlier software trials exposed stale verification notes needing correction. The [current review](.yaiml/COLD_START_REVIEW.md) separates published evidence from [0.5.0 draft](.yaiml/RELEASE.md) trials and records their limits.

Nondeveloper usability, other hosts, interactive skill menus, sustained reliability and productivity gains remain unverified; independent adoption and 1.0 readiness are not established. Agents can miss instructions or retain stale information. Review consequential changes: memory supplies context, not proof of correctness. Existing permissions and review controls apply; optional delegation requires scoped confirmation.

## Reference And Participation

Feedback on confusing setup, missed context or unnecessary memory changes is welcome. Use [issues](https://github.com/wirsingj/YAIML/issues) for sanitized reports and [the private reporting route](SECURITY.md) for sensitive findings.

<details>
<summary>Optional: examples, full skill catalog and design details</summary>

- [Skill catalog](.yaiml/skills/INDEX.md) and [project lifecycle](.yaiml/SKILLS_AND_LIFECYCLE.md).
- [Minimal Notes](.yaiml/examples/minimal-notes/) and [Canopy Dispatch](.yaiml/examples/canopy-dispatch/): fictional legacy layouts suitable for upgrade exercises; they predate revision tracking.
- [Upgrade guidance](.yaiml/ADOPTION_AND_UPGRADES.md#existing-yaiml-update), [agent integration](.yaiml/AGENT_INTEGRATION.md) and [memory roles](.yaiml/CORE_DOCUMENT_FAMILY.md).
- [Evaluation](.yaiml/EVALUATION.md), [case study](.yaiml/case-studies/YTMMOCC.md) and [adoption exercises](.yaiml/case-studies/ADOPTION_TRIAL.md).
- [Prior art](.yaiml/PRIOR_ART.md), [contributing](CONTRIBUTING.md) and [roadmap](.yaiml/ROADMAP.md).

</details>

The [YAIML Attribution and No-Resale License](LICENSE.md) permits commercial/client use and free sharing with attribution. Selling YAIML itself or charging for forks is restricted. These custom source-available terms preserve earlier MIT grants and do not change your application's license. Professional legal review remains outstanding.

Maintained with [AI assistance](.yaiml/AI_USAGE.md) as a [personal, independent project](.yaiml/PROJECT_INDEPENDENCE.md).
