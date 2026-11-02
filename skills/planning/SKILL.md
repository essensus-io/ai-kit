---
name: planning
description: Plan a substantial software change as small, ordered, verifiable slices. Use when scope, dependencies, sequencing, or acceptance criteria are unclear; skip for a straightforward small edit.
---

# Planning a Change

Inspect the relevant code and repository conventions before proposing work. The plan is an aid to implementation, not a substitute for the user's product decisions.

## Shape the work

- State the outcome, constraints, assumptions, and unresolved product questions.
- Map only the dependencies that affect implementation order: schema, contracts, validation, server/API, client state, UI, and deployment configuration.
- Prefer vertical slices that deliver a testable user outcome. Use horizontal groundwork only when it unlocks several slices.
- Surface risky or irreversible work early: migrations, auth/permission changes, public API compatibility, and third-party integrations.

## Task format

For each task provide:

- **Outcome** — the user-visible or technical capability delivered.
- **Acceptance criteria** — observable conditions that establish success.
- **Likely areas** — files or modules, expressed as estimates rather than promises.
- **Verification** — the smallest relevant test, type check, build, or manual QA step.
- **Dependencies** — only when sequencing matters.

Keep tasks small enough to implement and verify in one focused pass. Split a task when it combines independent outcomes, crosses unrelated subsystems, or cannot have clear acceptance criteria.

## Output and authority

Present plans in the response by default. Create plan files or task trackers only when the user requests persistent planning artifacts. Do not begin implementation if an unanswered question would materially change the product or data model; otherwise state the assumption and continue when implementation is authorized.
