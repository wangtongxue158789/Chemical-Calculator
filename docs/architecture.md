# Architecture Overview

## Design principles

- **Domain-first modeling**: represent chemical concepts explicitly.
- **Deterministic calculations**: avoid hidden behavior and non-reproducible results.
- **Layered responsibilities**: parsing, domain modeling, calculation, and I/O should remain separated.

## Proposed module boundaries

### 1) Parser layer (`src/parser/`)

Responsibilities:

- Convert formula strings into normalized internal structures.
- Validate syntax and report precise parse errors.

Output example:

- Input: `Ca(OH)2`
- Output: `{ "Ca": 1, "O": 2, "H": 2 }`

### 2) Domain/core layer (`src/core/`)

Responsibilities:

- Define shared domain types.
- Define unified error classes/codes used across modules.
- Encapsulate constants or data access contracts for periodic table values.

### 3) Calculator layer (`src/calculators/`)

Responsibilities:

- Implement concrete chemical calculations using parsed/domain data.
- Keep algorithms pure and easily testable.

Initial target:

- `molar_mass` calculator: sum of (atomic weight × element count).

### 4) Interface layer (future)

Responsibilities:

- CLI / API / UI adapters.
- Input validation at boundaries and response formatting.

## Testing strategy

- `tests/parser/`: valid and invalid formula coverage.
- `tests/calculators/`: numeric correctness and boundary handling.
- Keep test names aligned with business scenarios.

## Initial roadmap

1. Implement formula parser with nested group support.
2. Add molar mass calculator using a small periodic table dataset.
3. Add error model and user-facing error messages.
4. Introduce CLI or HTTP interface after core logic stabilizes.
