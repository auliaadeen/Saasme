# Implementation Plan — Lab MVP Core

## Architecture
Modular monolith using Next.js + TypeScript. Supabase provides Auth, PostgreSQL, Storage, and Row Level Security. OpenAI is accessed only through a server-side provider abstraction. Zod validates every AI-generated domain object. React renders interactive learning from canonical structured data.

## Stack
- Next.js + TypeScript
- Tailwind CSS + shadcn/ui
- Supabase Auth/PostgreSQL/Storage
- OpenAI provider abstraction
- Zod
- Vitest + Playwright
- EdgeOne initial deployment

## Security design
- Server-only secrets
- Supabase RLS for all user-owned tables
- Explicit authorization checks in server actions/routes
- Upload allowlist, size limits, parser isolation, and storage access controls
- Sanitized rendering of user-generated content
- Rate limiting for AI and upload operations
- Security headers and secure cookie configuration
- Dependency and secret scanning in CI

## Domain model
User → Project → Course → Learning Objectives / Learning Objects → Versions / QA Results / Exports.

## AI boundary
Source document → parser → AI structured output → Zod validation → canonical learning model → database → deterministic renderer.

## Testing strategy
Unit-test schemas/domain logic, integration-test AI parsing and persistence boundaries with mocks, and E2E-test the critical flow: create project → import → generate → edit → preview → QA → publish.
