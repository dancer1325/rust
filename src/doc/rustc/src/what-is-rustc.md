# What is rustc?

* `rustc`
  * == Rust programming language's compiler
    * provided by 
      * Rust project itself
    * produce from your source code -- a binary code / as
      * library
      * executable
  * 👀ways to use it👀
    * DIRECTLY -- through -- `rustc`
      * use cases
        * you ALREADY use ANOTHER build system
          * _Examples:_ Bazel, CMake, ...
    * -- through -- [Cargo](https://github.com/dancer1325/rust-cargo)
      * if you want to debug it -> `cargo build --verbose`

## Basic usage

TODO: 
Note that we only ever pass `rustc` the *crate root*, not every file we wish
to compile
* For example, if we had a `main.rs` that looked like this:

```rust,ignore (needs-multiple-files)
mod foo;

fn main() {
    foo::hello();
}
```

And a `foo.rs` that had this:

```rust,no_run
pub fn hello() {
    println!("Hello, world!");
}
```

To compile this, we'd run this command:

```bash
$ rustc main.rs
```

No need to tell `rustc` about `foo.rs`; the `mod` statements give it
everything that it needs
* This is different than how you would use a C
compiler, where you invoke the compiler on each file, and then link
everything together
* In other words, the *crate* is a translation unit, not a
particular module.
