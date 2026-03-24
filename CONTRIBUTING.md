# Contributing to Kreoza Tooling

Thank you for helping maintain our standards!

## Proposing Rule Changes

1. Open an issue to discuss the proposed change.
2. Provide rationale: Why is this change necessary? What problem does it solve?
3. Provide examples of code before and after the change.

## Adding Support for a New Language

1. Create a new directory under `packages/` (e.g., `rust-standards`).
2. Add the relevant configuration files (e.g., `rustfmt.toml`).
3. Add a pre-commit hook definition in `.pre-commit-hooks.yaml`.
4. Add an integration guide in `docs/integration/`.

## Development

We use **pnpm workspaces** and **Turborepo**.

```bash
pnpm install
pnpm run lint
```
