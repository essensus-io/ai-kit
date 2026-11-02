---
name: change-intelligence
description: Explain what changed across a diff, branch, pull request, or release using repository evidence. Use for catch-up, impact analysis, and risk assessment; do not use for a simple code review request.
---

# Change Intelligence

Help an owner understand change, not merely enumerate commits. Establish the exact repository and revisions before drawing conclusions. Distinguish merged code from deployed code.

## Choose proportionate depth

- **Quick scan**: a local, low-risk change — what changed, why it matters, and an obvious follow-up.
- **Focused analysis**: a feature or several related modules — behaviour before/after, affected callers, tests, and concrete risks.
- **Deep analysis**: contracts, data ownership, security, migrations, or cross-module work — trace the relevant flow end to end and inspect historical context when useful.
- **Project-level catch-up**: a release or long time period — group changes by outcome and subsystem rather than listing commits.

Increase depth only when evidence reveals wider impact. Stop when the requested scope is covered and further inspection is unlikely to change the decision.

## Evidence and reporting

Ground material claims in diffs, code paths, tests, configuration, migrations, and relevant history. Separate:

- **Confirmed facts** — directly supported by repository evidence.
- **Risks** — plausible impact that still needs verification.
- **Unknowns** — information absent from the repository or scope.

For focused and deeper analyses, report: scope and revisions; behaviour and architecture changes; contract/data implications; verification evidence and gaps; prioritized risks; and up to five concrete follow-ups. Do not persist project-history files or advance a checkpoint unless the user asks.
