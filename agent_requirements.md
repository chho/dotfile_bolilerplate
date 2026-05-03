# Requirements

## Tech Stack

- Rust binary crate, edition 2024
- Async runtime: tokio
- Ethereum interaction: alloy (full features)
- Error handling: eyre
- Logging: `tracing` + `tracing-subscriber` (env-filter), NOT the `log` crate
- Default log level: `base_gun=debug`, overridable via `RUST_LOG`

## Project Structure

- Single-file entrypoint: `src/main.rs`
- Target: DEX arbitrage bot on Base chain

## Code Style

1. Write short, precise English comments only where needed
2. Test-driven development: all code must be designed for testability; every feature requires unit and integration tests
3. Each function does one thing only; keep functions under 50 lines
4. Extract hardcoded strings and magic values into named constants
5. Avoid unnecessary `.clone()` and `.wrap()`. Prefer references, lifetimes, `Arc`, `Cow`, or restructuring ownership

## Logging

- Add structured logging at critical points. Use appropriate levels:
  - `error!` — unrecoverable failures (e.g. transaction reverted, connection lost)
  - `warn!` — recoverable issues or unexpected states (e.g. retryable RPC error, price impact too high)
  - `info!` — key business events (e.g. arbitrage opportunity found, trade executed, profit summary)
  - `debug!` — diagnostic details (e.g. price diffs, route evaluation steps, intermediate balances)
  - `trace!` — verbose internals only needed during deep debugging

## Workflow

1. When given a new requirement, carefully analyze it and evaluate whether the existing project design aligns with it
2. If a better design exists to accommodate the new requirement, explicitly call it out and suggest the alternative before proceeding with implementation
