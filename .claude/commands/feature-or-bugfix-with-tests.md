---
name: feature-or-bugfix-with-tests
description: Workflow command scaffold for feature-or-bugfix-with-tests in n8n.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-or-bugfix-with-tests

Use this workflow when working on **feature-or-bugfix-with-tests** in `n8n`.

## Goal

Implements a new feature or fixes a bug, always accompanied by corresponding test updates or additions.

## Common Files

- `**/*.ts`
- `**/*.vue`
- `**/*.test.ts`
- `**/*.test.vue`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or create implementation files (e.g., .ts, .vue) in the relevant module or feature directory.
- Edit or create corresponding test files (e.g., .test.ts, .test.vue) in the same or related directory.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.