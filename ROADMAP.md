# YAIML Roadmap

YAIML is in an early public convention-first phase. The current goal is to make the SoT-centered, self-unfolding project-memory pattern immediately useful without tooling.

The long-term ambition is industry-standard adoption. The path is practical: keep adoption cheap, prove usefulness in real projects, invite outside feedback, and let maturity claims follow evidence.

The current init paths are `prompts/init-yaiml.md` for quick adoption and `prompts/initialize-yaiml.md` for deeper repository setup. The primary adoption route is still copy/paste prompt text, not a download, install, dependency, runtime, or package format. A better init helper may come later, but it should still produce and maintain plain YAIML files in the user's project.

Near-term work should make the existing philosophy clearer, smaller, and more durable before adding more framework surface.

## Maturity Ladder

- YAIML 0.2: usable experiment. Freeze the tiny core around `yaiml.yml`, SoT, Architecture, Maintainer Guide, discovery/loading behavior, evidence states, and update/pruning expectations while testing adoption.
- YAIML 0.3: public pilot. Keep the core stable, publish clear adoption/reporting paths, and collect outside feedback across multiple AI-chat and coding-agent providers.
- YAIML 0.5: implemented draft. Show use in unrelated projects, document incompatibilities and failures, and demonstrate at least one external or separately maintained helper or workflow.
- YAIML 1.0: stable convention. Freeze the core contract, publish migration expectations, and support maturity claims with independent adopters and real case-study evidence.

## Now

- Test the templates on real repositories.
- Improve the prompt pack through actual AI-chat, agent, and contributor handoff sessions.
- Keep YAIML's own SoTY, Architecture, and Maintainer Guide short and honest.
- Add only examples that reveal how the pattern behaves in use.
- Refine self-unfolding document guidance so agents add useful supporting documents without creating empty ceremony.
- Keep the minimum viable adoption path smaller than the full initializer.
- Apply the cold-start evaluation method to real repositories without fabricating proof, including at least one mature local repo, one unfamiliar public repo, and one repo owned by another developer.
- Check YAIML 0.2 readiness by initializing or upgrading YAIML in repositories intended to move across machines, contributors, and AI chat provider instances, then verifying the generated memory remains useful without exposing private material.
- Prepare a concise enterprise-safe KT/demo path for a manager or senior-engineering audience: explain the repeated-context problem, show copy/paste initialization, demonstrate fresh-session recovery, and keep examples sanitized and policy-safe.
- Enable GitHub private vulnerability reporting, or document another maintainer-approved private contact path, before broader public pilot readiness.
- Keep the `yaiml.yml` discovery protocol tiny, versioned, and limited to paths for project memory.
- Reduce terminology where ordinary engineering language works.
- Avoid drifting back into schemas for Markdown memory documents, conformance fixtures, parser design, or standards-body language.

## Near Next

- Collect real failure cases where AI chats, agents, or contributors misunderstood intent, implementation, or risk.
- Refine the stable header until it is strong enough to guide agents and short enough to tolerate.
- Refine context-loading guidance from real AI-chat and agent sessions.
- Record real-project case studies using the evaluation template, keeping internal portfolio trials separate from independent adoption evidence.
- Improve self-unfolded document guidance for preferences, terms, risk review, security, domain models, product rules, operations, release, and legal/compliance memory.
- Create a brutally simple public demo: initialize YAIML in an unfamiliar repository, then open a fresh session and show whether the project can be recovered from repo memory.
- Adapt that demo for constrained enterprise AI tools without making any one provider, workplace process, or internal toolchain part of YAIML itself.
- Recruit a small pilot group across Codex, Claude Code, Cursor, Gemini CLI, and one local-model workflow before making broad adoption claims.
- Develop manual review checklists for project-memory quality.
- Prepare public release readiness criteria, including contribution expectations for multi-contributor projects, examples, evidence requirements, clear license communication, a simple adoption-report path, and a visible decision process.
- Decide whether future validation should exist for `yaiml.yml` only, while preserving Markdown memory as human-authored plain text.

## Later

Possible later work:

- an init helper for creating or refreshing project-local YAIML files;
- stale-claim auditing;
- document pruning assistance;
- editor snippets;
- provider-specific prompt variants;
- team review workflows;
- document health checks.

These remain deferred until the plain Markdown memory workflow and helper prompts prove themselves.

Not planned during the convention-first phase: runtime services, databases, storage layers, orchestration frameworks, package-manager dependencies, web applications, SDKs, provider adapters, or validators for Markdown memory documents.

## Still Human-Decided

YAIML now uses the MIT License for public use while preserving Jeff Wirsing's copyright ownership. Do not change the license, add license headers, or make new trademark, ownership, or endorsement claims without explicit maintainer approval.

Still human-decided: release labeling, broader contribution governance, evidence thresholds for maturity claims, the private sensitive-reporting channel, and whether future tooling should ever exist.
