# UMG Specification

This directory contains the authoritative specification for Universal Modular Generation (UMG).

All normative definitions of UMG are defined here.

---

## Authority

The contents of this directory are **normative** unless explicitly stated otherwise.

If any conflict exists between:
- documentation in `/docs`
- examples in `/examples`
- schemas or tooling behavior
- reference applications or implementations

the specification in this directory **takes precedence**.

Tooling and documentation must conform to the specification.  
The specification does not conform to tooling.

---

## Scope

The UMG specification defines:

- the Cognitive Specification Layer (CSL)
- Universal Modular Generation as a framework
- block structure and roles
- the Modular Operating Language of Thought (MOLT)
- merge semantics
- synthesis semantics
- priority and governance rules
- compiler resolution requirements
- required output artifacts (RuntimeSpec and Trace)

The specification does **not** define execution, runtime behavior, or learning systems.

UMG specifies **cognitive structure**, not behavior.

---

## Versioning

Specifications are versioned and immutable once published.

The current canonical version is:

```
spec/v0
```

Future revisions will be introduced as new versioned directories.  
Existing versions will not be modified retroactively.

---

## Relationship to Tooling

Reference tooling exists to demonstrate and validate the specification.

Tooling is **not authoritative**.  
Multiple independent implementations are expected.

---

## Reading Guidance (Non-Normative)

There is no required reading order within the specification.

Individual documents may be consulted independently.  
Cross-references are provided where definitions depend on one another.

---

## Status

This specification is released under **research / alpha status**.

Core definitions are considered stable for v0.  
Any changes require explicit version advancement.
