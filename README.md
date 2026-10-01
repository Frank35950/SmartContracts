# pi-smartcontracts

Soroban smart contracts for the Pi Network. The workspace currently contains a recurring paid-subscription contract under `contracts/subscription`.

## Workspace

- `contracts/subscription/src/lib.rs` — subscription contract implementation
- `contracts/subscription/src/test.rs` — Soroban unit tests
- `contracts/subscription/README.md` — contract API and storage documentation

## Development

```bash
cargo test --workspace
cargo fmt --all -- --check
cargo clippy --workspace --all-targets -- -D warnings
```

The contract uses Soroban SDK 22 and the Stellar token `approve`/`transfer_from` flow for recurring charges.

## Security status

This repository is experimental and has not undergone an independent audit. Do not deploy with production funds without reviewing the contract, its configured token contract, upgrade authority, storage TTL behavior, and the complete test suite.

See [SECURITY.md](SECURITY.md) for vulnerability reporting and deployment requirements.
