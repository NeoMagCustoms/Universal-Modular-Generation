# Current Sleeve Authoring Contract

This document defines the authoring boundary for current compiler-vNext v0.1 Sleeves.

## Authoring flow

```text
Purpose / design intent
        ↓
select or author real Blocks
        ↓
construct NeoBlocks
        ↓
construct NeoStacks
        ↓
construct Sleeve topology
        ↓
create separate explicit Selection
        ↓
schema validation
        ↓
compiler-vNext validation
        ↓
compile
        ↓
RuntimeSpec + Trace + diagnostics
```

## Core rules

1. Inspect the current compiler-vNext schema before authoring.
2. Use the seven current MOLT lanes only: Trigger, Directive, Instruction, Subject, Primary, Philosophy, Blueprint.
3. Preserve exact canonical IDs when using canonical library assets.
4. Do not fabricate canonical IDs.
5. Keep Sleeve and Selection as separate artifacts.
6. Do not infer natural-language intent inside the compiler.
7. Do not claim ACTIVE / READY / OFF / DISABLED until compilation establishes resolved state.
8. Do not silently migrate legacy compiler-v0 fields into vNext.
9. Canonical library sources are read-only by default.
10. Generated or experimental assets remain candidates until explicitly reviewed and promoted.

## What does not make a Sleeve current or valid

A Sleeve is not compiler-valid merely because:

- it is JSON;
- a Website or Studio renders it;
- Hermes or OpenClaw can describe it;
- an MCP search returns its blocks;
- an LLM generated it;
- a historical v0 application used it.

Current compatibility requires validation against the current vNext contract.

## Legacy concepts not to insert automatically

Do not add these merely because historical UMG software used them:

- Priority / weights
- PrimaryShell
- Persona as MOLT lane #8
- Language as a MOLT lane
- automatic routing from prose
- compiler-v0-only fields

## Approved package direction

Reusable approved Sleeves should eventually be packaged with explicit provenance:

```text
SLV.<ID>/
├── sleeve.json
├── manifest.json
├── README.md
├── selections/
│   ├── default.selection.json
│   └── examples...
└── tests/
    └── qualification evidence
```

The package manifest should record the Sleeve identity/version, compiler identity, schema versions, library revision/provenance, qualification status, and known compatible consumers.

