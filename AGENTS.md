# AGENTS.md - Root Context Engineering Standard (MurdaSoft Vibe MapOS)

> Universal, vendor-agnostic context file for Claude Code, Cursor, Codex, Windsurf, and Antigravity.

## 1. Core Engineering Philosophy
- **Plan Before Code:** Never generate multi-file changes without first inspecting existing contracts and writing a concise step-by-step plan.
- **Reverse Prompting Gate:** If requirements have blind spots (auth, DB concurrency, edge cases, mobile 375px), ask 3–5 sharp questions before coding.
- **Zero Stubs:** Never leave `// TODO`, `placeholder`, or fake mock handlers in production code.

## 2. Hard Constraints (The Do-Not-Do List)
- **NO Legacy Stacks:** Do not use `create-react-app`, raw unvalidated `req.json()`, or raw SQL string concatenation.
- **NO Client-Only Auth:** Every mutating API route and Server Action must verify session + resource ownership on the server (prevent IDOR).
- **NO AI-Slop UI:** Do not generate generic purple-blue gradients, blurry neon shadows, or >2 stacked toolbars. Follow `architecture-and-design/anti-slop-ui.md`.
- **NO Docker UFW Bypass:** Bind internal DB/Redis ports to `127.0.0.1:` in `docker-compose.yml`.

## 3. Repository Navigation (Progressive Disclosure)
- `memory-bank/` - Persistent project state (`activeContext.md`, `productContext.md`, `systemPatterns.md`). Always read on session start and update before exit.
- `mcp-registry/mcp-servers.json` - Standard MCP servers (GitHub, Figma, Playwright, Firecrawl, Qdrant, E2B).
- `architecture-and-design/` - FSD v2.1 layer rules, Zod `.strict()` contracts, and Anti-Slop UI rules.
- `automation-and-swarms/` - Planner/Generator/Reviewer swarm prompts and Playwright Self-Healing guardrails.
- `production-and-local/` - DevSecOps, `llms.txt` (AEO), N+1 prevention, and Telegram Mini App + Kaspi QR patterns.
