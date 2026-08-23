# Legacy UMG Migration Guidance

This document prevents historical UMG/compiler-v0 semantics from being mistaken for current compiler-vNext canon.

## Retired compiler

`NeoMagCustoms/umg-compiler` / compiler-v0 is retained for provenance and historical comparison only.

Do not target it for new UMG Sleeve development or new platform integrations.

## Common legacy concepts

### Priority / weights

Legacy compiler-v0 and older applications used Priority-style concepts.

Current compiler-vNext v0.1 does not use legacy numeric Priority/weight semantics as compiler authority.

Do not translate old Priority fields into new semantics by guesswork.

### PrimaryShell

PrimaryShell is a historical/application concept and is not a current compiler-vNext v0.1 primitive.

### Persona lane #8

Some historical MCP/library generations represented Persona as a base lane/type.

Current compiler-vNext has seven MOLT lanes only. Persona may be modeled as an extension/application concept but is not lane #8.

### Legacy Sleeve JSON

Historical Sleeves may contain fields such as `priorityOrder`, `primary_shell_block_id`, old compiler profiles, or application-specific adapter metadata.

Do not call them vNext-compatible until they are explicitly migrated and validated.

## Migration policy

A legacy asset should be handled as:

```text
legacy source
   ↓
read-only audit
   ↓
field/semantic crosswalk
   ↓
explicit migration proposal
   ↓
new candidate vNext asset
   ↓
schema validation
   ↓
compiler validation
   ↓
review and qualification
```

The original historical file remains preserved.

## Consumer migration

If Hermes, OpenClaw/Envoy, MCP, Studio, or another application expects compiler-v0 behavior, migrate or replace the consumer adapter. Do not alter frozen compiler-vNext semantics merely to preserve the old consumer behavior.

