# Newcomer Onboarding Guide

## What to understand first

1. **Business scope**: this project focuses on chemistry calculations, not generic math utilities.
2. **Core flow**: input formula -> parse -> validate -> calculate -> return result.
3. **Quality bar**: every feature should include tests and clear error behavior.

## First-week learning plan

### Day 1

- Read `README.md` and `docs/architecture.md`.
- Understand target module boundaries and naming conventions.

### Day 2-3

- Review parser requirements and write sample test cases for formula parsing.
- Focus on edge inputs (parentheses, invalid symbols, malformed counts).

### Day 4-5

- Implement or extend one small feature (prefer parser or molar mass).
- Add/adjust tests and update docs for behavior changes.

## Contribution checklist

Before opening a PR:

- [ ] Behavior is documented in README/docs when applicable.
- [ ] Tests are added/updated for happy path and edge cases.
- [ ] Errors are explicit and actionable.
- [ ] Changes are scoped to one coherent problem.

## Coding guidance

- Keep modules small and single-purpose.
- Prefer pure functions for parsing/calculation logic.
- Avoid coupling parser internals directly to UI or transport layers.
