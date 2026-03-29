# Global AI Agent Identity & Coding Standards

This file defines the core behavioral rules and coding standards that **all** AI agents (Gemini, Claude, and Copilot) on this system must follow.

## Core Mandates
- **Environment:** All JavaScript/TypeScript projects MUST use `bun` and `bunx` for package management.
- **Project Context:** Always maintain a `README.md` in the workspace root as the source of truth for the codebase.
- **Reliability:** Prioritize empirical reproduction of bugs and automated verification for all changes.
- **Collaboration:** Always seek to understand the existing codebase and collaborate with other agents before making changes.
- **Naming Conventions:** All variables, functions, and components choice of words MUST describe their purpose and functionality.
- **Documentation:** All code changes MUST be accompanied by clear, concise documentation and comments explaining the rationale behind the change.

## Naming Conventions
- **Components/Types:** PascalCase
- **Variables/Functions:** camelCase
- **Private Members:** Prefix with `_`
- **Constants:** ALL_CAPS
- **Compatibility:** Use `snake_case` only for external schema compatibility.

## Technical Standards
- **Error Handling:** Use try/catch blocks for async logic and other possible error scenarios. Implement proper error boundaries.
- **Logging:** Always provide contextual information for debugging.
- **Skills:** Always check `~/.agents/skills/` for relevant tools before starting a task.
- **Atomic Design:** Follow atomic design principles for UI components and functions, ensuring reusability and maintainability.
- **Testing:** All changes MUST include tests that verify the intended behavior and prevent regressions.
- **Security Reviews:** All code changes MUST undergo a security review to identify and mitigate potential vulnerabilities.
- **Version Control:** Use clear and descriptive commit messages that explain the purpose of the change.
