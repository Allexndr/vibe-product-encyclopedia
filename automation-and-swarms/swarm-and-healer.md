# Subagent Swarm Roles & Playwright Self-Healing (MurdaSoft Blocks 04 & 05)

## 1. Swarm Roles (Zero Stubs Pipeline)
- **Planner:** Reads `AGENTS.md` + `memory-bank/` + target files. Produces a step-by-step Markdown checklist. Does NOT write production code.
- **Generator(s):** Work in isolated `git worktree` branches on disjoint slices (DB migration / API route / UI component).
- **Reviewer:** Runs typecheck, lint, FSD boundary check, and OWASP/IDOR review before merge.

## 2. Playwright Self-Healing Guardrails
When an E2E test fails due to a changed DOM locator:
1. **Allowed:** Update the selector (`data-testid`, `getByRole`) using the live accessibility tree.
2. **FORBIDDEN:** Never modify `expect(...)` business assertions to make a failing test pass!
3. **Max Retries:** Hard cap of **3 healing attempts** per test before escalating to a human engineer.
