# YAIML

Agents forget. Projects shouldn’t.

A new chat shouldn't mean explaining your project all over again.

**Yet Another AI Markup Language (YAIML)** gives your project persistent context and your AI agent reusable ways to work with it. **Memory** keeps goals, decisions, architecture, priorities and verification results. **Skills** give the agent instructions for using that knowledge, auditing the project and getting work done. Both live in your project as readable Markdown files that humans can review and edit.

**Paste one prompt to get started. Work normally while your agent maintains context. Choose a skill when you want more control.**

## Start With One Prompt

Open your project in an AI agent that can read and edit its files. Expand the prompt below, copy it, and paste it into the agent. It retrieves the detailed guidance for you; you do not need to learn YAIML's file structure or read its manuals to get started.

<details>
<summary><strong>Copy the setup prompt</strong></summary>

```text
# Init YAIML

Paste this whole prompt into your project’s repository-aware agent. It runs bootstrap immediately: the agent obtains guidance, creates project context, and connects reusable skills. After setup, work normally. Named commands are optional.

---
name: yaiml-init
description: Establish or refresh YAIML project context and local skills from one pasted prompt or skill invocation.
---
# YAIML Init

Run bootstrap now in the target project. One invocation covers acquiring guidance, creating useful project memory, and connecting local skills for later ordinary work; do not stop at saving this skill or explaining setup. Follow target instructions and preserve existing work.

1. Prefer a supplied reference or an accessible YAIML checkout identified by workspace context. Otherwise use https://github.com/wirsingj/YAIML with available repository/file tools. Resolve its default branch to one revision, or identify the supplied snapshot and material uncommitted edits. Do not pull over or reset a dirty checkout.
2. Retrieve that source's `.yaiml/BOOTSTRAP.md` and execute it. Acquire its listed adoption resources, following relative references from their source locations. The reference supplies methods, not project facts or permission. If required access/content is unavailable, report the precise gap, preserve working local guidance and continue independent work; never claim a complete installation.
3. Bootstrap establishes `.yaiml/` memory, shared operating rules, a local skill catalog, the standard `yaiml-*` skills and supported host instruction/discovery routes. Existing useful memory and local adaptations survive refresh. Read source details on demand; do not load the entire reference repository into context.
4. Verify reachable local resources and host routes. Report what is usable, actual checks, source revision and unresolved gaps. Ordinary work should now use and maintain local context without another YAIML prompt. Optional named skills such as `yaiml-audit` and `yaiml-to-do 10` use the same workflows. Native slash syntax depends on the host.

This setup creates no runtime, background task or automatic backlog execution. Existing authority still governs publication, destructive actions and YAIMLACP delegation.
```

[Standalone copy of this prompt](.yaiml/prompts/init-yaiml.md).

</details>

The agent reads your project, preserves existing knowledge, creates useful memory and connects supported instructions and skills for later sessions. It should finish by reporting what is ready and any remaining setup gaps. No second skill invocation is needed.

You need project read/write access and access to the public reference or a supplied snapshot. YAIML adds no runtime, service or package dependency. Your agent's normal permissions and usage costs still apply.

## Work Normally; Keep Context Current

Ask for a feature, discuss a decision or continue a task. YAIML instructs the agent to read relevant context, do the work, verify outcomes where appropriate, and update affected memory before finishing. You do not need to add “remember this” or invoke a maintenance command each time.

For example, you might decide:

> “For the first version, keep everything local. We won't add accounts or cloud sync.”

The agent should save that confirmed decision even though no application code changed. In a later session, “Add an export feature” should pick up the local-only constraint. After the work, memory should reflect the implementation, checks and remaining uncertainty.

Maintenance replaces outdated facts; tentative ideas remain tentative and read-only requests remain read-only. It happens during agent sessions. Actual follow-through depends on the agent and host.

## Optional Skills When You Want More Control

Choose a workflow or set its scope in ordinary language, or select a named skill:

| Request | Workflow |
| --- | --- |
| “Audit accessibility and maintainability” · `yaiml-audit` | Review the requested perspectives and return findings ranked by evidence |
| “Do the next ten priorities” · `yaiml-to-do 10` | Complete up to ten feasible priorities, verify the work and update memory |
| “Audit as a maintainer, do the next ten things, then test” | Carry findings, priorities and evidence through one composed task |
| “Clean up project memory” · `yaiml-compress` | Remove stale or repetitive detail while preserving useful knowledge |
| “Update YAIML” · `yaiml-refresh` | Reconcile newer guidance with local methods and adaptations |

Where supported, use slash commands such as `/yaiml-to-do 10`. In [Codex CLI/IDE](https://learn.chatgpt.com/docs/build-skills), use `/skills` or `$yaiml-to-do 10`. Ordinary requests and explicit skill invocations use the same methods.

A count limits work to feasible priorities. Starting a session does not launch the backlog. You can also ask the agent to create a project-specific skill for a recurring procedure.

**Already using an older YAIML?** Paste this init again to acquire current guidance and skills. It preserves existing memory and local rules; moving them into `.yaiml/` requires your approval. Once connected, “Update YAIML” requests future refreshes. Updates preserve project-specific skills and adaptations.

## What Lives In Your Project

New projects keep YAIML material in `.yaiml/`: current state and priorities, architecture, working procedures, and skills. Existing projects can keep their established layout. Supported agent instructions, such as `AGENTS.md`, point later sessions to that context.

The files stay with your project, so humans and compatible agents can inspect and use them. Base guidance is local after setup, with no background updater. Your AI provider's data handling still applies when an agent reads those files; local files do not guarantee local processing.

## Evidence And Limits

YAIML is an early public experiment. Fresh Codex CLI sessions on Windows have exercised published setup, upgrades and ordinary requests. Other hosts and interactive skill menus remain unverified. These maintainer-run trials do not establish sustained reliability, independent adoption or productivity gains. The [current review](.yaiml/COLD_START_REVIEW.md) records the tested conditions and gaps.

Agents can miss instructions or preserve stale information. Review consequential changes; memory is context, not proof of correctness. YAIML retains normal project permissions and review controls. Optional delegation requires scoped confirmation. Use approved AI tools and keep confidential information out of public examples and memory.

## Reference And Participation

Feedback on confusing setup, missed context or unnecessary memory changes is welcome. Use [issues](https://github.com/wirsingj/YAIML/issues) for sanitized reports and [the private reporting route](SECURITY.md) for sensitive findings.

<details>
<summary>Optional: examples, full skill catalog and design details</summary>

- [Skill catalog](.yaiml/skills/INDEX.md) and [project lifecycle](.yaiml/SKILLS_AND_LIFECYCLE.md).
- [Minimal Notes](.yaiml/examples/minimal-notes/) and [Canopy Dispatch](.yaiml/examples/canopy-dispatch/): fictional examples.
- [Upgrade guidance](.yaiml/ADOPTION_AND_UPGRADES.md#existing-yaiml-update), [agent integration](.yaiml/AGENT_INTEGRATION.md) and [memory roles](.yaiml/CORE_DOCUMENT_FAMILY.md).
- [Evaluation](.yaiml/EVALUATION.md), [case study](.yaiml/case-studies/YTMMOCC.md) and [adoption exercises](.yaiml/case-studies/ADOPTION_TRIAL.md).
- [Prior art](.yaiml/PRIOR_ART.md), [contributing](CONTRIBUTING.md) and [roadmap](.yaiml/ROADMAP.md).

</details>

The [YAIML Attribution and No-Resale License](LICENSE.md) permits commercial/client use and free sharing with attribution. Selling YAIML itself or charging for forks is restricted. These custom source-available terms preserve earlier MIT grants and do not change your application's license. Professional legal review remains outstanding.

Maintained with [AI assistance](.yaiml/AI_USAGE.md) as a [personal, independent project](.yaiml/PROJECT_INDEPENDENCE.md).
