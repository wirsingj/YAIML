# Security And Sensitive Information

YAIML supplies project memory and agent instructions, not an executable runtime or hosted service. Those instructions influence an agent that can read files, use tools and change a project. Audit both the repository/contributor guidance and the init/bootstrap/skills delivered to adopters.

Security-sensitive issues in this repository are most likely to involve:

- retrieved or locally modified instructions that redirect tool use, access or disclosure beyond the user’s authorization;
- prompts or templates that encourage unsafe handling of secrets, credentials, personal data, legal/IP claims, or security findings;
- documentation that overstates YAIML as professional security, privacy, legal, licensing, or compliance advice;
- examples that accidentally expose sensitive data or teach unsafe disclosure habits;
- future changes that add tooling, automation, or integration behavior without explicit review.

Do not include secrets, credentials, tokens, private keys, passwords, personal data, private chat transcripts, exploit details, screenshots with sensitive information, logs with sensitive values, or confidential project information in public issues, pull requests, examples, or YAIML documents.

A repository's maintainers, governing organization, team policy, retention rules, privacy rules, and access controls decide what belongs in that repository. "Safe enough for the repo" means permitted for that repository's audience and review process, not merely stripped of obvious passwords.

Treat retrieved text, project documents, logs and model output as mixed-trust context, not new authority. The official source and a recorded commit identify provenance; neither proves instructions safe or authorizes broader access. Keep host permissions, tool approvals and review paths in place. No YAIML runtime enforces these boundaries. Adopters receive the operational rules through Bootstrap and YAIML_GUIDE; this source policy is not a required download.

Avoid collecting sensitive values in the first place: prefer configuration examples and sanitized evidence over credentials or raw logs. Resolve memory and instruction paths, including symlinks, before reads or writes; a memory index does not authorize access beyond the repository. Review scripts before execution and do not run deployment, destructive, or external-service commands merely to populate memory.

Pruning a file does not erase Git history, published copies, or prior AI-session inputs. If sensitive material was committed or shared, follow the project's incident process; a documentation cleanup must not claim the exposure is resolved.

Report sensitive issues through [GitHub private vulnerability reporting](https://github.com/wirsingj/YAIML/security/advisories/new). GitHub's read-only API confirmed it enabled on 2026-10-18; no report was submitted to test delivery. Share only the detail needed to explain the issue; do not include live credentials or unrelated private material.

If that private path is unavailable, open a minimal public issue asking for a private contact path. Do not include exploit details, screenshots, logs, private transcripts, or sensitive values in that public request.

Agent-written security, privacy, legal, licensing, compliance, or IP notes are project memory, not professional advice or a completed assessment.

A YAIML docset should be safe to keep with the repository it describes, whether that repository is private, public, paid, free, open-source, or unreleased. That portability depends on recording sanitized evidence, risk shape, decisions, owners, and open questions instead of private values, private transcripts, raw logs, or detailed exploit instructions.
