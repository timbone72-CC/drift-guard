# SECTION 3 — INPUT AND FILE BOUNDARY CONTRACT

## 3.1 CORE RULE

Drift Guard V1 accepts text-based source inputs only.

It does not operate on:
- binary files
- compiled artifacts
- images
- archives
- opaque structured blobs as comparison authority

---

## 3.2 REQUIRED INPUT SHAPE

V1 accepts exactly two input files.

Each input must be:
- a readable file path
- file content, not a directory
- decodable as text
- suitable for raw text tag scanning

Directories are invalid inputs.

---

## 3.3 FILE READABILITY RULE

If either file cannot be read because it is missing, locked, inaccessible, unreadable, or permission-blocked, the run fails as infrastructure failure.

Unreadable input cannot become PASS.

---

## 3.4 RAW TEXT SCAN RULE

Drift Guard scans the full file as plain text for Warden tags.

It does not require:
- AST parsing of the host language
- semantic understanding of surrounding code
- file-extension-specific interpretation

The scanning surface is raw text only.

---

## 3.5 EMPTY INPUT RULE

If either file is empty, the run fails.

V1 does not support empty-source success.

---

## 3.6 NO-BLOCK RULE

If both files contain zero valid Warden blocks, the run fails.

Reason:
NO_BLOCKS_FOUND

V1 does not treat no-op comparison as PASS.

---

## 3.7 SINGLE-SIDED BLOCK RULE

If one file contains valid Warden blocks and the other does not, the run fails.

Reason:
BLOCK_SET_MISMATCH

---

## 3.8 WHOLE-FILE AUTHORITY RULE

Only explicitly tagged Warden blocks are in scope.

All untagged content is out of scope.

Drift Guard does not infer logic from surrounding code, nearby comments, function names, or filenames.
