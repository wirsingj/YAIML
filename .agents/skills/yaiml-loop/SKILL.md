---
name: yaiml-loop
description: Execute a requested sequence of skills repeatedly, preserving order, arguments, progress and stopping conditions.
metadata:
  yaiml-revision: "0.60.2ecf23cf990c1aec"
---

Read and follow the canonical [yaiml-loop](../../../reference/skills/yaiml-loop/SKILL.md) skill. Pass the user's sequence, counts, scope and other arguments unchanged. Resolve that skill's references from its own directory. Reuse current task context; this entry does not launch a worker. Report missing access without inventing guidance.
