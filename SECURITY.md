# Security And Sensitive Information

YAIML is currently a plain-file documentation convention. This repository does not ship a runtime, package, hosted service, CLI, parser, SDK, or application code.

Security-sensitive issues in this repository are most likely to involve:

- prompts or templates that encourage unsafe handling of secrets, credentials, personal data, legal/IP claims, or security findings;
- documentation that overstates YAIML as professional security, privacy, legal, licensing, or compliance advice;
- examples that accidentally expose sensitive data or teach unsafe disclosure habits;
- future changes that add tooling, automation, or integration behavior without explicit review.

Do not include secrets, credentials, tokens, private keys, passwords, personal data, exploit details, or confidential project information in public issues, pull requests, examples, or YAIML documents.

If you find a sensitive issue, report it without public sensitive detail. Use a private maintainer contact or GitHub private vulnerability reporting if available. If no private channel is available, open a minimal public issue asking for a private contact path and avoid including exploit details or sensitive values.

YAIML-created security, privacy, legal, licensing, compliance, or IP notes are project memory, not professional advice or a completed assessment.
