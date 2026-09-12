# Feature Specification: Lab MVP Core

## Goal
Allow an e-learning content developer to transform a storyboard or source document into an editable, interactive, testable web learning experience.

## User stories
- Create and manage a learning project.
- Paste or upload a storyboard.
- Ask Lab to analyze the source.
- Review generated learning objectives and structure.
- Generate and edit interactive learning objects.
- Preview the learner experience on desktop/mobile.
- Run content, interaction, and objective-coverage QA.
- Fix issues and publish a web course.

## MVP inputs
- Pasted storyboard text
- DOCX
- PDF

## MVP interaction types
- Content
- Multiple choice
- True/false
- Drag & drop
- Scenario

## Acceptance criteria
### AC-01 Project
A signed-in user can create, rename, archive, and open a project. A project is accessible only to authorized users.

### AC-02 Import
A user can paste text or upload a supported DOCX/PDF. Unsupported type, oversized files, malformed files, and parsing failures produce safe actionable errors.

### AC-03 AI analysis
The system extracts learning objectives, sections, content, potential interactions, assessment candidates, and unresolved ambiguities. AI output is schema-validated before persistence.

### AC-04 Review
The user can accept, edit, or reject generated content before it becomes part of the course.

### AC-05 Editor
The user can create, edit, reorder, duplicate, and delete MVP learning objects.

### AC-06 Preview
Preview renders from the canonical learning model and supports desktop and mobile viewport modes.

### AC-07 QA
QA reports errors, warnings, suggestions, and passed checks with category, message, location, and status. Critical findings cannot be represented as production-ready.

### AC-08 Objective coverage
The system maps learning objects/assessments to objectives and identifies objectives with insufficient assessment coverage.

### AC-09 Publish
A validated course can be published as a web-based interactive course snapshot. Publishing never exposes secrets or private source documents.

## Security acceptance criteria
- Authentication and authorization are enforced server-side.
- Supabase Row Level Security isolates user/project data.
- Service-role credentials are server-only.
- File uploads are type/size validated and treated as untrusted.
- AI output is validated with schemas before persistence/rendering.
- AI output is never executed as code/SQL/shell commands.
- Sensitive values are not written to application logs.
- AI and upload endpoints have abuse/rate controls before production release.

## Non-goals
LMS, payments, student analytics, enterprise SSO, collaboration, H5P export, SCORM export, and a full H5P-compatible authoring engine are outside MVP.
