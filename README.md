# Embassy STM32F446RE Template

A minimal Embassy project template for the STM32F446RE (Nucleo-F446RE), using async Rust for embedded development.

## What This Is For

This template gets you up and running with [Embassy](https://embassy.dev) on the STM32F446RE as quickly as possible — no fighting with dependency versions or boilerplate. It includes the right `Cargo.toml`, `.cargo/config.toml`, `memory.x`, and `Embed.toml` configuration for the Nucleo-F446RE board out of the box.
## Requirements

### Rust Toolchain

Install [rustup](https://rustup.rs), then add the ARM target:

```bash
rustup target add thumbv7em-none-eabihf
```

### probe-rs

> **Note:** A full flashing and debugging guide using probe-rs will be added here. For now, make sure you install it the right way — **use the prebuilt installer, not `cargo install`**, as building from source takes a very long time and is unnecessary.
> **Note:** Also for installing probe-rs and the target, you're much better off referring to the actual documentation for it, I'll change this to have more details when I go through the toolchain again
**Windows (PowerShell):**
```powershell
irm https://github.com/probe-rs/probe-rs/releases/latest/download/probe-rs-tools-installer.ps1 | iex
```

**Linux / macOS:**
```bash
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/probe-rs/probe-rs/releases/latest/download/probe-rs-tools-installer.sh | sh
```

**Linux only** — after installing, set up udev rules so you can flash without root:
```bash
probe-rs complete install-udev-rules
```

Verify the install worked:
```bash
probe-rs --version
```

## Flashing

```bash
cargo run
```
