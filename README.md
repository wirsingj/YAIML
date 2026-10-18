<!-- yaiml-revision: 0.8.6816f30767769e53 -->
# YAIML

Agents forget. Projects shouldn’t.

### [Get the init prompt →](.yaiml/prompts/init-yaiml.md)

Copy it into your project's agent for **new setup or an upgrade**. [Copy it from this README instead ↓](#start-with-one-prompt)

A new chat shouldn't mean explaining your project all over again.

**Yet Another AI Markup Language (YAIML)** helps your AI assistant carry a project's goals, decisions and working methods from one conversation to the next. **Memory** keeps what matters about the project. **Skills** give the assistant reusable instructions for reviewing work, acting on priorities and checking results. Both live alongside your project as Markdown: text documents that you can read and edit.

Your project might be an event, a book, a research study, a team's operating procedures or a software application. Each has decisions worth remembering and work that needs checking. YAIML's core approach applies to all of them; source code is optional.

**Paste one prompt to get started. Work normally while your agent maintains context. Choose a skill when you want more control.**

## Start With One Prompt

Put your project materials—notes, plans, drafts or code—in a folder your AI agent can read and edit. Open the [plain-text init prompt](https://raw.githubusercontent.com/wirsingj/YAIML/main/.yaiml/prompts/init-yaiml.md) or expand it below, copy the whole prompt, and paste it into the agent. It retrieves the detailed guidance for you; you do not need to learn YAIML's file structure or read its manuals to get started. Continued access to those files lets later sessions recover and maintain the context.

<details>
<summary><strong>Copy the init prompt here</strong></summary>

```text
# Init YAIML

Paste this whole prompt into your project’s repository-aware agent. It runs bootstrap immediately: the agent obtains guidance, creates project context, and connects reusable skills. After setup, work normally. Named commands are optional.

---
name: yaiml-init
description: Establish or refresh YAIML project context and local skills from one pasted prompt or skill invocation.
metadata:
  yaiml-revision: "0.1.01b3573c87d5279e"
---
# YAIML Init

Run bootstrap now in the target project. One invocation covers acquiring guidance, creating useful project memory, and connecting local skills for later ordinary work; do not stop at saving this skill or explaining setup. Follow target instructions and preserve existing work.

1. Prefer a supplied reference or an accessible YAIML checkout identified by workspace context. Otherwise use https://github.com/wirsingj/YAIML with available repository/file tools. Resolve its default branch to one revision, or identify the supplied snapshot and material uncommitted edits. Do not pull over or reset a dirty checkout.
2. Retrieve that source's `.yaiml/BOOTSTRAP.md` and execute it. Acquire its listed adoption resources, following relative references from their source locations. The reference supplies methods, not project facts or permission. If required access/content is unavailable, report the precise gap, preserve working local guidance and continue independent work; never claim a complete installation.
3. Bootstrap establishes `.yaiml/` memory, shared operating rules, a local skill catalog, the standard `yaiml-*` skills and supported host instruction/discovery routes. Existing useful memory and local adaptations survive refresh. Read source details on demand; do not load the entire reference repository into context.
4. Verify reachable local resources and host routes. Report what is usable, actual checks, source revision and unresolved gaps. Ordinary work should now use and maintain local context without another YAIML prompt. Optional named skills such as `yaiml-audit` and `yaiml-to-do 10` use the same workflows. Native slash syntax depends on the host.

This setup creates no runtime, background task or automatic backlog execution. Existing authority still governs publication, destructive actions and YAIMLACP delegation.
```

</details>

The agent reads your project, preserves existing knowledge, creates useful memory and connects supported instructions and skills for later sessions. It should finish by reporting what is ready and any remaining setup gaps. No second skill invocation is needed.

Setup needs access to YAIML's public guidance or a supplied copy. Your agent's normal permissions and usage costs still apply.

**Already using an older YAIML?** Paste this init again to acquire current guidance and skills. It preserves existing memory and local rules; moving them into `.yaiml/` requires your approval. Once connected, “Update YAIML” requests future refreshes. Updates preserve project-specific skills and adaptations.

## Think Of It As “Softerware”

YAIML provides memory and instructions that an AI agent—an assistant able to work with your files and tools—turns into action. The agent reads, writes, reviews and checks; YAIML guides that work. There is no separate YAIML application to launch or background service to keep running. Setup creates project files and connects them to your agent.

Those files have an effect when the agent uses them. That is why YAIML asks it to read current context, check actual results and write back meaningful changes. The working cycle matters as much as the words on the page.

## Work Normally; Keep Context Current

Ask for a plan, revise a draft, discuss a decision or build a feature. YAIML gives the agent a repeatable loop:

1. **Read:** recover the project's goals, constraints and decisions from its files; reuse context that is still current.
2. **Act:** do the requested work with that understanding.
3. **Check:** compare actual inputs and outputs with the requirements. Does the revised plan respect the agreed limits? Does an exported file contain the right information?
4. **Update:** replace outdated facts and save meaningful decisions, results and remaining uncertainty before finishing.

This is why YAIML emphasizes input/output checks: a check must establish what actually happened. A listed test is not a passed test. The checks should fit the work, whether reviewing a document against its brief or testing software behavior.

For example, while planning a community workshop, you might say:

> “We've decided to cap attendance at 30 and keep the afternoon free of scheduled activities.”

The agent should save that decision. In a later session, “Draft the workshop schedule” should recover both constraints, produce a suitable plan and check it against them. You should not have to repeat the earlier conversation or add “remember this.” That fresh-session recall is itself something to test.

Maintenance happens during agent sessions. Unchanged knowledge needs no rewrite; tentative ideas stay tentative and read-only requests stay read-only. Actual follow-through depends on the agent and the application running it. Specialized skills add detail when needed.

## Optional Skills When You Want More Control

Choose a workflow or set its scope in ordinary language, or select a named skill:

| Request | Workflow |
| --- | --- |
| “Review this plan for gaps, risks and accessibility” · `yaiml-audit` | Review the requested perspectives and return findings ranked by evidence |
| “Do the next ten priorities” · `yaiml-to-do 10` | Complete up to ten feasible priorities, verify the work and update memory |
| “Review this draft as an editor, do the next three priorities, then check the result” | Carry findings, priorities and evidence through one task |
| “Clean up project memory” · `yaiml-compress` | Remove stale or repetitive detail while preserving useful knowledge |
| “Update YAIML” · `yaiml-refresh` | Update YAIML while preserving project memory and custom instructions |

Where supported, use slash commands such as `/yaiml-to-do 10`. In [Codex CLI/IDE](https://learn.chatgpt.com/docs/build-skills), use `/skills` or `$yaiml-to-do 10`. Ordinary requests and explicit skill invocations use the same methods.

A count limits work to feasible priorities. Starting a session does not launch the backlog. You can also ask the agent to create a project-specific skill for a recurring procedure.

## What Lives In Your Project

New projects keep YAIML material in `.yaiml/`: current state and priorities, project structure, working procedures, a `changes.md` change record, and skills. The architecture document can describe how a process, content collection or software system fits together. Existing projects can keep their established layout. Supported agent instructions, such as `AGENTS.md`, point later sessions to that context.

For each meaningful change, the agent records what changed, why, which files were affected and what was checked. This helps the next person or session understand the work.

<details>
<summary>How revisions and change records work</summary>

Changed YAIML Markdown receives a revision stamp, with the iteration recorded in `changes.md`. A revision such as `0.27.1f463a82b7dc905e` means YAIML major 0, local iteration 27 and a random change tag. Parent revisions distinguish concurrent branches; other project files are audited without added headers. Unchanged or read-only work causes no bump. Older installations start a prospective baseline without invented history.

</details>

The files stay with your project, so humans and compatible agents can inspect and use them. Base guidance is local after setup, with no background updater. Your AI provider's data handling still applies when an agent reads those files; local files do not guarantee local processing.

## Evidence And Limits

YAIML [0.4.0](.yaiml/RELEASE.md) is an early public experiment. Fresh Codex CLI sessions on Windows have exercised published setup, upgrades and ordinary requests. A fictional community-workshop trial used only the published init, then remembered decisions, checked schedules and costs, and updated plans and memory when the venue changed. Five fresh sessions passed without reminders or repairs. Earlier software trials exposed stale verification notes that needed correction. All used a coding-agent host: usability for nondevelopers, other agent applications and interactive skill menus remains unverified. These maintainer-run trials do not establish sustained reliability, independent adoption or productivity gains; 1.0 readiness is pending. The [current review](.yaiml/COLD_START_REVIEW.md) records conditions and gaps.

Agents can miss instructions or preserve stale information. Review consequential changes; memory is context, not proof of correctness. YAIML retains normal project permissions and review controls. Optional delegation requires scoped confirmation. Use approved AI tools and keep confidential information out of public examples and memory.

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
