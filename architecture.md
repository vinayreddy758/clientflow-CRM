# ClientFlow — Architecture

ClientFlow is a full-stack monolithic web application.

## Tech Stack
- **Framework:** TanStack Start (React 19, TypeScript)
- **Styling:** Tailwind CSS v4
- **Database:** Supabase PostgreSQL
- **Authentication:** Supabase Auth

## Architecture Diagram
```text
Browser
   ↓
TanStack Start
   ├── React UI
   └── Server-side logic
          ↓
       Supabase
       ├── PostgreSQL
       ├── Auth
       └── Storage (when required)
```