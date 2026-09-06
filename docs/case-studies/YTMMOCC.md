---
yaiml: 0.2
kind: case-study
title: YTMMOCC Case Study
purpose: Record a real maintainer-owned YAIML adoption case without overstating independent evidence.
belongs-here: inspected repository evidence, human-reported experience, public listing observations, limitations, lessons for YAIML.
not-here: fabricated productivity metrics, private transcripts, complete YTMMOCC project memory, store credentials, raw diagnostic logs.
durability: evidence note; update when the case is reinspected or new public evidence changes the conclusions.
read-with: Evaluation And Case Studies; SoTY.
update-when: YTMMOCC evidence is reinspected, public listing status changes, or YAIML evaluation standards change.
agent-guidance: Distinguish observed repository facts, human reports, public listing evidence, inference, and unknown outcomes.
---

# YTMMOCC Case Study

## Project And Evidence Scope

Project: [YTMMOCC](https://github.com/wirsingj/ytmmocaptions), a Chrome/Firefox WebExtension that turns YouTube captions and transcripts into an MMO-style dialogue panel.

Public source baseline: [commit `1c197351892262793d35eb55d8fb1a3cbe6e3cf1`](https://github.com/wirsingj/ytmmocaptions/commit/1c197351892262793d35eb55d8fb1a3cbe6e3cf1), independently accessible on GitHub and advertised as remote HEAD when rechecked on 2026-09-05. The source claims below were reinspected at this revision using read-only Git object access; file links are pinned to it.

Inspection date: 2026-09-05.

Earlier local inspection: commit `51e379a39c4f133db49b29768cad6cec12e3eebf` on `codex/sot-next-audit-pass`, with uncommitted `README.md`, `yaiml.yml`, and `AI_USAGE.md`. That later snapshot was not publicly reproducible during review. It is context only, not the source baseline below; its additional reading-glow, launcher, and diagnostic changes are excluded from the public claims.

Verification scope: source and document inspection only. No extension tests, builds, browser diagnostics, or store uploads were executed for this case. Assertions described below are defined checks, not passing-run evidence. Historical results in project memory remain attributed historical reports.

Public listing evidence checked on 2026-09-05:

- [Chrome Web Store listing](https://chromewebstore.google.com/detail/ytmmocc/cocgdaogbkknnhdpmojlmodalmblndgf): accessible listing named YTMMOCC, showing version `1.1.4`, updated June 1, 2026, 4 users, and 1 rating.
- [Firefox Add-ons listing](https://addons.mozilla.org/en-GB/firefox/addon/dialogue-captions/): accessible listing named YTMMOCC, showing version `1.1.6`, last updated July 23, 2026, 1 user, and 1 review.

Human report: the maintainer reports that YTMMOCC is published in both Chrome and Firefox stores. The public listings above independently confirm accessible store listings, but the Chrome listing observed during this pass lagged the local repository version.

Measured outcomes: none recorded. This is maintainer-owned field evidence, not an independent controlled productivity study.

## YAIML Family Observed

The public [discovery file](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/yaiml.yml) uses a recognizable older YAIML layout (excerpt):

```yaml
yaiml: "0.2"
usage: loose-project-memory
documents:
  sot:
    path: STATE_OF_THE_UNION.md
  architecture:
    path: ARCHITECTURE.md
  maintainer:
    path: MAINTAINER_GUIDE.md
```

The map points to the three core documents and `docs/YAIML.md`. Its paths are inspectable; successful discovery by other consumers has not been tested here.

Lesson for YAIML: apply the [discovery migration policy](../ADOPTION_AND_UPGRADES.md#discovery-layout-compatibility), preserving this map during routine refreshes.

## Preserved Knowledge Traced To Evidence

YouTube-only release boundary:

- Observed repository fact: [manifest.json](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/manifest.json), [manifest.chrome.json](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/manifest.chrome.json), and [manifest.firefox.json](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/manifest.firefox.json) limit host permissions and content-script matches to `https://www.youtube.com/*`.
- Observed repository fact: [src/universal-captions.js](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/src/universal-captions.js) and [tests/universal-captions.test.js](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/tests/universal-captions.test.js) exist, while compliance tests assert that release manifests do not include `universal-captions.js`.
- YAIML value: [STATE_OF_THE_UNION.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/STATE_OF_THE_UNION.md), [ARCHITECTURE.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/ARCHITECTURE.md), and release checklist language preserve the distinction between broader caption support in source and the shipped YouTube-only release boundary.

Persisted preferences versus excluded transcript/video state:

- Observed repository fact: [PRIVACY.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/PRIVACY.md) and [ARCHITECTURE.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/ARCHITECTURE.md) state that local UI preferences can persist, while transcript text, active bubble, playback position, current timestamp, current video id, and viewing history should not.
- Source-inspected test definitions: [tests/settings-store.test.js](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/tests/settings-store.test.js) covers unlocked layout staying session-local, locked layout persistence, workspace preset snapshots, dropping transient video state, and last-writer behavior for overlapping global settings.
- YAIML value: the project memory keeps storage rules visible as product and privacy constraints, not just implementation detail.

Experimental functionality kept separate from shipped behavior:

- Observed repository fact: [README.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/README.md) says Timeline Scrub remains experimental and hidden from normal release UI.
- Source-inspected implementation and assertions: [src/ui-panel.js](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/src/ui-panel.js) contains `TIMELINE_MODE_EXPERIMENT_ENABLED = false`, while [tests/compliance.test.js](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/tests/compliance.test.js) asserts that Timeline Scrub stays optional and hidden.
- Intended memory benefit: keep experimental code distinct from approved release behavior; prevention of future mistakes was not measured.

Caption fallback decisions, regressions, and verification limits:

- Observed repository fact: [src/transcript.js](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/src/transcript.js) implements multiple YouTube acquisition paths, and [test definitions](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/tests/transcript.test.js) assert behavior for generated preferred-language timedtext candidates, rejection of language-opaque original-language fallbacks after preferred translation misses, stale player data, and stale DOM transcript entries.
- Observed memory evidence: [STATE_OF_THE_UNION.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/STATE_OF_THE_UNION.md) records language-fallback and launcher changes, historical check results, and limits of optional diagnostics. Those reports were not rerun here.
- YAIML value: regressions and verification limits are preserved as current engineering caution rather than raw session diary.

Release procedures and store boundaries:

- Observed repository fact: [package.json](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/package.json) defines `npm test`, `npm run build`, `npm run release:check`, and `npm run release:sanity`.
- Observed repository fact: [RELEASE.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/RELEASE.md) describes numbered GitHub workflows for preparing a release and publishing to Firefox and Chrome behind a `store-publish` environment.
- Source-inspected test definitions: [tests/compliance.test.js](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/tests/compliance.test.js) checks release automation structure, store publish scripts, release sanity behavior, and packaging boundaries.
- YAIML value: the [Maintainer Guide](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/MAINTAINER_GUIDE.md) gives future sessions a concise release map while release details remain in [RELEASE.md](https://github.com/wirsingj/ytmmocaptions/blob/1c197351892262793d35eb55d8fb1a3cbe6e3cf1/RELEASE.md).

## What This Case Shows

This case supports modest claims:

- A mature, real project can carry useful YAIML-shaped memory without YAIML becoming a build input, release gate, schema, package, or runtime dependency.
- YAIML can preserve easily lost product constraints that source code alone may not communicate, especially release scope, storage boundaries, experimental features, and verification limits.
- Older discovery layouts can remain understandable when they point clearly to SoT, Architecture, and Maintainer Guide roles.

This case does not prove:

- broad adoption;
- productivity gains;
- causality between YAIML and successful release work;
- independent maintainer value;
- compatibility across all agents or tools.

## Follow-Up Evaluation Path

A stronger trial would compare fresh sessions on bounded YTMMOCC tasks with and without YAIML context, using documented baselines and the evaluation dimensions in [evaluation guidance](../EVALUATION.md). Useful tasks would include:

- deciding whether to promote generic captions into manifests;
- modifying preference persistence without storing transcript or video state;
- touching Timeline Scrub without accidentally shipping it;
- reviewing a caption fallback bug while preserving verification limits.

Record failures and neutral results alongside successes.
