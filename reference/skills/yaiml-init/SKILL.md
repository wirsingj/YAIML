---
name: yaiml-init
description: Establish or refresh YAIML project context and local skills from one pasted prompt or skill invocation.
metadata:
  yaiml-revision: "0.43.65c0797e642cbbde"
---
# YAIML Init

Run bootstrap now in the target project. One invocation obtains reusable guidance, creates useful project memory and connects supported instruction/skill routes for later work. Follow target instructions and preserve existing work; do not stop at saving this prompt.

1. Use https://github.com/wirsingj/YAIML by default. Resolve the exact tag ref `refs/tags/latest`, peel it to its commit once, and use that commit for every resource in this acquisition. `latest` is the moving public-ready tag; record the resolved commit, not just the tag name. A branch with the same short name is not that tag. If the tag is absent or cannot be distinguished from a branch, report incomplete setup; never substitute a branch, `main`, or another release. Use a local checkout, snapshot, fork or different ref only on explicit user request. For an ambiguous requested ref, resolve its namespace before proceeding. Identify requested snapshots and material uncommitted reference edits; never reset a dirty checkout. A recorded source note or nearby checkout is not a new source request.
2. Retrieve `reference/BOOTSTRAP.md` from that exact source and execute it. Acquire its listed project-agnostic guides, methods and templates, plus required notices. The upstream `.yaiml/` directory is not an input to adoption, directly or through links. Record the bootstrap's product identity and resolved source revision as provenance, not target-project history. If the reference layout or required access is unavailable, preserve working guidance and report the gap; do not fall back to source-project documents or invent missing content.
3. Populate target memory from the target's evidence and human direction. Reuse existing useful documents, local methods and established paths; otherwise use `.yaiml/`. Connect applicable existing agent instructions and supported native skill routes. Do not import completed source artifacts, example facts or source revision counters as project knowledge. Keep target release versions and policy independent from YAIML guidance versions and memory stamps.
4. Check the acquired resources without the source repository's project-memory tree present. Verify target-derived content, relevant supporting-document discovery and host routes. Report applied source, actual checks and unresolved gaps; configuration alone does not establish fresh-session behavior.

Ordinary work should now read and maintain local context without another YAIML prompt. Named skills remain optional. This setup creates no runtime, background task or automatic backlog execution, and grants no publication, destructive-action or delegation permission.
