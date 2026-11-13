# systemPatterns.md — Architectural Contracts & Patterns

## Stack & Boundaries
- Frontend: Next.js / React + TypeScript + Tailwind + shadcn/ui (FSD v2.1 layers)
- Validation: `zod.strict()` at every API boundary
- Persistence: Parameterized ORM / MongoDB queries with explicit indexes

## Security & Reliability Invariants
- AuthN/AuthZ verified server-side on every private route
- Outbound `fetch` to user URLs protected against SSRF (`127.0.0.1`, `169.254.169.254`, private CIDRs)
- Payment/webhook handlers are strictly idempotent
