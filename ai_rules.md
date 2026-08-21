# ClientFlow — AI Development Rules

1. **Source of Truth:** Codebase > Project Context Docs > Task Spec. Never invent project state.
2. **Small Steps:** Work in small, well-defined units. Avoid generating entire architectures at once.
3. **Follow Patterns:** Use existing project patterns and reusable components. Do not create unnecessary abstractions.
4. **Scope Control:** Implement only the requested scope. Do not add unapproved features, dependencies, or database tables.
5. **Security First:** Never expose secrets, trust client authorization, or bypass workspace isolation.
6. **Verify Work:** Run type checks (`npx tsc --noEmit`), build the project, and verify behavior before concluding tasks.