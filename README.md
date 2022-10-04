# Rust Bazel Test

This repo is a minimal reproducible example of google/cargo-raze#530.

## Reproduce

To reproduce, run:

```
$ cd 3rdparty/rust/cargo
$ cargo raze
thread 'main' panicked at 'assertion failed: tree_output.status.success()', /home/rdelfin/.cargo/registry/src/github.com-1ecc6299db9ec823/cargo-raze-0.16.0/src/features.rs:149:3
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
```

You should see the error above.
