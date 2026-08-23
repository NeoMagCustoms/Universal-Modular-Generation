# Historical UMG Specification Archive

The material under `/spec/v0` is retained as a historical UMG specification generation.

It predates the H4-qualified compiler-vNext v0.1 freeze and includes concepts that are not current compiler-vNext semantics, including legacy Priority-era assumptions.

## Current authority

For current UMG work, start with:

- [`/CANON.md`](../CANON.md)
- [`/docs/current/COMPILER.md`](../docs/current/COMPILER.md)
- [`/docs/current/SLEEVE_AUTHORING.md`](../docs/current/SLEEVE_AUTHORING.md)

Current compiler authority:

- compiler-vNext v0.1.0-experimental
- H4 commit `c505f9a7f23010574733c8c03c4162af5317a5eb`
- tag `compiler-vnext-v0.1.0-experimental-h4-qualified`
- repository `https://github.com/NeoMagnetar/umg-compiler-vnext`

## Historical preservation rule

Files under `/spec/v0` are preserved for provenance, migration research, and the history of UMG's development.

Do not silently rewrite those historical documents to look like compiler-vNext. When concepts from `/spec/v0` conflict with current H4 compiler-vNext contracts, the historical material does not govern current compilation.

Future formal UMG specification work should use a new explicitly versioned current-spec location and must state its relationship to the frozen compiler contract rather than retroactively changing `/spec/v0`.
