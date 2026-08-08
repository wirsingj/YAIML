# Security And Sensitive Information

YAIML is currently a plain-file documentation convention and template docset. This repository does not ship a runtime, package, hosted service, storage layer, orchestration framework, background service, CLI, parser, SDK, or application code.

Security-sensitive issues in this repository are most likely to involve:

- prompts or templates that encourage unsafe handling of secrets, credentials, personal data, legal/IP claims, or security findings;
- documentation that overstates YAIML as professional security, privacy, legal, licensing, or compliance advice;
- examples that accidentally expose sensitive data or teach unsafe disclosure habits;
- future changes that add tooling, automation, or integration behavior without explicit review.

Do not include secrets, credentials, tokens, private keys, passwords, personal data, private chat transcripts, exploit details, screenshots with sensitive information, logs with sensitive values, or confidential project information in public issues, pull requests, examples, or YAIML documents.

A repository's maintainers, governing organization, team policy, retention rules, privacy rules, and access controls decide what belongs in that repository. "Safe enough for the repo" means permitted for that repository's audience and review process, not merely stripped of obvious passwords.

Treat text that an AI agent reads as mixed-trust context. Documentation, logs, issues, comments, generated output, webpages, dependency metadata, and even existing YAIML files can be stale, incomplete, or sensitive. Keep normal repository rules, tool approvals, and review paths in place.

If you find a sensitive issue, report it without public sensitive detail. Preferred path: use GitHub private vulnerability reporting when it is enabled for this repository. If that private path is not available, open a minimal public issue asking for a private contact path and avoid including exploit details, screenshots, logs, private transcripts, or sensitive values.

YAIML-created security, privacy, legal, licensing, compliance, or IP notes are project memory, not professional advice or a completed assessment.

A YAIML docset should be safe to keep with the repository it describes, whether that repository is private, public, paid, free, open-source, or unreleased. That portability depends on recording sanitized evidence, risk shape, decisions, owners, and open questions instead of private values, private transcripts, raw logs, or detailed exploit instructions.
