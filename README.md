# SCL Python SDK (SCL:V1)

This repository contains the **official Python SDK** for SCL:V1.

The SDK provides:
- A reference-correct parser
- Canonical validator
- Canonical runtime engine
- Canonical JSON serialization
- Deterministic golden-hash computation
- Full compliance with the frozen SCL:V1 specification

The Python implementation is mechanically aligned with the Go implementation and must always produce **identical ASTs, runtime results, and hashes**.

## Repository Structure

scl-python/
  src/        # SDK implementation
  tests/      # Conformance & parity tests
  README.md
  LICENSE
  CHANGELOG.md

## Installation

The SDK will be published to PyPI after the public SCL:V1 launch.

For now, use local installation:

pip install -e .

## Guarantees

The Python SDK must:
1. Parse exactly as defined in PARSER_CONTRACT_V1.md
2. Validate exactly as defined in VALIDATION_CONTRACT_V1.md
3. Execute runtime behavior exactly as defined in RUNTIME_CONTRACT_V1.md
4. Produce canonical JSON exactly as defined in CANONICAL_JSON_V1.md
5. Compute golden hashes exactly as defined in ENGINE_V1_CONTRACT.md
6. Match Go and JS SDK outputs bit-for-bit

Any deviation is considered a protocol violation.

## Contributing

See CONTRIBUTING.md in the main spec repository.

## License

See LICENSE for terms.
