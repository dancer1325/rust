## how to compile EACH example?

* `rustup component add rustc-dev llvm-tools`
* `rustup run nightly rustc <FILE_NAME_HERE>.rs` OR `rustup run nightly-<SPECIFIED_VERSION> rustc <FILE_NAME_HERE>.rs`
  * _Example:_ `rustup run nightly rustc rustc-driver-example.rs` OR `rustup run nightly-2025-03-28 rustc rustc-driver-example.rs`

## how to run an executable?

* [compile](#how-to-compile-each-example)
* `rustup run nightly ./<FILE_NAME>`
  * _Example._ `rustup run nightly ./rustc-driver-example`
