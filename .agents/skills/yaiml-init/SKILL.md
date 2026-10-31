---
name: yaiml-init
description: Establish or refresh YAIML project context and local skills from one pasted prompt or skill invocation.
metadata:
  yaiml-revision: "0.43.65c0797e642cbbde"
---

Read and follow the canonical [yaiml-init](../../../reference/skills/yaiml-init/SKILL.md) skill. Pass the user’s count, perspectives, scope and other arguments unchanged. Resolve that skill’s references from its own directory. Reuse current task context; this entry does not launch a worker. Report missing access without inventing guidance.
