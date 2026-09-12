# Security Baseline

## Threat model priorities
1. Secret leakage
2. Cross-user/project data access
3. Malicious document uploads
4. Prompt injection through uploaded learning content
5. Stored XSS through generated/user-authored content
6. AI endpoint abuse and cost exhaustion
7. Dependency/supply-chain vulnerabilities
8. Sensitive data leakage through logs or public course URLs

## Required controls before production
- RLS policies tested for every user-owned table
- Server-side authorization checks
- File MIME/extension/size allowlists
- Sandboxed or hardened document parsing
- HTML/content sanitization where rendering requires it
- AI output schema validation
- Rate limits and request budgets
- Secure headers
- Dependency audit
- Secret scanning
- Error messages that do not expose stack traces, prompts, tokens, or provider internals
- Public publishing must expose only explicitly published course data

## Security rule
Treat documents, prompts, generated text, URLs, and model output as untrusted input.
