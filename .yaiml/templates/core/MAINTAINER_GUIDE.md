---
yaiml-revision: "0.3.e5a6701538b64592"
yaiml: 0.2
role: maintainer
title: Maintainer Guide
purpose: Current procedures, commands, diagnostics, and failure playbooks.
belongs-here: setup, commands, tests, build/run flows, debugging paths, important files, operations, release, recovery.
not-here: Product intent, durable architecture, full history.
durability: current-only; remove dead commands and obsolete paths.
read-with: SoT; Architecture.
update-when: commands, setup, diagnostics, release, or recovery procedures change.
agent-guidance: Verify command claims when practical. Mark environment-dependent or unverified procedures.
---
# Maintainer Guide
Adapt headings; omit unused sections; keep procedures actionable/current.
## Setup And Commands
Shortest checkout-to-work path, tools, assumptions. Separate executed/defined commands and unverified procedures. Retain consequential command, outcome, date, revision, environment; existence is not a pass.
## Focused Checks And Diagnostics
Test/build/lint/diagnostic procedures and interpretation; service/hardware/account/credential requirements without sensitive values. Retain sanitized outcomes, not logs. Name consequential invariants, independent expectation sources, comparison conditions, evidence gaps; matching outputs alone do not establish intent.
## Important And Dangerous Files
Editing boundaries and important files; no complete inventory.
## Failure, Release, And Recovery Procedures
Recurring symptoms, likely owners, evidence, recovery. Relevant release, rollback, backup/restore procedures and verification limits.
## YAIML Maintenance
Record project-specific setup: memory/discovery locations, shared-guide route, current product release and exact source revision, local skills/adaptations, partial-update exceptions, host activation evidence and gaps. Keep private reference locations in workspace configuration.
Point to the acquired YAIML_GUIDE.md for ordinary context/evidence/maintenance rules and VERSIONING.md for revision procedures; do not copy those generic rules into project memory. Identify the audit owner and any project-specific retention, authority or coordination constraints. Keep current source notes concise; changes.md owns the audit.
