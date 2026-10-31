---
yaiml-revision: "0.46.42a0394f3a2abb59"
role: release-identity
title: YAIML Release
purpose: Identify YAIML's product release and source-maintainer publication readiness.
not-here: Target-project release procedures or portable method instructions.
durability: Current release identity; prior published content remains in Git and release tags.
agent-guidance: Source-only planning; never retrieved or installed by consumer init. Consumer identity belongs in reference bootstrap metadata.
---
# YAIML Release

This document belongs to the YAIML source project. Adopters record only applied YAIML release/status and source revision in their own Maintainer Guide; their release plans remain project-owned.

Product release: **0.5.2**. Status: **experimental**. Previous published baseline: **0.4.0**. Revision major: **0**. Discovery layout remains **0.2.0**.

This release separates reusable `reference/` material from this project's `.yaiml/` memory. Both init forms exclude completed source artifacts. It provides one retained-record workflow: consolidate during normal work with established sole ownership, defer during overlap, and prepare changes for review through the existing Git method. It supplies eleven methods plus one compatibility alias and the change-record guide. No adopter mode switch, hook or runtime is introduced. Default acquisition targets `refs/tags/latest`; local review preparation does not establish public availability of that ref. This label alone proves no reliability.

Networked acquisition requires exact tag `refs/tags/latest`, peeled once to a commit for all `reference/` resources. The tag is a moving public-ready pointer, not an immutable content identity. A same-named branch is never a substitute. Consumer product identity lives in `reference/BOOTSTRAP.md`; this planning document is not retrieved. Existing layouts, local adaptations, retained records and earlier grants survive upgrade. Prior trials remain attributed to their tested revisions; the new layout requires fresh acceptance.


Release numbers identify product guidance independently of the moving `latest` tag. Before 1.0, use a minor increment for a material convention change and a patch increment for a correction; numbered release tags, when created, remain immutable. A project-memory-only change does not require a product release. Record the exact applied source commit and local adaptations in the adopter's Maintainer Guide.

The 1.0 claim remains pending: stable core and revision expectations, checked legacy/custom upgrades, repeated fresh-session ordinary maintenance and concurrent reconciliation, evidence from another host and independent adopters. Current maintainer-run trials do not satisfy all of these conditions. Revision tracking is guidance performed by agents and people, with no runtime enforcement.

## Publication Boundary

Feature work belongs on feature branches; optional release branches can collect reviewed changes. `main` is stable development. Under the maintainer's chosen workflow, merging to main is the public-ready decision: [.github/workflows/latest.yml](../.github/workflows/latest.yml) advances `refs/tags/latest` on main updates. No GitHub Release object is required. Only `latest` moves; numbered tags remain fixed.

The workflow serializes its runs, reads live main rather than an older event commit, and creates or updates only the latest tag with job-scoped contents-write permission. It uses no checkout or third-party action. Repository rules or token restrictions can block it; report failure instead of bypassing protections. This is source maintenance, never an adopter dependency or copied release procedure.

On 2026-10-31, authorized [PR #2](https://github.com/wirsingj/YAIML/pull/2) merged the complete local 0.5.2 work at `91c8307120215a499c4e7fd0801c0b5db70f98f5`. The [live workflow](https://github.com/wirsingj/YAIML/actions/runs/41175440712) succeeded and `refs/tags/latest` resolved to that commit. All 39 public README/license/reference files were retrieved at that exact source and matched their Git blob identities, including both init prompts. This verifies publication and resource availability, not fresh-session setup/upgrade acceptance. Those behavioral checks and broader-host evidence remain pending.