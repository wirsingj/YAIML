# YAIML

Agents forget. Projects shouldn’t.

**Yet Another AI Markup Language** is a context and project management convention for humans and AI agents. It keeps the project's understanding in ordinary Markdown and gives agents reusable skills for working with it: orienting, auditing, completing priorities, verifying results and keeping that understanding current.

## Start With One Prompt

Paste [Init YAIML](.yaiml/prompts/init-yaiml.md) into your project's repository-aware agent. The prompt contains a bootstrap skill that runs immediately. It identifies the public reference, retrieves the needed guidance and skills, creates useful project context, and connects the agent's supported instruction files. No prior YAIML knowledge, manual downloads or second skill invocation is required.

Use a prompt whose reference resources have been published together. A supplied development snapshot can also be used; an unpublished local change is not available to a new user through the public URL. [Current review](.yaiml/COLD_START_REVIEW.md) records what has actually been checked.

The agent needs project read/write access and either reference access or a supplied snapshot. It reports missing access or unsupported persistence rather than claiming setup worked. YAIML introduces no runtime, service or package dependency. Your existing documents and decisions remain the starting point.

After setup, **work normally**. Ask for a feature, discuss a project decision or continue a task. Connected instructions tell the agent to read relevant context, do the work and maintain material understanding before finishing. You do not need to remember a YAIML maintenance command.

**Already using an older YAIML?** Paste the current init into that project again. It can add the new skills even when the old installation has no skill catalog or recorded source. Existing memory and local rules are reconciled; moving them into `.yaiml/` requires your approval. See [upgrading an existing project](.yaiml/ADOPTION_AND_UPGRADES.md#existing-yaiml-update).

## Optional Skills When You Want More Control

| Request | Result |
| --- | --- |
| `/yaiml-audit accessibility, maintainability` | Review the requested perspectives and return evidence-ranked findings |
| `/yaiml-to-do 10` | Complete up to ten feasible priorities, verify the work and update memory |
| “Audit as a maintainer, do the next ten things, then test” | Carry findings, priorities and evidence through one composed task |
| `/yaiml-compress` | Synthesize stale or repetitive memory while preserving useful knowledge |
| “Update YAIML” | Reconcile newer guidance with local methods and adaptations |

Slash commands are available where the host supports them; use that host's native syntax or ordinary language otherwise. In [Codex CLI/IDE](https://learn.chatgpt.com/docs/build-skills), use `/skills` or `$yaiml-to-do 10`. The same local methods support both interaction styles. Setup connects the supported discovery route and reports gaps. See the [skill catalog](.yaiml/skills/INDEX.md) for orientation, maintenance, verification, growth and realignment too.

A count is a work limit, not a demand to invent tasks. Audits preserve uncertainty; tests are reported as passed only when actually run under the stated conditions. Ordinary startup does not launch the backlog.

## What Lives In Your Project

New adoption keeps YAIML-owned material in `.yaiml/`:

| Resource | Responsibility |
| --- | --- |
| `SOT.md` — State Of The project | Current direction, capabilities, risks, uncertainty and priorities |
| `ARCHITECTURE.md` | Durable boundaries, responsibilities and intended design |
| `MAINTAINER_GUIDE.md` | Procedures, checks, recovery and current YAIML source/adaptation notes |
| `yaiml.yml` | Paths to the actual memory owners and supporting resources |
| `skills/INDEX.md` and `skills/yaiml-*/SKILL.md` | Discoverable methods and their workflows |
| `YAIML_GUIDE.md`, `YAIMLACP.md`, templates and notice | Shared operating rules, optional coordination, writing aids and copied-material attribution |

Host instructions such as `AGENTS.md` stay where the host expects them. They route future sessions to memory and skills. Existing mature layouts remain usable; a requested relocation preserves knowledge and repairs consumers.

Memory holds project facts; skills read those facts when they act. A recurring domain topic can grow into a supporting document, and a useful recurring method can grow into a project-specific `yaiml-` skill. Unused templates stay dormant. Local knowledge and skills survive convention refreshes, which reconcile changes rather than replace the project with a generic template.

The base resources are local after init. Agents load relevant material, reuse current context and acquire extra reference material only for a concrete need. Updates record the reference revision and preserve local adaptations. No background process or routine upstream polling is implied. [Skills And Project Lifecycle](.yaiml/SKILLS_AND_LIFECYCLE.md) explains the design.

## Evidence And Limits

YAIML is an early public experiment with the ambition of broader adoption. The [YTMMOCC case](.yaiml/case-studies/YTMMOCC.md) and [local adoption exercises](.yaiml/case-studies/ADOPTION_TRIAL.md) are maintainer-owned evidence. Earlier trials do not establish that the new skills lifecycle works across hosts. [Evaluation](.yaiml/EVALUATION.md) defines trials; [Cold Start Review](.yaiml/COLD_START_REVIEW.md) distinguishes structural checks from observed behavior.

The agent and host still determine whether instructions are loaded and followed. Memory costs context and requires upkeep; stale or overgrown files can mislead. Project intent, implementation and verification remain distinct. Optional [YAIMLACP](.yaiml/YAIMLACP.md) uses existing host subagents only after its scoped confirmation; it adds no infrastructure.

## Reference And Participation

- [Minimal Notes](.yaiml/examples/minimal-notes/) and [Canopy Dispatch](.yaiml/examples/canopy-dispatch/): fictional memory examples; Minimal Notes includes a cold-start walkthrough.
- [Core Document Family](.yaiml/CORE_DOCUMENT_FAMILY.md), [Context Loading](.yaiml/CONTEXT_LOADING.md) and [Agent Integration](.yaiml/AGENT_INTEGRATION.md): ownership, reading and activation.
- [Adoption And Updates](.yaiml/ADOPTION_AND_UPGRADES.md), [Ambiguity And Evidence](.yaiml/AMBIGUITY_AND_EVIDENCE.md) and [Pruning And Lifecycle](.yaiml/PRUNING_AND_LIFECYCLE.md): compatibility and trustworthy maintenance.
- [Concepts](.yaiml/CONCEPTS.md), [Prior Art](.yaiml/PRIOR_ART.md), [Contributing](CONTRIBUTING.md) and [Roadmap](.yaiml/ROADMAP.md): background and future direction.

The [YAIML Attribution and No-Resale License](LICENSE.md) allows use in commercial products and client work. Give credit to YAIML and Jeff Wirsing; you may not sell YAIML itself or charge for access to a modified or rebranded fork. Free sharing and free forks are allowed. These are custom, source-available terms; they preserve rights already granted for earlier MIT releases and do not set your application's license. Professional legal review is still needed before publishing these new terms.

Maintained with [AI assistance](.yaiml/AI_USAGE.md) as a [personal, independent project](.yaiml/PROJECT_INDEPENDENCE.md). Follow [Security And Sensitive Information](SECURITY.md), and keep the applicable license and attribution with copied YAIML material.
