# rust-m5paperdiy-embassy-examples

Async (Embassy) hardware examples for the [`epdpi`](https://github.com/melastmohican/epdpi) e-paper
driver on the M5Stack PaperDIY (ESP32-S3, ED047TC1 panel). Structure and dependency versions follow
`rust-reterminal-e1002-examples`.

This is the async twin of `rust-m5paperdiy-examples`. It is a separate project on purpose: `epdpi`
has mutually exclusive blocking and async modes, and Cargo would unify them inside one workspace.

## Run

Needs the `esp` Rust toolchain and `espflash`. `epdpi` is a sibling checkout (`../epdpi`).

```text
cargo run --release --example epdpi_lcd_ramp
```

| Example | What it checks |
| :--- | :--- |
| `epdpi_lcd_ramp` | The `LcdBus` async path: 16-gray `M5Quality` ramp, compare with the blocking example |

## Status

Hardware-tested: nothing yet. The first run of `epdpi_lcd_ramp` is the test for the async `LcdBus`.
