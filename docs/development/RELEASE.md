---
yaiml-revision: "0.56.7665a059b603a2d9"
role: release-identity
title: YAIML Release
purpose: Identify YAIML's product release and source-maintainer publication readiness.
not-here: Target-project release procedures or portable method instructions.
durability: Current release identity; prior published content remains in Git and release tags.
agent-guidance: Source-only planning; never retrieved or installed by consumer init. Consumer identity belongs in reference bootstrap metadata.
---
# YAIML Release

This document belongs to the YAIML source project. Adopters record only applied YAIML release/status and source revision in their own Maintainer Guide; their release plans remain project-owned.

Product release: **0.6.0**. Status: **experimental**. Previous published guidance: **0.5.2**. Revision major: **0**. Discovery layout remains **0.2.0**.

The 0.5.2 baseline separated reusable `reference/` material from this project's `.yaiml/` memory. Both init forms exclude completed source artifacts. The current package provides one retained-record workflow: consolidate during normal work with established sole ownership, defer during overlap, and prepare changes for review through the existing Git method. It supplies twelve methods plus one compatibility alias and the change-record guide. No adopter mode switch, hook or runtime is introduced. Default acquisition targets `refs/tags/latest`; local review preparation does not establish publication. A version label alone proves no reliability.

Networked acquisition requires exact tag `refs/tags/latest`, peeled once to a commit for all `reference/` resources. The tag is a moving public-ready pointer, not an immutable content identity. A same-named branch is never a substitute. Consumer product identity lives in `reference/BOOTSTRAP.md`; this planning document is not retrieved. Existing layouts, local adaptations, retained records and earlier grants survive upgrade. Prior trials remain attributed to their tested revisions; the new layout requires fresh acceptance.


Release numbers identify product guidance independently of the moving `latest` tag. Before 1.0, use a minor increment for a material convention change and a patch increment for a correction; numbered release tags, when created, remain immutable. A project-memory-only change does not require a product release. Record the exact applied source commit and local adaptations in the adopter's Maintainer Guide.

The 1.0 claim remains pending: stable core and revision expectations, checked legacy/custom upgrades, repeated fresh-session ordinary maintenance and concurrent reconciliation, evidence from another host and independent adopters. Current maintainer-run trials do not satisfy all of these conditions. Revision tracking is guidance performed by agents and people, with no runtime enforcement.

## Publication Boundary

The maintainer selected 0.6.0 for this revision batch: `yaiml-diagram` and portable draw.io notes, clearer file-based memory explanations, and tightened offline setup. Offline init connects existing supported instruction routes and checks real setup decisions without inventing a demonstration decision or launching another agent. Full setup follows the acquired catalog; self-contained setup still installs no skill package. Record semantics, local revision major and discovery layout are unchanged; this label does not require a target-project version bump or memory migration.

The maintainer's 1:1 workflow batches work on revision-cycle branches rather than one branch per feature. Roughly two weeks is a working rhythm, not a deadline. Test and review the batch before merging; choose any product-version bump deliberately, not from the branch name or elapsed time. `main` is stable development. Merging to main is the public-ready decision: [.github/workflows/latest.yml](../../.github/workflows/latest.yml) advances `refs/tags/latest` on main updates. No GitHub Release object is required. Only `latest` moves; numbered tags remain fixed.

The workflow serializes its runs, reads live main rather than an older event commit, and creates or updates only the latest tag with job-scoped contents-write permission. It uses no checkout or third-party action. Repository rules or token restrictions can block it; report failure instead of bypassing protections. This is source maintenance, never an adopter dependency or copied release procedure.

On 2026-10-31, [PR #5](https://github.com/wirsingj/YAIML/pull/5) merged this batch at `02735018d0248cede9437bf86e236d1a72553592` before the numeric-label approval arrived. The [latest workflow](https://github.com/wirsingj/YAIML/actions/runs/41201044666) succeeded; all 41 public README/license/reference files matched their Git blobs at that commit. The 0.6.0 label is a follow-up to that verified publication, not evidence of new agent behavior. [Review evidence](../evaluation/COLD_START_REVIEW.md#revision-batch-audit) retains the tested scope and earlier baselines. Fresh-session setup/upgrade acceptance and broader-host evidence remain pending.
