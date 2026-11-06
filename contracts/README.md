# Credence Smart Contracts

Soroban smart contracts powering the decentralized Buy Now Pay Later (BNPL) protocol on the Stellar Network, built with Rust and Soroban SDK v22.

## Structure

```text
contracts/
├── adapter-trustless-contract/     # Adapter contract for trustless protocol interactions
├── creditline-contract/            # Core credit line logic, loan lifecycle, repayments
├── liquidity-pool-contract/        # Liquidity pool, LP shares, deposits & withdrawals
├── merchant-registry-contract/     # Merchant registration, status and metadata
├── parameters-contract/            # Protocol parameters & governance emergency pause
├── reputation-contract/            # User credit/reputation score tracking
└── tests/
    └── integration/                # Cross-contract integration tests
```

## Building

Build the Rust workspace from repo root:
```bash
cargo check --workspace
```

Build individual contracts for Wasm target:
```bash
cargo build --package reputation-contract --target wasm32-unknown-unknown
cargo build --package creditline-contract --target wasm32-unknown-unknown
cargo build --package liquidity-pool-contract --target wasm32-unknown-unknown
cargo build --package merchant-registry-contract --target wasm32-unknown-unknown
cargo build --package parameters-contract --target wasm32-unknown-unknown
cargo build --package adapter-trustless-contract --target wasm32-unknown-unknown
```

## Testing

Run workspace checks and tests:
```bash
cargo check --workspace
cargo test --workspace
```
