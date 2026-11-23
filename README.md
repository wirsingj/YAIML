<!-- yaiml-revision: 0.63.7ce032a3b160d120 -->
# YAIML

**Pick up the project. Skip the recap.**

Every new AI conversation needs the context: what you're building, what you've decided, what failed, and what's next. YAIML gives that understanding a home in your project.

**Yet Another AI Markup Language** is shared project memory in ordinary Markdown. Its instructions ask your agent to read the relevant context before working and keep it current afterward. You can read, edit and review those same files—and take them into the next chat, tool or teammate's checkout.

**[Start with one prompt →](reference/prompts/init-yaiml.md)** · [See an example](examples/current-memory/README.md) · [Explore the skills](reference/skills/INDEX.md)

## Keep What Matters

A useful handoff might look like this:

```text
Goal: A tool my friend can run without a development environment.
Decided: Windows first. No account required.
Checked: The packaged app launches on my machine.
Still unknown: Whether it works on a clean machine.
Next: Test the recipient's launch path.
```

The next agent has a starting point: the goal, the constraints, the evidence and the unfinished work. Human decisions stay distinguishable from guesses and untested plans.

YAIML brings three habits together:

- **Carry decisions forward.** Keep goals, constraints and rationale available across sessions.
- **Keep understanding current.** Replace stale summaries as the project changes; preserve meaningful changes in an audit.
- **Make work explicit.** Use written methods for reviewing, implementing, verifying and maintaining the project.

Your existing agent does the work. YAIML supplies the guidance and files—there is no separate app, server or runtime to install. It can sit alongside existing specs, issues and documentation.

## Start With One Prompt

1. Open your project folder in an agent that can read and write files.
2. Copy the **[full setup prompt](reference/prompts/init-yaiml.md)**, including its notice, and send it to the agent.
3. Review what it created or connected, then work normally.

Start with an existing project or an idea in an empty folder. Setup connects project memory and reusable skills to supported agent instructions; you do not need to keep mentioning YAIML.

Need setup without downloads? The **[offline prompt](reference/prompts/init-yaiml-offline.md)** embeds memory guidance but does not install the skill collection. Your AI may still need a network connection. [Setup, compatibility and upgrades →](docs/ADOPTION_AND_UPGRADES.md)

## Give The Work Some Structure

Ask for what you need:

> “Audit the project, complete the next five feasible priorities, then verify the results.”

Or repeat a workflow:

> “Use yaiml-loop: audit, then yaiml-to-do 5. Repeat that sequence five times.”

The loop carries updated findings into each cycle and reports completed work and early stops. Skills also cover packaging, diagrams, Git work and memory cleanup. They run through your agent, within its permissions; they are not background jobs.

[Browse the methods and their instructions →](reference/skills/INDEX.md)

Setup installs the published `latest` revision; this checkout's catalog may include additions that are not published yet.

## Evidence And Limits

YAIML is an **early public experiment**. Maintainer-run trials have shown some fresh-session recall and memory maintenance, alongside missed updates and unnecessary reading. Sustained reliability, broader host support and productivity gains remain unproven. [Read the evidence →](docs/evaluation/COLD_START_REVIEW.md)

Review consequential changes. Your agent's costs, permissions and data handling still apply; storing memory locally does not guarantee local processing. [Security and privacy →](SECURITY.md)

## Find Your Way Around

[Examples](examples/README.md) · [How the memory files fit together](docs/CORE_DOCUMENT_FAMILY.md) · [Full documentation](docs/README.md) · [Reusable guidance](reference/) · [Roadmap](ROADMAP.md)

This repository's own development memory lives in [.yaiml/](.yaiml/); it is not copied into adopting projects.

Tried it? Tell us where context was lost or where the process got in your way. [Report an issue](https://github.com/wirsingj/YAIML/issues) · [Contribute](CONTRIBUTING.md)

---

By **Jeff Wirsing**, a [personal, independent project](docs/PROJECT_INDEPENDENCE.md) developed with [AI assistance](docs/AI_USAGE.md).

[Custom source-available license](LICENSE.md): commercial/client use and free sharing with attribution are allowed; selling YAIML or paid forks is restricted. Earlier MIT grants remain intact. Your project keeps its own license.
