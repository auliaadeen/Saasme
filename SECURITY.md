# Security Policy

## Scope

Security is a first-class requirement for Lab. This policy applies to application source code and documented infrastructure.

## Never commit secrets

Do not commit API keys, Supabase service-role credentials, database passwords, OAuth secrets, deployment tokens, private keys/certificates, production .env files, or confidential user-uploaded learning content.

Only safe placeholders may appear in .env.example.

## Secret handling

- Server-side secrets must remain server-side.
- Public environment variables must contain only intentionally public values.
- Supabase service-role credentials must never reach client-side code.
- Validate and authorize every server-side operation.
- Do not log prompts, uploaded documents, tokens, credentials, or sensitive user content unnecessarily.

## Application security requirements

1. Authentication and authorization.
2. Project-level data isolation.
3. Server-side input validation.
4. Zod validation for AI-generated structured data.
5. File type and file size validation.
6. Safe document parsing.
7. Rate limiting for AI and upload endpoints.
8. Output encoding/sanitization for rendered user content.
9. Secure HTTP headers.
10. Least-privilege database access and Row Level Security.
11. Dependency and secret scanning in CI.

## AI-specific security

AI output is untrusted input. Never execute model-generated code or treat model output as trusted HTML, SQL, shell commands, or application logic. Uploaded content must be treated as untrusted data, including embedded instructions intended to manipulate the model.

## Reporting

Report suspected security vulnerabilities privately through GitHub's private security reporting mechanism when available. Do not publish exploit details in a public issue.
