# ClientFlow — Security Rules

## Core Principle
Anything controlled by the browser is untrusted. Validate everything on the server.

## Authentication & Authorization
- **Authentication** (Supabase Auth) verifies identity but does not grant permissions.
- **Authorization** must verify: Authenticated User + Workspace Membership + Required Role + Resource Ownership.

## Workspace Isolation (Multi-Tenancy)
- Resources must be strictly isolated by workspace.
- Enforced via application-level checks and PostgreSQL Row Level Security (RLS).
- Users must never access other workspaces' data by manipulating IDs.

## Roles
- **Owner, Admin, Member**. Do not create custom roles.

## Secret Handling
- Never expose or commit service-role keys, private API keys, or database credentials to Git or the browser.

## Input Validation
- Validate all external input on the server-side. Never trust client-provided IDs, roles, or prices.