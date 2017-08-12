rlibc
=====

A bare minimum "libc" for Rust crates that do not want to rely on libc itself.
This crate provides functions which LLVM often lowers intrinsic calls to and
will be required to link correctly.

## Usage

Add this to your git submodules:
```
git submodule add https://github.com/Restioson/rlibc.git
```

Add this to your `Cargo.toml`:

```toml
[dependencies]

rlibc = { path = "rlibc/" }
```

And add this to your crate root:

```rust
extern crate rlibc;
```

Make sure you have a `core` crate in `../libcore`.

---

This fork make `rlibc` depend on an external `core` crate in `../libcore`. Forked for use with AVR-Rust.
