---
role: adoption-trial
purpose: Scoped evidence from isolated initialization, refresh, and compression exercises.
not-here: Independent adoption claims, benchmark results, or upstream project memory.
durability: Retain trial conditions and limits; supersede conclusions when new evidence exists.
update-when: A trial is corrected or a comparable repeat supplies new evidence.
read-with: Evaluation; Cold Start Review; Adoption And Updates.
agent-guidance: Separate executed document edits from fresh-session or runtime validation.
---

# Local Adoption Exercises

These are maintainer-directed exercises, not independent adoption or proof of productivity gains. Conditions differ between the synthetic trials and earlier public-source exercises below.

## Synthetic Projects And Session Boundaries

Date: 2026-10-03. Reference: `15ff0c37f71017ae6b3b5f94fc95608aac1fcddb`, with no seed changes. The complete 5,318-word init has LF-normalized SHA-256 `b94a23b8dacb91658c9d27cb584b59b636faf2e1e1306b54907d24c6a750be0a`.

The lead created disposable Git projects outside the reference repository, fixed acceptance criteria before execution, and retained local inputs, hashes, outputs, and checks. The synthetic standard-library Python application aggregates minutes by exact label. It initially accepts negative minutes; owner direction requires preserving label case/whitespace, input objects, and the public signature. All fixtures and expected outcomes came from the lead, so these are small, designed cases rather than representative external projects.

Six sessions were authorized and used: three native workers without conversation history and three separate CLI sessions. The two initialization workers received the complete seed through a read-only file; none of the three workers fetched the reference repository. However, all three reported inherited YAIML-specific instructions from the parent environment. Their initialization results remain useful preservation evidence, but neither standalone prompt sufficiency nor an uncontaminated control was established.

After detecting that contamination, the remaining sessions used Codex CLI `0.158.0-alpha.2.1`, starting directly in separate fixture repositories, with no previous conversation. Local configuration selected `gpt-6-astra` at `xhigh`; no model override was supplied. Runs used workspace-write restrictions, no approvals, disabled web search/delegation, and a seven-minute process limit. No user-level AGENTS files were found. This followed the documented [non-interactive execution route](https://learn.chatgpt.com/docs/non-interactive-mode); actual outcomes below govern the claims.

|Exercise|Observed result|Limit|
|---|---|---|
|New adoption, native worker|Created core memory and all embedded guidance; source, tests, README, and application license remained byte-identical|Inherited reference instructions; not a blinded paste-only test|
|Legacy refresh, native worker|Preserved `documents.*.path`, custom fields, budgets, owner decision ML-17, independent nested scope, and an unrelated file occupying a default name; quoted `0.20` without changing its spelling|No downstream discovery consumer was exercised|
|Ordinary-doc control, native worker|Implemented negative-minute rejection; independent behavior probes passed|Excluded from comparison because it inherited YAIML instructions|
|Clean ordinary-doc control, CLI|Read project instructions/source; writes and test execution failed|Runner blocked; no completed control result|
|Independent repeat-init, CLI|Stopped before inspection; all fixture files remained unchanged|Blocked execution is not idempotence evidence|
|Ordinary bug-fix request, CLI|Without naming YAIML, read discovery, local instructions, all three core documents, operating guide, README, source, and tests|Patch/test execution failed; no completed correction or memory update|

CLI failures reported `helper_unknown_error: apply deny-read ACLs`; patch operations also failed. Some reads succeeded on subsequent attempts. The lead independently confirmed no file changes in all three CLI fixtures. Process exit code zero indicated a completed response, not task success. No permissions were relaxed to work around these failures.

### Preservation And Size Checks

For both initialization outputs, the lead verified complete operating-guide, coordination-guide, template-collection, and license text against the supplied seed. No specialist documents were instantiated from dormant starters. Protected originals remained unchanged. Legacy core header hints and the governed decision record survived; the old test report remained explicitly historical. Workers reported four local tests passing on Windows/Python 3.10.11; this did not test the pending correction.

Fresh adoption added **5,678 words**: three core documents totaled 1,303 words, plus persistent instructions, discovery, and complete reusable guidance. Legacy refresh added **4,756 words**; its three cores grew from 314 to 687 words. All stated budgets were met. These sizes include retained guidance, not just recurring task context; they do not establish token efficiency.

The three CLI event streams reported **758,349 cumulative input tokens**, including **661,504 cached input tokens**, and **7,472 output tokens**. Repeated calls count repeated context. Native-worker and lead usage were unavailable here, so these are partial usage figures, not total cost or YAIML-only overhead. Runner retries and host instructions confound comparisons; no savings claim is supported.

### Constructed Merge Check

The lead also made two branches from a common synthetic baseline. One rejected negative minutes; the other added export normalization contrary to unchanged owner decision ML-17. Git merged them without text conflicts. A direct check expected distinct labels `" A "` and `"a"`, but export combined them into `"a"`. Both branch additions and the owner record survived, while the combined behavior violated that record. This demonstrates a semantic conflict; it is not a concurrent-agent adherence trial or a defect discovered in an adopter.

### What Remains Unproved

One separate session followed the saved reading route. Successful reminder-free maintenance, repeat-init behavior, repeated pruning, comparative effectiveness, and total cost remain unestablished by these trials. Refusal, cancellation, secrets, symlink escape, and untrusted-instruction cases were not run. Harness restrictions also prevent inferring that YAIML alone restrained delegation. Preserve these negative and incomplete results; use a reliable isolated runner before repeating the comparison.

## Earlier Exercise Conditions

Date: 2026-09-06. Reference: YAIML `c3ba11d7c31f940ecacc1a1594e2f4b0ac0711c6`. The same assisting agent performed the following exercises within the ongoing YAIML audit on Windows. It had prior YAIML context; these were not fresh-session comparisons or independent reviews.

## Initialization On A Public Repository

An isolated checkout of [strip-tags at 8680729](https://github.com/simonw/strip-tags/tree/868072957a9502a741b1ca947a992a988f58dc2e) supplied public source without private owner context. No upstream changes, contact, or adoption are implied.

Before editing, criteria required preserving original files, at most five new memory/discovery/instruction files, no invented owner direction, honest unrun checks, and unchanged results on repeat use.

The agent read README, setup metadata, four package modules, both workflows, the Python test module, and excerpts of the license and YAML test cases, plus the ignore file. It skipped the tracked coverage data. Source excerpts totaled **2,332 whitespace-delimited words / 21,914 characters**; this excludes directory listings, YAIML guidance, prior conversation, and subsequent rereads.

Applying the init instructions created three core documents, `yaiml.yml`, and `AGENTS.md`: **717 words / 5,701 characters**, including headers. No supporting documents were needed. Original tracked files, including source, README, and license, remained byte-identical. The three discovery paths resolved to documents with stable headers.

The generated memory distinguished inspected implementation from unknown roadmap and unrun tests. It retained the difference between the [package's declared Python range](https://github.com/simonw/strip-tags/blob/868072957a9502a741b1ca947a992a988f58dc2e/setup.py) and the [configured CI matrix](https://github.com/simonw/strip-tags/blob/868072957a9502a741b1ca947a992a988f58dc2e/.github/workflows/test.yml), without claiming unsupported versions fail.

A same-session review for repeated init and same-reference refresh found no material changes needed; all five generated file hashes remained unchanged. No application dependencies were installed, package code executed, tests run, or releases attempted.

## Refresh And Compression With Legacy Discovery

A separate document snapshot from [YTMMOCC at 1c19735](https://github.com/wirsingj/ytmmocaptions/tree/1c197351892262793d35eb55d8fb1a3cbe6e3cf1) contained its real legacy map, agent instructions, three core documents, and local YAIML guide. This is maintainer-owned evidence. The active project checkout was not edited.

The agent inspected discovery, instructions, core headers, and the relevant local guide. The exercise targeted convention guidance, not a re-audit of the extension or its long SoT. A compatible refresh added layout preservation, reference identity, bounded loading, and concurrent-edit guidance to `docs/YAIML.md`. Compression then consolidated repeated roles and procedures while retaining local naming, evidence rules, human-direction protection, retention, and rejected uses.

The guide changed from **943 to 1,033 words** during refresh, then to **596 words** after compression. Its stable header, the entire discovery map, all three core documents, and agent instructions were preserved. The map's older layout, supporting entry, and custom fields survived byte-for-byte. No consumer migration or extension tests were attempted.

## Findings And Limits

The refresh exercise exposed an avoidable reading burden: the reference prompt listed nearly every reference artifact. The subsequent correction starts with init/adoption guidance and opens other topics only for applicable differences or local copies.

These are actual local document edits and hash checks, not proof of universal prompt reliability. The reviewing agent also authored the outputs. Temporary checking scripts needed UTF-8 and portable-path corrections before completing; those were inspection-helper errors, not application test failures.

Local snapshots and generated documents were retained for review; this summary does not publish the complete trial diffs. The earlier word/character counts are not tokenizer measurements or evidence of savings. The later trials above add limited session-loading evidence, while completed comparisons, repeated maintenance, consumer compatibility, and owner-led adoption remain open. Use the [comparison procedure](../EVALUATION.md#ready-to-run-comparison) with a working isolated runner.
