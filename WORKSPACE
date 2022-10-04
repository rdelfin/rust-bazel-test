WORKSPACE_NAME = "rust-bazel-test"

workspace(name = WORKSPACE_NAME)

http_archive(
    name = "rules_rust",
    sha256 = "0cc7e6b39e492710b819e00d48f2210ae626b717a3ab96e048c43ab57e61d204",
    urls = [
        "https://github.com/bazelbuild/rules_rust/releases/download/0.10.0/rules_rust-v0.10.0.tar.gz",
    ],
)

http_archive(
    name = "cargo_raze",
    sha256 = "58ecdbae2680b71edc19a0f563cdb73e66c8914689b6edab258c8b90a93b13c7",
    strip_prefix = "cargo-raze-0.15.0",
    url = "https://github.com/google/cargo-raze/archive/refs/tags/v0.15.0.tar.gz",
)

# Rust

load("@rules_rust//rust:repositories.bzl", "rust_repositories", "rust_repository_set")

rust_repositories(
    edition = "2021",
    version = "1.61.0",
)

load("@rules_rust//tools/rust_analyzer:deps.bzl", "rust_analyzer_deps")

rust_analyzer_deps()

"""
# Cargo raze
load("//3rdparty/rust/cargo:crates.bzl", "raze_fetch_remote_crates")

raze_fetch_remote_crates()

load("@cargo_raze//:repositories.bzl", "cargo_raze_repositories")

cargo_raze_repositories()

load("@cargo_raze//:transitive_deps.bzl", "cargo_raze_transitive_deps")

cargo_raze_transitive_deps()
"""
