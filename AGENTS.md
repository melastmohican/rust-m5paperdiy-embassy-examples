# rust-m5paperdiy-embassy-examples

Async twin of `../rust-m5paperdiy-examples`, for the `epdpi` workspace in `../epdpi`. Model it on
`../rust-reterminal-e1002-examples`.

- Own project, never a member of the blocking examples workspace (feature unification would turn
  `epdpi/blocking` back on). Board support in `src/lib.rs` is copied on purpose.
- Build and run from here: `cargo build --release --examples`, `cargo run --release --example X`.
- Checks: `cargo fmt --all -- --check`, `cargo clippy --release --examples --lib -- -D warnings`.
- Blocking is only for start-up work (PMIC I2C). Everything on the bus is `.await`ed.
- Open work lives in `../epdpi/.agents/notes/backlog.md`, queue item 2 and 3.
