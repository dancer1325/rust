# src/etc/

TODO: 
Miscellaneous utilities, configs, and support files for developing and distributing Rust.

## Debugger support

- `rust-gdb`, `rust-lldb`, `rust-gdbgui` — wrapper scripts that launch GDB/LLDB with Rust pretty-printers preloaded
- `gdb_providers.py`, `gdb_lookup.py`, `gdb_load_rust_pretty_printers.py` — GDB pretty-printers for Rust types (Vec, HashMap, String, etc.)
- `lldb_providers.py`, `lldb_lookup.py` — LLDB pretty-printers for Rust types
- `lldb_batchmode/` — LLDB batch-mode runner for testing
- `natvis/` — Visual Studio / WinDbg visualizers (.natvis files)
- `rust-windbg.cmd` — WinDbg launcher with Rust natvis loaded
- `rust_types.py` — shared type definitions used by the debugger scripts

## Editor / rust-analyzer configs

- `rust_analyzer_settings.json` — recommended rust-analyzer settings for VS Code
- `rust_analyzer_zed.json` — rust-analyzer settings for Zed
- `rust_analyzer_helix.toml` — rust-analyzer settings for Helix
- `rust_analyzer_eglot.el` — rust-analyzer settings for Emacs (eglot)
- `ctags.rust` — ctags definitions for Rust

## Shell completions

- `completions/` — tab-completion scripts for the `x.py` / `x` build system (bash, zsh, fish, PowerShell)

## Scripts and utilities

- `htmldocck.py` — checks generated rustdoc HTML against expected patterns (used in tests)
- `generate-keyword-tests.py` — generates test files for Rust keywords
- `dec2flt_table.py` — generates lookup tables for decimal-to-float conversion
- `cpu-usage-over-time-plot.sh` — plots CPU usage from CI logs
- `cat-and-grep.sh` — helper for CI test scripts
- `pre-push.sh` — git pre-push hook for contributors
- `indenter` — helper script for indenting output
- `xhelp` — help text for the `x.py` build system options

## Installer resources

- `installer/` — assets for building .pkg (macOS) and .msi (Windows) installers
- `third-party/` — third-party license files (GCC runtime library)

## See also

- [CONFIGS.md](CONFIGS.md) — links to officially maintained editor plugin repos
