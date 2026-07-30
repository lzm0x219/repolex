# Repolex core

- Product state: zero-implementation rewrite baseline; it is not a runnable product and has no frozen product specification.
- Documentation truth order: `README.md` → `docs/README.md` → a specific checked-in specification when one exists.
- Do not infer future product behavior, package layout, or public APIs from the historical archive or scaffold shape.
- Virtual Cargo workspace root: `Cargo.toml`; current library crate: `crates/repolex`.
- Private JS root is tooling-only and never published; no package workspace currently exists.
- Agent workflow and local issue/domain conventions: `AGENTS.md`, `docs/agents/`.
- Toolchain details: `mem:tech_stack`; task commands: `mem:suggested_commands`; completion gates: `mem:task_completion`; conventions: `mem:conventions`.
