# FSD v2.1 & Zod Contracts (MurdaSoft Block 03)

## Layer Hierarchy (Strict Top-Down Imports Only)
1. `app` — App initialization, providers, global styles
2. `processes` — Multi-page flows (optional)
3. `pages` — Route composition
4. `widgets` — Self-contained UI + data blocks
5. `features` — User interactions & business actions
6. `entities` — Core domain models & UI cards
7. `shared` — UI kit (`shadcn/ui`), API client, lib helpers

**Hard Rule:** A module may ONLY import from layers strictly below it. Cross-imports between slices on the same layer are forbidden.

## API Boundary Contract (`zod.strict()`)
```ts
import { z } from 'zod';

export const CreateOrderSchema = z.object({
  itemId: z.string().min(1),
  quantity: z.number().int().min(1).max(100),
  idempotencyKey: z.string().uuid(),
}).strict();
```
