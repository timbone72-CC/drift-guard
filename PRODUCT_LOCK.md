# Drift Guard V1 — PRODUCT LOCK SPEC

## Core Definition
Drift Guard V1 is a local-first developer tool that enforces mathematical equivalence of business logic expressions across codebases.

It extracts explicitly tagged expressions and compares them using symbolic math.
If they differ, the system fails.

## Scope (V1)
Included:
- Mathematical expressions only
- Python-style arithmetic
- Symbolic equivalence checking
- Explicit tagged blocks
- Strict variable identity

Excluded:
- Conditionals
- Functions
- NULL handling
- Type systems
- Inference or guessing

## Principle
No magic.
No guessing.
Fail loudly and deterministically.

## Final Statement
If two systems calculate the same concept differently, the system fails.
