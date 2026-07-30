# Task completion

- Scope-check with `rtk git status --short --untracked-files=all` and `rtk git diff -- <touched paths>`; preserve unrelated staged/untracked work.
- For `package.json`/tooling-only edits: parse the manifest, run `rtk proxy mise exec -- pnpm exec oxfmt --check .` and `rtk proxy mise exec -- pnpm exec oxlint .`, then execute the smallest affected direct tool command.
- For Rust edits: `cargo fmt --all -- --check`, `cargo clippy --workspace --all-targets -- -D warnings`, and `cargo test --workspace` unless the task has a narrower justified gate.
- For TypeScript/module edits: typecheck, lint, and relevant Vitest suites only when those source/test entrypoints exist.
- For native/package/release work, also validate the affected binding build, package metadata/artifacts, pack/install smoke path, and release-specific tests; static inspection alone is not release proof.
- Report exact commands run and distinguish passing validation from checks skipped because implementation paths do not exist.
