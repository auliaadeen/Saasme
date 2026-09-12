# Lab Project Constitution

## Principle 1 — Specification Before Implementation
No production feature shall be implemented without an approved specification.

## Principle 2 — Structured Learning Model
All learning content must use a validated, versioned structured learning model. AI output must never bypass schema validation.

## Principle 3 — AI Is Assistive, Not Authoritative
AI-generated content is untrusted, editable, reviewable, and subject to validation.

## Principle 4 — Deterministic Rendering
Interactive experiences are rendered from structured data. AI must never directly control executable application logic.

## Principle 5 — Security and Privacy by Default
Secrets, private content, credentials, and internal implementation details must be protected by default. User data must be isolated by authorization and database policy.

## Principle 6 — Quality Is a Product Feature
Content QA, interaction QA, accessibility, and learning-objective coverage are first-class product concerns.

## Principle 7 — Free-First Architecture
The MVP prioritizes free or already-available infrastructure.

## Principle 8 — Reuse Existing Engineering Knowledge
Prefer technologies already used successfully in Zunara AI and Smesh AI unless a measurable requirement justifies a different choice.

## Principle 9 — Simple Before Scalable
Use a modular monolith for the MVP. Avoid premature microservices.

## Principle 10 — Testable by Design
Critical user flows must have acceptance criteria and automated tests.

## Principle 11 — Accessible and Responsive
The product and generated learning experiences must work on desktop and mobile and should not rely solely on color.

## Principle 12 — Observable Failures
Parsing, AI, validation, publishing, and infrastructure failures must produce actionable user-facing errors without leaking sensitive internals.

## Principle 13 — Provider Independence
The domain model must not depend on OpenAI, H5P, Supabase, EdgeOne, or another provider.

## Principle 14 — Portfolio Quality
The MVP should be reliable, understandable, documented, and demonstrable as a real product.

## Principle 15 — Secure AI Boundary
Uploaded documents, prompts, and model output are untrusted data. The application must never execute model-generated code, SQL, shell commands, or arbitrary HTML.

## Governance
Architectural decisions that conflict with this constitution require explicit documentation and justification. This constitution governs specifications, plans, tasks, implementation, and convergence reviews.
