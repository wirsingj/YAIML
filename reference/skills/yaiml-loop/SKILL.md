---
name: yaiml-loop
description: Execute a requested sequence of skills repeatedly, preserving order, arguments, progress and stopping conditions.
metadata:
  yaiml-revision: "0.60.2ecf23cf990c1aec"
---

# yaiml-loop

Use this method when the user requests repeated skills or repeated groups of steps. Follow the [shared guide](../../YAIML_GUIDE.md), reusing current context. Carry out the sequence in the active task; this method adds no scheduler, background worker or execution runtime. Discussing or authoring a loop does not execute its example.

## Resolve The Sequence

Translate the request into a finite ordered sequence with positive repetition counts, preserving each skill's arguments and scope. Accept natural language and nested groups; native invocation syntax depends on the host. State the interpreted sequence briefly and begin without requiring approval for already authorized work. Clarify only ambiguity that changes the work or unusable counts that context cannot resolve. Do not infer an unbounded loop or invent a missing outer count.

For example:

```text
yaiml-loop: repeat 10 times:
  yaiml-audit
  repeat 2 times:
    yaiml-to-do
```

This requests ten cycles, each audit followed by two separate to-do invocations: ten audits and twenty to-do invocations if completed. Each to-do without an argument selects the next feasible priority. Repeating `yaiml-to-do 2` twice instead requests two invocations of up to two priorities each. Invocation counts are not completed-item counts. Nested groups finish in order before the enclosing sequence advances.

Resolve the named methods through available metadata or the local catalog and read their canonical instructions before their first use. Confirm required resources are available; never substitute an imagined method or download missing methods merely to satisfy the sequence. Report an unavailable step and its impact; independent authorized preparation may continue.

## Execute And Account

Keep a compact task-local progress account: requested sequence/counts, current cycle and nested step, completed/partial/blocked/skipped outcomes, evidence references and next action. Use the host's task state or an existing permitted working-note location; do not create another project backlog or put a transcript in current memory.

Run steps sequentially. Each invocation uses the current project state and preceding findings, retaining uncertainty and approved priority ordering. Audit findings inform to-do selection without automatically becoming approved work. Preserve every method's verification, maintenance and authority requirements. A child method finishing ends that invocation, not the remaining loop. Do not collapse repeated invocations into a larger batch or launch workers unless the user requests that change.

Complete required checks and material maintenance at the child's normal boundaries so the next step sees current understanding. Reuse loaded guidance; do not create records for no-op calls or duplicate a completed child iteration solely to log a cycle. Advance progress only after the actual outcome is known. Report meaningful progress concisely, including cycle position, rather than narrating every file read.

## Stop And Resume Honestly

Continue to the requested count unless cancelled, the authorized objective is exhausted, a necessary decision/access limit blocks the sequence, or a whole cycle produces no useful work or new evidence with no changed conditions to justify another. A repeated-observation request may intentionally seek unchanged results; respect that purpose. Never manufacture priorities, changes or findings to fill repetitions.

Use the active method's bounded repair rules for failures; no endless retry. Default to pausing the sequence on an unresolved failed or partial step rather than claiming a completed cycle. Independent work may continue within scope, but skipping or reordering required steps needs the user's instruction. Existing approval requirements still apply; repetition grants no new publication, destructive-action or delegation authority.

After interruption or context loss, recover the progress account and inspect actual artifacts, checks and pending memory before resuming the first unfinished step. Do not blindly replay completed mutations. If completion cannot be established, report the uncertainty and resolve it before dependent action; a counter alone is not proof. Host limits may prevent continuation: leave an accurate continuation point, never promise unattended execution.

Finish with completed cycles versus requested, any partial cycle and step outcomes, actual work/checks, stop reason and exact next step when unfinished. Distinguish all requested steps completed from early exhaustion or blockage. Persist material project understanding through its existing owners; routine loop bookkeeping alone is not durable project knowledge.
