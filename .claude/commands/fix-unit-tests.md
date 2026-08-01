---
name: fix-unit-tests
description: Workflow command scaffold for fix-unit-tests in microfeed.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /fix-unit-tests

Use this workflow when working on **fix-unit-tests** in `microfeed`.

## Goal

Fixes or updates existing unit test files after changes or to resolve test failures.

## Common Files

- `tests/unit/**/*.test.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Identify failing or outdated unit tests.
- Edit the relevant test files to fix issues or update expectations.
- Run the test suite to verify fixes.

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.