# Global AI Agents Setup

This directory is the **Single Source of Truth** for all AI agents (Gemini, Claude, and GitHub Copilot) on this machine.

## How to Activate the Centralization

### 1. For Gemini CLI
This tool is already configured to use this folder. It prioritizes the rules in `GEMINI.md` and the global identity in `AGENTS.md`.

### 2. For Claude (Claude Desktop)
To give Claude access to your local tools and these instructions, link this configuration to Claude's official settings:

```bash
ln -sf /Users/ircham/.agents/mcp-config.json ~/Library/Application\ Support/Claude/claude_desktop_config.json
```
*Note: Restart Claude Desktop after running this command.*

### 3. For GitHub Copilot (VS Code)
To ensure Copilot follows your global standards:
1. Open VS Code Settings (`Cmd + ,`).
2. Search for `github.copilot.chat.customInstructions`.
3. Add the path: `/Users/ircham/.agents/COPILOT.md`.

### 4. For Antigravity
1. Link Global Instructions
  Antigravity uses ~/.gemini/GEMINI.md for its global behavior. Since we already created a GEMINI.md in your central folder, we can link it:

   1 `mkdir -p ~/.gemini`
   2 `ln -sf /Users/ircham/.agents/GEMINI.md ~/.gemini/GEMINI.md`

2. Link Global Skills
  Antigravity looks for global skills in ~/.gemini/antigravity/skills/. We can link your central skills folder there:
   1 `mkdir -p ~/.gemini/antigravity`
   2 `ln -sf /Users/ircham/.agents/skills ~/.gemini/antigravity/skills`

---

## Directory Structure

| File/Folder | Purpose | Target Provider |
| :--- | :--- | :--- |
| **`AGENTS.md`** | Global coding standards & identity. | **All Agents** |
| **`GEMINI.md`** | Specific instructions for Gemini CLI. | Gemini CLI |
| **`CLAUDE.md`** | Specific instructions for Claude. | Claude Desktop |
| **`COPILOT.md`** | Specific instructions for GitHub Copilot. | Copilot (VS Code) |
| **`skills/`** | The actual logic/tools (e.g., `resend`, `shadcn`). | **All Agents** |
| **`mcp-config.json`** | The bridge for Claude/Gemini/Cursor. | Claude, Cursor |

## Core Mandates (Summary)
- **Package Manager:** Always use `bun` and `bunx`.
- **Documentation:** Always maintain a `README.md` as the source of truth.
- **Naming:** PascalCase for components/types, camelCase for variables/functions.
- **Standards:** Atomic Design, try/catch for async, mandatory testing.
