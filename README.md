# Repolex

Repolex is a repository language statistics engine built around a Rust core. Developer tools will use it to identify the languages in a source tree and measure how much content belongs to each one.

> [!WARNING]
> This checkout is the rewrite baseline. It has no business implementation or runnable product. This README describes the direction of the project, not a frozen contract.

## What Repolex is for

Repolex is meant to be embedded in other tools. Its Rust core will define language detection and statistics, with adapters for Rust applications, Node.js packages, command-line tools, and automation. The same data model should cover local working trees and Git revisions, and callers will receive structured results rather than a presentation-only report.

Repolex is not a hosted repository service, code search engine, semantic index, compiler, linter, or formatter. It is not ready to replace an existing language statistics tool.

## Repository status

The workspace contains an empty Rust library crate with no third-party dependencies. The formatters, linters, tests, hooks, and Rust and TypeScript workspace configuration are already in place for the rewrite.

There is no frozen public API, command-line interface, package graph, compatibility target, or release commitment. Add an approved specification under `docs/spec/` before treating any of those decisions as a contract.

## Documentation

The [documentation index](docs/README.md) lists the available project and contributor documentation.

The old implementation is available on the local branch `archive/pre-rewrite-2026-07-31` at commit `3e575c0`.

## Check the workspace

The product does not run yet, but the Rust workspace does. Check it with:

```bash
cargo fmt --all -- --check
cargo clippy --workspace --all-targets -- -D warnings
cargo test --workspace
```

## License

[MIT](LICENSE)
