# Library Provenance and Canonical Assets

UMG must distinguish reusable block/component libraries from complete compiler-valid Sleeve libraries.

## Canonical library layers

```text
UMG LIBRARIES
│
├── MOLT BLOCK LIBRARY
│   └── reusable typed MOLT Blocks
│
├── COMPONENT LIBRARY
│   ├── NeoBlocks
│   └── NeoStacks
│
├── SLEEVE LIBRARY
│   └── complete compiler-valid versioned Sleeve packages
│
└── EXPERIMENTAL LIBRARY
    ├── candidate blocks
    ├── Persona research
    ├── DSG research
    └── unqualified Sleeves
```

## Provenance rule

No directory, corpus, Website dataset, MCP registry, or application-local store becomes canonical solely because it contains many UMG assets.

Canonical status requires:

- explicit source identity;
- version/revision identity;
- stable IDs;
- provenance preservation;
- current MOLT taxonomy compatibility;
- compiler-vNext compatibility where applicable;
- review/promotion status.

## Current evidence

Existing UMG work includes multiple overlapping asset sources, including historical Resleever content, MCP corpora, Website datasets, application-local Envoy content, and a dedicated UMG Block Library candidate.

These must be inventoried and crosswalked before any one is declared the canonical current library.

The later compiler-vNext composition audit also established that a component catalog alone does not supply all Sleeve-specific topology needed to materialize arbitrary compiler-valid Sleeves.

Therefore:

**Block Library != Sleeve Library.**

## Write policy

Canonical libraries are read-only by default.

New or modified assets enter as candidates:

```text
candidate
  ↓
review
  ↓
schema validation
  ↓
compiler validation
  ↓
qualification/package checks
  ↓
approved canonical revision
```

Model-generated or agent-generated assets must not be written directly into canonical libraries without explicit promotion authority.

## Mirrors and Websites

Website and application datasets should become generated or synchronized projections of canonical versioned sources whenever practical.

Mirrors must record their upstream source/revision so consumers can detect drift.

