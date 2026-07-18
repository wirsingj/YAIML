# YAIML Roadmap

YAIML is in an incubation and convention-first phase. The current goal is to make the SoT-centered, self-unfolding project-memory pattern immediately useful without tooling.

The current init paths are `prompts/init-yaiml.md` for quick adoption and `prompts/initialize-yaiml.md` for deeper repository setup. A better init helper may come later, but it should still produce and maintain plain YAIML files in the user's project rather than turning YAIML into an installed dependency, runtime, or package format.

Near-term work should make the existing philosophy clearer, smaller, and more durable before adding more framework surface.

## Now

- Test the templates on real repositories.
- Improve the prompt pack through actual AI-chat, agent, and contributor handoff sessions.
- Keep YAIML's own SoTY, Architecture, and Maintainer Guide short and honest.
- Add only examples that reveal how the pattern behaves in use.
- Refine self-unfolding document guidance so agents add useful supporting documents without creating empty ceremony.
- Keep the minimum viable adoption path smaller than the full initializer.
- Apply the cold-start evaluation method to real repositories without fabricating proof.
- Check YAIML 0.2 readiness by initializing or upgrading YAIML in repositories intended to move across machines, contributors, and AI chat provider instances, then verifying the generated memory remains useful without exposing private material.
- Choose or document a private sensitive-reporting path before broad public release, or explicitly rely on GitHub private vulnerability reporting if enabled.
- Reduce terminology where ordinary engineering language works.
- Avoid drifting back into schemas, conformance fixtures, parser design, or standards-body language.

## Near Next

- Collect real failure cases where AI chats, agents, or contributors misunderstood intent, implementation, or risk.
- Refine the stable header until it is strong enough to guide agents and short enough to tolerate.
- Refine context-loading guidance from real AI-chat and agent sessions.
- Record real-project case studies using the evaluation template.
- Improve self-unfolded document guidance for preferences, terms, risk review, security, domain models, product rules, operations, release, and legal/compliance memory.
- Develop manual review checklists for project-memory quality.
- Prepare public release readiness criteria, including license selection, contribution expectations for multi-contributor projects, examples, and evidence requirements.

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

Not planned during the convention-first phase: runtime services, databases, storage layers, orchestration frameworks, package-manager dependencies, web applications, SDKs, or provider adapters.

## Still Human-Decided

A restrictive all-rights-reserved notice exists for incubation protection. Do not replace it with an open-source license, license headers, or broader reuse permission without explicit human approval.

The maintainer intends to choose an open license before broad public reuse, but no license or date has been selected.
