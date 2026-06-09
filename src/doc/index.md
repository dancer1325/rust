* goal
  * "The Rust Bookshelf" 

* if you want to open LOCALLY the documentation ->  `rustup doc`

## Learning Rust

If you'd like to learn Rust, this is the section for you! All of these resources
assume that you have programmed before, but not in any specific language:

### The Rust Programming Language

Affectionately nicknamed "the book," [The Rust Programming Language](book/index.html)
will give you an overview of the language from first principles. You'll build a
few projects along the way, and by the end, you'll have a solid grasp of how to
use the language.

### Rust By Example

If reading multiple hundreds of pages about a language isn't your style, then
[Rust By Example](rust-by-example/index.html) has you covered. RBE shows off a
bunch of code without using a lot of words. It also includes exercises!

### Rustlings

[Rustlings](https://github.com/rust-lang/rustlings) guides you
through downloading and setting up the Rust toolchain, then provides an
interactive tool that teaches you how to solve coding challenges in Rust.

### Rust Playground

The [Rust Playground](https://play.rust-lang.org) is a great place
to try out and share small bits of code, or experiment with some of the most
popular crates.


## how to use Rust?

### Standard Library

* [here](/library/std/src/lib.md)

### Your Personal Documentation

* | work | crate,
  * `cargo doc --open`
    * generate documentation -- for -- 
      * your project 
      * your project's dependencies
    * if you want to show items / NOT marked as `pub` -> pass the flag `--document-private-items`

### Rust Version History

* [Release Notes](/RELEASES.md)
* [Edition Guide](/src/doc/edition-guide)

### The `rustc` Book

* [here](rustc/src/what-is-rustc.md)

### The Cargo Book

[The Cargo Book](cargo/index.html) is a guide to Cargo, Rust's build tool and
dependency manager.

### The Rustdoc Book

[The Rustdoc Book](rustdoc/index.html) describes our documentation tool, `rustdoc`.

### The Clippy Book

[The Clippy Book](clippy/index.html) describes our static analyzer, Clippy.

### Extended Error Listing

Many of Rust's errors come with error codes, and you can request extended
diagnostics from the compiler on those errors (with `rustc --explain`). You can
also read them here if you prefer: [rustc error codes](error_codes/index.html)


## Mastering Rust

Once you're quite familiar with the language, you may find these advanced
resources useful.

### The Reference

[The Reference](reference/index.html) is not a formal spec, but is more detailed
and comprehensive than the book.

### The Style Guide

[The Rust Style Guide](style-guide/index.html) describes the standard formatting
of Rust code. Most developers use `cargo fmt` to invoke `rustfmt` and format the
code automatically (the result matches this style guide).

### The Rustonomicon

[The Rustonomicon](nomicon/index.html) is your guidebook to the dark arts of
unsafe Rust. It's also sometimes called "the 'nomicon."

### The Unstable Book

[The Unstable Book](unstable-book/index.html) has documentation for unstable
features.

### The `rustc` Development Guide

[The `rustc-dev-guide`](https://rustc-dev-guide.rust-lang.org/)
documents how the compiler works and how to contribute to it. This is useful if
you want to build or modify the Rust compiler from source (e.g. to target
something non-standard).


## Specialized Rust

When using Rust in specific domains, consider using the following resources
tailored to each area.

### Embedded Systems

When developing for Bare Metal or Embedded Linux systems, you may find these
resources maintained by the [Embedded Working Group] useful.

[Embedded Working Group]: https://github.com/rust-embedded

#### The Embedded Rust Book

[The Embedded Rust Book] is targeted at developers who are familiar with embedded
development and Rust, but who have not used Rust for embedded development.

[The Embedded Rust Book]: embedded-book/index.html
[Rust project]: https://www.rust-lang.org

<script>
// check if a given link is external
function isExternalLink(url) {
  const tmp = document.createElement('a');
  tmp.href = url;
  return tmp.host !== window.location.host;
}

// Add the `external` class to all <a> tags with external links and append the external link SVG
function updateExternalAnchors() {
  /*
    External link SVG from Font-Awesome
    CC BY-SA 3.0 https://creativecommons.org/licenses/by-sa/3.0
    via Wikimedia Commons
  */
  const svgText = `<svg
     class='external-link'
     xmlns='http://www.w3.org/2000/svg'
     viewBox='0 -256 1850 1850'
     width='100%'
     height='100%'>
       <g transform='matrix(1,0,0,-1,30,1427)'>
         <path d='M 1408,608 V 288 Q 1408,169 1323.5,84.5 1239,0 1120,
           0 H 288 Q 169,0 84.5,84.5 0,169 0,288 v 832 Q 0,1239 84.5,1323.5 169,
           1408 288,1408 h 704 q 14,0 23,-9 9,-9 9,-23 v -64 q 0,-14 -9,-23 -9,
           -9 -23,-9 H 288 q -66,0 -113,-47 -47,-47 -47,-113 V 288 q 0,-66 47,
           -113 47,-47 113,-47 h 832 q 66,0 113,47 47,47 47,113 v 320 q 0,14 9,
           23 9,9 23,9 h 64 q 14,0 23,-9 9,-9 9,-23 z m 384,864 V 960 q 0,
           -26 -19,-45 -19,-19 -45,-19 -26,0 -45,19 L 1507,1091 855,439 q -10,
           -10 -23,-10 -13,0 -23,10 L 695,553 q -10,10 -10,23 0,13 10,23 l 652,
           652 -176,176 q -19,19 -19,45 0,26 19,45 19,19 45,19 h 512 q 26,0 45,
           -19 19,-19 19,-45 z' style='fill:currentColor' />
         </g>
     </svg>`;
  let allAnchors = document.getElementsByTagName("a");

  for (var i = 0; i < allAnchors.length; ++i) {
    let anchor = allAnchors[i];
    if (isExternalLink(anchor.href)) {
      anchor.classList.add("external");
      anchor.innerHTML += svgText;
    }
  }
}

// on page load, update external anchors
document.addEventListener("DOMContentLoaded", updateExternalAnchors);

</script>
