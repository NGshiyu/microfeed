```markdown
# microfeed Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you how to contribute to the `microfeed` repository, a TypeScript project built on the Astro framework. You'll learn the project's coding conventions, how to manage and fix unit tests, and the common workflows and commands used in development.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `feedManager.ts`

### Import Style
- Mixed import styles are used. Both default and named imports may appear.
  - Example:
    ```typescript
    import React from 'react';
    import { getFeed } from './feedManager';
    ```

### Export Style
- **Default exports** are preferred.
  - Example:
    ```typescript
    const FeedManager = () => { /* ... */ };
    export default FeedManager;
    ```

## Workflows

### Fix Unit Tests
**Trigger:** When someone needs to fix failing unit tests or update them after code changes.  
**Command:** `/fix-tests`

1. **Identify** failing or outdated unit tests.
   - Run the test suite with `vitest` to see which tests are failing.
     ```bash
     npx vitest
     ```
2. **Edit** the relevant test files to fix issues or update expectations.
   - Example:
     ```typescript
     // Before: outdated expectation
     expect(getFeed().length).toBe(5);

     // After: updated expectation
     expect(getFeed().length).toBe(6);
     ```
3. **Run** the test suite again to verify that all tests pass.
   - Example:
     ```bash
     npx vitest
     ```

**Files Involved:**  
- `tests/unit/**/*.test.ts`

**Frequency:**  
- Approximately 2 times per month.

## Testing Patterns

- **Framework:** [vitest](https://vitest.dev/)
- **Test File Pattern:** All unit tests are placed in files matching `*.test.ts`.
  - Example: `userProfile.test.ts`
- **Test Example:**
  ```typescript
  import { describe, it, expect } from 'vitest';
  import getFeed from '../feedManager';

  describe('getFeed', () => {
    it('returns an array of feed items', () => {
      const feed = getFeed();
      expect(Array.isArray(feed)).toBe(true);
    });
  });
  ```

## Commands

| Command     | Purpose                                             |
|-------------|-----------------------------------------------------|
| /fix-tests  | Fix or update unit tests after code changes         |
```
