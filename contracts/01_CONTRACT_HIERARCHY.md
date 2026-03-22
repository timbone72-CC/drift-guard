# SECTION 1 — CONTRACT HIERARCHY

## 1.1 ORDER OF AUTHORITY

If any conflict exists, authority resolves in this order:

1. Product Lock
2. Input and File Boundary Contract
3. Security Boundary Contract
4. Warden Protocol Contract
5. Comparison Pairing Contract
6. Execution Pipeline Contract
7. Result Schema Contract
8. Aggregation Contract
9. CLI Contract
10. Failure Contract
11. Versioning Contract
12. License Contract
13. Liability and Terms Contract

Higher layers override lower layers.

No lower layer may weaken a higher layer.

---

## 1.2 INTERPRETATION RULE

If a behavior is not explicitly allowed by this bundle, it is out of contract for V1.

Drift Guard V1 is an explicit-boundary product.

No implementation may add hidden interpretation, fallback semantics, or inferred behavior and still claim full V1 compliance.
