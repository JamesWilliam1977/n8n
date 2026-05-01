---
name: frontend-feature-or-bugfix-with-store-and-view
description: Workflow command scaffold for frontend-feature-or-bugfix-with-store-and-view in n8n.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /frontend-feature-or-bugfix-with-store-and-view

Use this workflow when working on **frontend-feature-or-bugfix-with-store-and-view** in `n8n`.

## Goal

Implements or fixes a frontend feature, involving both store logic and view components, often with tests.

## Common Files

- `packages/frontend/**/features/**/*.store.ts`
- `packages/frontend/**/features/**/*.vue`
- `packages/frontend/**/features/**/*.test.ts`
- `packages/frontend/**/features/**/*.test.vue`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or create a store file (e.g., *.store.ts) in the frontend feature directory.
- Edit or create a view or component file (e.g., *.vue) in the same feature directory.
- Edit or create a corresponding test file (e.g., *.test.ts or *.test.vue).

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.