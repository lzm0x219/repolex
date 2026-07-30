# Suggested commands

- Use `rtk` before shell commands per `AGENTS.md`; prefix every segment in command chains.
- Install JS dependencies and hooks: `rtk proxy mise exec -- pnpm install`.
- Check JS/TS/JSON formatting: `rtk proxy mise exec -- pnpm exec oxfmt --check .`.
- Format JS/TS/JSON: `rtk proxy mise exec -- pnpm exec oxfmt .`.
- Lint JS/TS: `rtk proxy mise exec -- pnpm exec oxlint .`.
- Check Rust formatting: `rtk cargo fmt --all -- --check`.
- Lint Rust: `rtk cargo clippy --workspace --all-targets -- -D warnings`.
- Test Rust: `rtk cargo test --workspace`.
- Install hooks manually: `rtk proxy mise exec -- pnpm exec lefthook install`.
- Run the configured hook: `rtk proxy mise exec -- pnpm exec lefthook run pre-commit`.
- TypeScript and Vitest entrypoints are intentionally absent until package workspaces exist.
