---
name: browser-testing
description: Plan and perform focused manual browser QA for a web change. Use for user-visible flows, visual regressions, and end-to-end checks; do not assume a particular browser automation tool, port, or login method.
---

# Browser Testing

Verify the user-visible behaviour that changed. Use the browser and automation capability available in the current environment; do not prescribe Chrome DevTools, a local port, or credentials that may not exist.

## Before testing

- Identify the changed flow, expected outcome, test data, environment, and required account/permissions.
- Reuse documented project commands and avoid changing shared environments or production data.
- If authentication or a required integration is unavailable, report the blocked scenario and validate independent parts instead of fabricating a result.

## Test the flow

Exercise the happy path, one relevant validation or failure path, loading and empty states where applicable, and the changed responsive layout if it is a UI change. Check that errors are understandable and do not expose sensitive data.

Capture a screenshot or short recording when it materially helps a reviewer confirm a visual or interaction change. Do not claim manual testing from code inspection alone.

## Report

State the environment, scenarios attempted, observed result, evidence captured, and anything not verified. Turn a discovered defect into a reproducible report with steps, expected result, actual result, and relevant console or network evidence when available.
