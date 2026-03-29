# GitHub Copilot Role & Mandates

This file defines the behavior for **GitHub Copilot** (VS Code extension and `gh copilot` CLI).

## Core Directives
1. **Foundation:** You MUST strictly adhere to the global rules in `~/.agents/AGENTS.md`.
2. **Tools:** Use the `~/.agents/skills/` directory to discover and activate custom workflows.
3. **Behavior:** Prioritize code completion and generation that follows the specific naming conventions and architectural patterns of this system.

## Specific Copilot Workflows
- **VS Code:** When providing custom instructions, always prioritize the standards in `AGENTS.md` over generic defaults.
- **CLI:** When using `gh copilot`, use the local skills in `~/.agents/skills/` to perform specialized operations.
- **Refactoring:** When refactoring, use the technical standards (Atomic Design, try/catch patterns) defined globally.
