---
yaiml: 0.2
role: security
title: Security Memory
purpose: Project-specific security assumptions, trust boundaries, reviewed constraints, evidence notes, and active security risks.
belongs-here: human-reviewed security constraints, trust boundaries, threat assumptions, sensitive data categories, active security risks, open security questions.
not-here: professional security advice, raw secrets, exploit details, complete audit history, command reference.
durability: durable with active-risk pruning.
read-with: SoT; Architecture; Maintainer Guide.
update-when: trust boundaries, authentication, authorization, secrets, or data exposure change.
agent-guidance: Verify security claims against code, configuration, tests, or runtime evidence. Surface uncertainty. Do not present agent-written notes as professional security advice. Do not store raw secrets or exploit details that should not be broadly visible.
---

# Security Memory

This template is for project-specific security memory. It is not security advice or a professional assessment.

## Trust Boundaries

## Sensitive Data

Record categories, storage locations, handling rules, and risks. Do not record raw secrets, credentials, tokens, private keys, passwords, or customer personal data.

Use the repository's governing retention, privacy, and access-control rules. This document records the rules, evidence, owners, and open questions the project is allowed to keep; it does not decide what is safe to store.

## Authority And Review

- Security owner or review group:
- Last meaningful review:
- Higher-authority sources:
- Required review path for material changes:

## Authentication And Authorization

## Active Risks

## Known Divergence

## Verification Notes

## Open Security Questions
