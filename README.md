# Nando Wave Operator Kernel

This package is the small, source-neutral operator kernel extracted from the
Nando Wave project. It gives an agent or runtime a typed place to represent a
bounded operator, canonicalize its identity, and reject malformed or
unbounded programs before execution.

## What it provides

- `CanonicalOperatorIrV1`: origin-neutral typed operator representation.
- canonical JSON and SHA-256 identities that are stable across ordering noise;
- bounded roles, relations, transforms, and composition edges;
- typed response-program contracts and renderer validation;
- fail-closed validation for malformed phases, selectors, private material,
  unbounded output, and invalid control structure;
- deterministic generation and commitment helpers.

The crate is deliberately a kernel, not an LLM and not a complete Wave
machine. It does not learn, call a provider, store private datasets, grant
runtime authority, or claim that a validated structure is a generally capable
model.

## Why this boundary exists

```text
evidence / learning / admission
             |
             v
  CanonicalOperatorIrV1  ->  bounded program contract  ->  independent runtime
```

The kernel owns structure and deterministic validation. Learning, proof
corpora, deployment policy, and authority remain outside it. A caller should
use an explicit verifier and an `ABSTAIN` path before treating any compiled
operator as safe to execute.

## Quick start

```bash
cargo test
cargo clippy --all-targets --all-features -- -D warnings
```

The public API is exposed from the crate root. The module names mirror the
operator concepts: `canonical_operator_ir`, `program`, `contracts`,
`operator_generation`, and `vm`.

## Status

This is an initial public extraction. It preserves the tested kernel behavior
from Nando Wave while keeping the private learner, transition-serving path,
transport credentials, datasets, and runtime admission system out of the
package.
