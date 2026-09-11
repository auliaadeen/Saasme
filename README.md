# Lab — From Storyboard to Interactive Learning

> AI-assisted authoring and QA for interactive learning content.

**Status:** Product specification / architecture phase — implementation has not started.

Lab is a SaaS concept that transforms learning storyboards and source material into structured, editable, interactive learning experiences.

## Product flow

Storyboard / DOCX / PDF → AI Analysis → Learning Structure → Interactive Editor → Preview → AI + Content QA → Publish

## MVP

- Storyboard input via paste, DOCX, and PDF
- Structured learning-object model
- AI-assisted interaction suggestions
- Editable interactive content
- Multiple choice, true/false, drag & drop, and scenario interactions
- Desktop/mobile preview
- Content, interaction, and learning-objective QA
- Publish as a web-based interactive course

H5P and SCORM export are intentionally planned for a later phase. The Lab domain model remains provider-independent.

## Engineering principles

- Specification before implementation
- Structured, validated learning data
- AI is assistive, not authoritative
- Deterministic rendering from structured data
- Security and privacy by default
- Free-first infrastructure
- Modular monolith before microservices
- Automated testing for critical flows

## Planned stack

- Next.js + TypeScript
- Tailwind CSS + shadcn/ui
- Supabase PostgreSQL + Auth + Storage
- OpenAI API behind a provider abstraction
- Zod validation
- Vitest + Playwright
- EdgeOne for initial deployment
- GitHub + Spec Kit for source control and SDD

## Security

Never commit API keys, service-role credentials, database passwords, OAuth secrets, private certificates, or production environment files.

See [SECURITY.md](SECURITY.md).

## SDD

This project follows GitHub Spec Kit / Spec-Driven Development. Requirements, architecture, data contracts, acceptance criteria and tests are defined before production implementation.

Current governing document: [.specify/memory/constitution.md](.specify/memory/constitution.md)

## License

MIT License. See [LICENSE](LICENSE).
