---
name: test-driven-development
description: Implement a behaviour change or bug fix through small red-green-refactor cycles. Use when the user requests test-first work, regression coverage, or when a change has meaningful domain logic; do not force it for trivial presentational edits.
---

# Test-Driven Development

Use TDD to establish confidence in behaviour, not to maximize test count.

## The loop

1. Identify the public seam: a pure function, API/RPC contract, user interaction, or integration boundary.
2. Add one failing test that expresses an observable requirement, including a known expected value from the specification or a worked example.
3. Implement only the smallest change that makes it pass.
4. Refactor after the suite is green, preserving behaviour. Repeat in small vertical slices.

## Test quality

- Test behaviour through public interfaces. Avoid private-method tests, implementation-coupled mocks, and assertions about incidental markup or calls.
- Cover the new rule, its important boundary or failure case, and the reported regression for a bug fix.
- Keep tests deterministic. Control time, randomness, network, and external services at the boundary.
- Prefer real collaborators when they are cheap and reliable; mock only external, slow, nondeterministic, or failure-mode-specific boundaries.
- Name tests in domain language: the name should explain the capability or policy being protected.

## Stack guidance

Place tests alongside the project's existing convention. For React work, test a user-observable interaction and resulting state rather than component internals. For server work, validate inputs and error contracts at the API/RPC boundary. Respect the repository's Zod and typed API conventions in fixtures and assertions.

If no suitable test harness exists, explain the gap and propose the smallest setup needed; do not silently introduce a testing framework.
