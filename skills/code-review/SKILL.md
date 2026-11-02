---
name: code-review
description: Review a TypeScript/React change for correctness, architecture, security, performance, and adherence to this AI Kit. Use for pull requests, diffs, completed features, and bug fixes; do not use to implement a change.
---

# Code Review

Review the requested diff or change, starting with its intended behaviour and verification. Do not make edits unless the user also asks for a fix.

## Review process

1. Establish the scope: task intent, base revision, changed files, and checks already run.
2. Read relevant tests before implementation when they exist. Test behaviour through public boundaries, not component internals.
3. Trace changed inputs, state, error paths, and affected callers. Inspect adjacent modules when a contract changes.
4. Report only actionable findings, ordered by impact. Do not invent issues to fill a checklist.

## Review dimensions

- **Correctness**: expected behaviour, empty/loading/error states, validation, async races, and regression coverage.
- **Architecture**: follow the repository rules. Keep routes thin, domain behaviour in features, cross-domain utilities in `shared`, and public imports behind layer barrels. Avoid duplicate helpers and circular dependencies.
- **TypeScript and data boundaries**: no unjustified `any`; validate untrusted input with co-located Zod schemas; keep API DTO adaptation at the API boundary.
- **UI and state**: respect component and styling rules; use stable query keys; avoid unnecessary global Zustand state and avoid avoidable re-renders.
- **Security and reliability**: authorization and RLS where applicable, no secrets in source or logs, safe error handling, and no trust in external input.
- **Performance**: pagination for potentially large collections, bounded work, sensible query invalidation, and no obvious N+1 or render loops.

## Findings and outcome

For each finding include a priority, exact path and line/symbol, evidence, impact, and the smallest safe correction.

- `P0` — release blocker: data loss, security exposure, or broken core behaviour.
- `P1` — should fix before merge: likely defect, contract break, or significant regression.
- `P2` — worthwhile follow-up: maintainability or coverage concern with concrete impact.
- `P3` — optional suggestion; never present preference as a defect.

If there are no material findings, say so, name the scope reviewed, and list any remaining verification gap. Never claim tests, manual QA, or runtime checks were performed unless they actually were.

## Change size

Prefer focused, independently reviewable changes. Suggest splitting only when it materially obscures behaviour, mixes an unrelated refactor with a feature, or prevents meaningful verification. Do not block a change merely because it differs from a personal preference.
