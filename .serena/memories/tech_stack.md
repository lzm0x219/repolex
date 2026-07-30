# Tech stack

- Rust 2024 virtual workspace; toolchain pin in `rust-toolchain.toml`; formatting policy in `rustfmt.toml`.
- Node/pnpm private monorepo root; package manager pin is the `packageManager` field in `package.json`; workspace/catalog in `pnpm-workspace.yaml` and `pnpm-lock.yaml`.
- TypeScript ESM tooling; root solution/config files are `tsconfig.json` and `tsconfig.tooling.json`.
- JS/JSON formatting: Oxfmt (`.oxfmtrc.json`); linting: Oxlint (`.oxlintrc.json`).
- Tests/tooling dependencies may precede implementation files in this scaffold; check file existence before assuming an entrypoint is usable.
- Git hooks: Lefthook configured by `lefthook.yml`.
