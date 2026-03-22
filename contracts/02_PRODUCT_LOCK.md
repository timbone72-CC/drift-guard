# SECTION 2 — PRODUCT LOCK

## 2.1 CORE DEFINITION

Drift Guard V1 is a local-first developer tool that enforces mathematical equivalence of explicitly declared business logic expressions across codebases.

It does this by:
- extracting explicitly tagged logic expressions from source files
- comparing them using symbolic math
- failing execution when they are not identical

It is not:
- a data tool
- a documentation tool
- an inference engine
- an auto-fixer

It is a logic integrity enforcement engine.

---

## 2.2 V1 HARD BOUNDARIES

### INCLUDED

- mathematical expressions only
- Python-style arithmetic
- symbolic equivalence checking
- explicit tagged logic blocks
- strict variable identity

### EXCLUDED

- conditionals
- functions
- NULL handling
- type systems
- inference
- auto-mapping

---

## 2.3 DESIGN PRINCIPLES

- no magic
- no guessing
- no inference
- no silent passes
- fail loudly

---

## 2.4 FINAL STATEMENT

If two systems declare the same logic and calculate it differently, the system fails.
