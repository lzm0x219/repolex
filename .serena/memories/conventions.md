# Conventions

- Default collaboration language: Chinese; preserve code, command, identifier, and raw error spelling.
- Prefer current checked-in specifications when they exist; do not infer a product contract otherwise.
- Keep the root npm package private, unversioned, and orchestration-only; package-specific ownership belongs under `packages/*` when those workspaces exist.
- Rust formatting follows `rustfmt.toml`; JS/TS/JSON follows Oxfmt and Oxlint configs.
- Preserve unrelated dirty/untracked changes; this checkout can be entirely staged as an initial repository snapshot.
- Do not claim planned capabilities are implemented: distinguish design goal, structural/static evidence, narrow validation, and production support.
- New local issues/specs are created under `docs/spec/`; domain and triage guidance lives under `docs/agents/`.
