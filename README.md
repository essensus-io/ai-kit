# AI Kit
The single source of truth for AI-assisted development at Essensus. Contains rules, reusable skills, and slash commands — organized into general standards that apply everywhere and stack-specific guides.

## Contents

- **Rules** (`rules/`):
  - **General**
    - [Core standards](rules/general/core-standards.mdc) — global code style, naming, and TS conventions.
  - **Web**
    - [Folder structure](rules/web/folder-structure.mdc) — FSD-style layout for `src/app`, `src/features`, `src/shared`, and `src/screens`.
    - [React components](rules/web/react-components.mdc) — props, styling helpers, handler naming, and component splitting.
    - [Env](rules/web/env.mdc) — typed environment variables with `@t3-oss/env-core`.
    - [UI & styling](rules/web/ui-styling.mdc) — shadcn/ui, Radix, Tailwind, and responsive UI patterns.
    - [API layer](rules/web/api-layer.mdc) — shared API client conventions for `src/shared/api`.
    - [Global store](rules/web/global-store.mdc) — Zustand patterns for global stores in `src/shared/stores`.
  - **Technologies**
    - **RPC**
      - [tRPC](rules/technologies/rpc/trpc.mdc) — tRPC router, typing, and server module structure.
      - [tRPC + TanStack Query](rules/technologies/rpc/trpc-tanstack-query.mdc) — using `@trpc/tanstack-react-query` with React Query for typed queries and mutations.
      - [oRPC](rules/technologies/rpc/orpc.mdc) — oRPC router, typing, and error handling conventions.
      - [oRPC + TanStack Query](rules/technologies/rpc/orpc-tanstack-query.mdc) — integrating oRPC clients with TanStack Query (queries, infinite queries, streaming, mutations).
    - **Supabase**
      - [Supabase auth](rules/technologies/subabase/supabase-auth.mdc) — using Supabase auth safely in server code.
      - [Postgres RLS](rules/technologies/subabase/postgres-rls.mdc) — RLS-aware query and access patterns.
    - [Prisma](rules/technologies/prisma.mdc) — Prisma models, migrations, and seeds conventions.
- **Skills** (`skills/`):
  - [Commit messages](skills/commit-messages/SKILL.md) — generate conventional commit messages from diffs or staged changes.
  - [Immer](skills/immer/SKILL.md) — use Immer to write mutable-style updates for immutable state (nested objects, arrays, reducers).
  - [date-fns](skills/date-fns/SKILL.md) — standardize all date/time parsing, formatting, and arithmetic with date-fns.
  - [ts-pattern](skills/ts-pattern/SKILL.md) — replace complex `if`/`switch` chains with type-safe pattern matching.
- **Commands** (`commands/`):
  - [Daily status](commands/daily-status.md) — generate daily standup-style status updates.
  - [PR](commands/pr.md) — create or update GitHub pull requests with a consistent title and body template.