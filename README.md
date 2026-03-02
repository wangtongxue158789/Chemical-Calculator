# Chemical Calculator

Chemical Calculator is an early-stage project for building reliable chemistry-related calculations in a structured, testable way.

## Current status

This repository currently provides a starter project structure and onboarding documentation. Core calculation features are still to be implemented.

## MVP goals

The first milestone should focus on a small, usable subset of features:

1. Parse basic chemical formulas (for example: `H2O`, `Ca(OH)2`, `H2SO4`).
2. Compute molar mass from parsed formulas.
3. Return clear errors for invalid formulas.
4. Provide deterministic test cases for core parsing and mass calculation logic.

## Repository structure

- `docs/architecture.md`: high-level architecture and module boundaries.
- `docs/onboarding.md`: newcomer learning path and contribution flow.
- `src/`: source code for calculator modules.
- `tests/`: unit and integration tests.

## Suggested development workflow

1. Write or update a requirement in docs.
2. Add tests that describe expected behavior.
3. Implement the smallest working code change.
4. Run tests and formatting checks.
5. Open a PR with examples and edge cases.

## Next implementation targets

- `src/parser/`: formula tokenizer + parser.
- `src/calculators/molar_mass/`: molar mass computation.
- `src/core/errors.py`: unified domain error model.
- `tests/parser/` and `tests/calculators/`: feature-level test suites.
