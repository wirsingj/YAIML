---
yaiml-revision: "0.35.4b577caa77f80cc3"
role: release-identity
title: YAIML Release
purpose: Identify the reusable product guidance independently of adopter revisions and discovery layout.
durability: Current release identity; prior published content remains in Git and release tags.
agent-guidance: Use the resolved source commit for exact content; a label alone does not prove verification.
---
# YAIML Release

Product release candidate: **0.5.1**. Status: **experimental**. Previous published baseline: **0.4.0**. Revision major: **0**. Discovery layout remains **0.2.0**.

This candidate provides one retained-record workflow: consolidate during normal work with established sole ownership, defer during overlap, and prepare changes for review through the existing Git method. It supplies eleven methods plus one compatibility alias and the change-record guide. No mode switch, hook or runtime is introduced. Default acquisition targets `v0.5.1`; local review preparation does not establish public availability of that ref. This label alone proves no reliability.

This candidate pins upstream acquisition to reviewed release ref `v0.5.1` in the official GitHub repository, resolved once to an exact commit. Floating `main` requires an explicit testing request; unavailable pins fail without fallback. Document stamps identify content revisions, not alternative source pins. Local checkouts and other sources require explicit user requests; recorded provenance alone does not select an upstream. Init, refresh, growth and missing-guidance repair share that rule. Ordinary work uses installed local context offline. Upgrades preserve mature layouts, memory, records, earlier grants and local adaptations. The [evaluation gate](EVALUATION.md#post-review-cross-host-trial-gate-2026-10-24) separates the candidate's structural/manual checks from unrun fresh-session and cross-host trials; an adopter need not acquire that source-only evidence file. Previous tested revisions retain their attributed evidence in source history and review notes.


Release numbers identify published product guidance. Before 1.0, use a minor increment for a material convention change and a patch increment for a correction; never silently replace an existing release tag. A project-memory-only change does not require a product release. Record the exact applied source commit and local adaptations in the adopter's Maintainer Guide.

The 1.0 claim remains pending: stable core and revision expectations, checked legacy/custom upgrades, repeated fresh-session ordinary maintenance and concurrent reconciliation, evidence from another host and independent adopters. Current maintainer-run trials do not satisfy all of these conditions. Revision tracking is guidance performed by agents and people, with no runtime enforcement.

## Release Ref Preparation

Reserve `v0.5.1` for the checked 0.5.x hardening candidate. Cut the local ref against the complete reviewed commit, never an earlier commit missing the offline/pinning changes; do not replace an existing tag. Pushing the commit/tag or publishing a release requires maintainer approval. Until publication, public resolution is unverified and may fail. Record the exact applied commit in adopter provenance; no self-referential commit hash is embedded here.
