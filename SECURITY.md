# Security policy

## Scope

The Soroban contracts under `contracts/` are in scope. Please include the contract name, commit or deployed WASM hash, network, affected entry point, and a minimal reproduction when reporting a vulnerability.

## Reporting

Do not disclose an exploitable vulnerability in a public issue. Contact the repository maintainer privately through GitHub and encrypt sensitive details where possible. Do not include private keys, seed phrases, or real user data in a report.

## Deployment requirements

Before deploying or upgrading the contract:

- run `cargo test --workspace` and `cargo clippy --workspace --all-targets -- -D warnings`;
- review the configured token contract and its authorization behavior;
- verify the admin and upgrade authority independently;
- test allowance expiry and short billing periods on the target network;
- review every upgrade as a state/schema migration and preserve authorization checks;
- use a separate deployment/admin account from ordinary merchant accounts.

The contract is experimental and has no guarantee of fitness for production use.
