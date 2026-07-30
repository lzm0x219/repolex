# Repository Guidelines

Repolex is a Rust and TypeScript monorepo for repository language analysis. Checked-in specifications define contracts; planned code does not.

## Project structure and module organization

- `crates/repolex/`: Rust workspace crate; library code starts in `src/lib.rs`
- `packages/`: reserved for pnpm workspace packages; no TypeScript package exists yet
- `docs/`: documentation and contributor conventions
- `docs/spec/`: local issue and specification records, created when the first item is added

Do not commit generated directories such as `target/`, `node_modules/`, or `.pnpm-store/`.

## Build, test, and development commands

Node tooling runs through `mise`; Rust follows `rust-toolchain.toml`. Agent shells prefix commands with `rtk`.

- `rtk proxy mise exec -- pnpm install`: install JavaScript tooling and Git hooks
- `rtk cargo fmt --all -- --check`: verify Rust formatting
- `rtk cargo clippy --workspace --all-targets -- -D warnings`: lint all Rust targets
- `rtk cargo test --workspace`: run Rust tests
- `rtk proxy mise exec -- pnpm exec oxfmt --check .`: check JavaScript, TypeScript, and JSON formatting
- `rtk proxy mise exec -- pnpm exec oxlint .`: lint JavaScript and TypeScript

## Coding style and naming conventions

Use UTF-8, LF endings, final newlines, and spaces. Indent Rust with four spaces and other files with two. Let `rustfmt` and `oxfmt` decide layout. Use Rust-standard `snake_case` and `PascalCase` names.

## Testing guidelines

Place Rust unit tests beside implementations and integration tests in `crates/repolex/tests/`. Name future TypeScript tests `*.test.ts`. Add regression tests for fixes. No coverage threshold exists.

## Commit and pull request guidelines

The current `main` branch has no commit history. Use short imperative subjects, optionally scoped, such as `docs: define issue workflow`. Pull requests should explain intent, list validation, link the relevant `docs/spec/` item, and identify skipped checks.

## Agent skills

Use the smallest applicable skill set and read each `SKILL.md` before acting.

- `rust-skills`: required for Rust implementation and review
- `domain-modeling` and `codebase-design`: specifications, domain language, APIs, and module boundaries
- `dsa-design`: substantive algorithm or data-structure choices
- `diagnosing-bugs`: complex defects and performance regressions
- `napi-rs`: native Node.js bindings, once that crate exists
- `pnpm`, `typescript-pro`, `tsdown`, and `vitest`: TypeScript package, build, or test work
- `tdd`: requested test-first work; `code-review`: review-only tasks

Do not invoke conditional skills for paths or product surfaces that do not exist.

## Specifications and agent workflow

Read [README.md](README.md) and [docs/README.md](docs/README.md) first. Follow `docs/agents/` and preserve unrelated dirty-worktree changes.
