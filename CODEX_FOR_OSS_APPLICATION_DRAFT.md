# Codex for Open Source application draft

Status: draft only. This document has not been submitted to OpenAI.

## Repository

Proposed public repository:

```text
https://github.com/radislabus-star/nando-wave-operator-kernel
```

## Maintainer role

Primary maintainer and author of the Nando Wave operator-kernel extraction.

## Why this project matters

Nando Wave explores a practical boundary between adaptive systems and
deterministic execution. This public kernel makes one reusable part of that
work available independently: typed operator structures, canonical identities,
bounded program contracts, and fail-closed validation. It is useful for agent
runtimes that need to keep learned or generated operators separate from
execution authority.

The package intentionally does not claim to be a general language model. It
does not contain private datasets, provider credentials, or a production
authority path.

## Intended use of API credits

API credits would support:

- public documentation and examples;
- compatibility tests against real agent workflows;
- pull-request review and release automation;
- independent verifier and held-out evaluation work;
- maintaining a small public reference runtime around the kernel.

The credits would not be used to turn proof fixtures into runtime authority or
to make unsupported claims about general intelligence.

## Evidence and limits

- the extracted kernel passes 25 unit tests from the source project;
- canonical identities are deterministic and order-stable;
- malformed, unbounded, private, and tampered structures fail closed;
- learning, datasets, deployment admission, and provider routing remain
  outside this package.

Repository adoption, stars, and downloads must be filled from the public
repository after publication. No adoption number is claimed in this draft.
