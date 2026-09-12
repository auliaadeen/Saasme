# Lab Architecture

## Principle
The domain model is provider-independent. AI generates structured learning data; deterministic application code validates, stores, and renders it.

```text
User
  ↓
Next.js UI
  ↓
Application services
  ├── Storyboard parser
  ├── AI provider
  ├── Learning model validator
  ├── QA engine
  └── Publishing
  ↓
Supabase PostgreSQL / Storage
```

## Canonical flow
Storyboard → parsing → AI analysis → schema validation → learning model → editor → preview → QA → published snapshot.

## Security boundary
Browser code never receives server-only secrets. Supabase service-role credentials and OpenAI keys remain server-side. Database access is constrained by Row Level Security. Uploaded files and model output are untrusted.

## Future exporters
H5P and SCORM should consume the canonical learning model through deterministic exporters rather than becoming the internal domain representation.
