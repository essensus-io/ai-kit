---
name: codebase-onboarding
description: Build a concise, evidence-based working model of an unfamiliar codebase for future AI-assisted development. Use when onboarding or documenting a repository; do not generate a large context directory for a small targeted task.
---

# Codebase Onboarding

Produce only the context needed to work safely in the repository. Start with existing instructions and documentation, then verify them against the code and runnable commands.

## Investigate

- Entry points, package manager, development/test/lint/build commands, and environment requirements.
- Top-level modules, ownership boundaries, dependency direction, and important domain flows.
- Data schemas, API/RPC contracts, authentication boundaries, configuration, migrations, and external integrations when present.
- Existing engineering conventions, test layout, and CI checks.

Use deterministic repository evidence first: manifests, configuration, source imports, tests, and git history. Explain uncertainty rather than inventing architecture from directory names.

## Deliverable

Return a compact map containing the project purpose, commands verified versus merely discovered, architecture, critical flows, local conventions, and open questions. Link every important statement to relevant paths.

When the user requests persistent context, update or create the repository's existing instruction format first. Create `AGENTS.md` or a `context/` directory only with explicit authorization and keep it concise, revision-aware, and easy to maintain. Do not add AST tooling, generated inventories, or scripts unless the repository's size and repeated use justify them.
