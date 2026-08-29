```markdown
# n8n Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches the core development patterns and workflows used in the [n8n](https://github.com/n8n-io/n8n) codebase, a TypeScript-based project for workflow automation. You'll learn the project's coding conventions, how to structure features and bugfixes (including tests), and how to work with both backend and frontend code. This guide also covers the use of conventional commits and provides ready-to-use commands for common development tasks.

## Coding Conventions

**File Naming**

- Use `camelCase` for filenames.
  - Example: `userService.ts`, `workflowRunner.ts`

**Import Style**

- Use **relative imports**.
  - Example:
    ```typescript
    import { getUser } from './userService';
    ```

**Export Style**

- Use **named exports**.
  - Example:
    ```typescript
    export function runWorkflow() { ... }
    export const WORKFLOW_STATUS = { ... };
    ```

**Commit Messages**

- Follow [Conventional Commits](https://www.conventionalcommits.org/):
  - Prefixes: `fix`, `feat`, `refactor`
  - Example: `feat: add support for custom webhook headers`

## Workflows

### Feature or Bugfix with Tests

**Trigger:** When adding a new feature or fixing a bug, always with corresponding test updates or additions.  
**Command:** `/feature-with-tests`

1. **Edit or create implementation files**  
   - Add or update `.ts` (TypeScript) or `.vue` (Vue component) files in the relevant module or feature directory.
   - Example:
     ```typescript
     // src/features/user/userService.ts
     export function createUser(data: UserData) { ... }
     ```
2. **Edit or create corresponding test files**  
   - Add or update `.test.ts` or `.test.vue` files in the same or related directory.
   - Example:
     ```typescript
     // src/features/user/userService.test.ts
     import { createUser } from './userService';
     test('should create a user', () => {
       expect(createUser({ name: 'Alice' })).toBeDefined();
     });
     ```

**Files Involved:**
- `**/*.ts`
- `**/*.vue`
- `**/*.test.ts`
- `**/*.test.vue`

---

### Frontend Feature or Bugfix with Store and View

**Trigger:** When adding or fixing a frontend feature that involves both state management (store) and UI (view), often with tests.  
**Command:** `/frontend-feature`

1. **Edit or create a store file**
   - Add or update `*.store.ts` in the frontend feature directory.
   - Example:
     ```typescript
     // packages/frontend/features/user/user.store.ts
     export const userStore = { ... };
     ```
2. **Edit or create a view or component file**
   - Add or update `*.vue` in the same feature directory.
   - Example:
     ```vue
     <!-- packages/frontend/features/user/UserProfile.vue -->
     <template>
       <div>{{ user.name }}</div>
     </template>
     <script lang="ts">
     import { userStore } from './user.store';
     export default { ... }
     </script>
     ```
3. **Edit or create a corresponding test file**
   - Add or update `*.test.ts` or `*.test.vue`.
   - Example:
     ```typescript
     // packages/frontend/features/user/user.store.test.ts
     import { userStore } from './user.store';
     test('userStore initializes correctly', () => {
       expect(userStore.state).toBeDefined();
     });
     ```

**Files Involved:**
- `packages/frontend/**/features/**/*.store.ts`
- `packages/frontend/**/features/**/*.vue`
- `packages/frontend/**/features/**/*.test.ts`
- `packages/frontend/**/features/**/*.test.vue`

## Testing Patterns

- **Framework:** [Jest](https://jestjs.io/)
- **Test file pattern:** `*.test.ts` (and `*.test.vue` for Vue components)
- **Test location:** In the same or related directory as the implementation.
- **Example:**
  ```typescript
  // src/utils/calculateSum.test.ts
  import { calculateSum } from './calculateSum';
  test('adds numbers correctly', () => {
    expect(calculateSum(2, 3)).toBe(5);
  });
  ```

## Commands

| Command              | Purpose                                                        |
|----------------------|----------------------------------------------------------------|
| /feature-with-tests  | Start a new feature or bugfix with corresponding tests         |
| /frontend-feature    | Add or fix a frontend feature with store, view, and tests      |
```
