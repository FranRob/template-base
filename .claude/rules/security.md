---
description: Security baseline rules — always active
---

## General

- Never log secrets, tokens, passwords, or PII
- Never hardcode credentials — always use environment variables
- Validate and sanitize all user input at system boundaries
- Never trust client-supplied IDs for authorization — verify server-side

## Multi-tenancy (if applicable)

- Every query MUST be scoped to the authenticated tenant/user
- Never query across tenants, even for admin operations unless explicitly designed for it

## Dependencies

- Never add a dependency without checking it has recent maintenance and no critical CVEs
- Prefer well-known packages over unknown ones with similar functionality
