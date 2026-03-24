# Kreoza Tooling

Centralized, maintainable repository for managing code formatting, linting, and tooling configurations across all Kreoza projects and languages.

## Repository Structure

- `packages/`: NPM packages and standards for shareable configurations.
  - `prettier-config`: Shareable Prettier configuration.
  - `eslint-config`: Shareable ESLint configuration.
  - `stylelint-config`: CSS/SCSS linting.
  - `go-standards`: Go formatting & linting rules.
  - `python-standards`: Python (Ruff) configuration.
- `.pre-commit-hooks.yaml`: Centralized pre-commit hook definitions.
- `docs/`: Integration and setup guides.

## Quick Start

Detailed setup guides are available in the [docs/integration/](./docs/integration/) directory.

### JavaScript/TypeScript
Install the desired configuration:
```bash
pnpm add -D @kreozalabs/prettier-config @kreozalabs/eslint-config
```
See [JS/TS Integration Guide](./docs/integration/javascript.md) for configuration details.

### Go
We use `gofmt` and `golangci-lint`. See [Go Integration Guide](./docs/integration/go.md) for the standard `.golangci.yml`.

### Python
We use **Ruff** for formatting and linting. See [Python Integration Guide](./docs/integration/python.md) for the standard `ruff.toml`.

## Universal Integration (Pre-commit)

The recommended way to apply these standards across any project is via **pre-commit**.

Add a `.pre-commit-config.yaml` to your project:
```yaml
repos:
  - repo: https://github.com/kreozalabs/tooling
    rev: v1.0.0
    hooks:
      - id: kreoza-prettier
      - id: kreoza-ruff
      - id: kreoza-gofmt
```

See [Migration & Setup Guide](./docs/integration/migration.md) for more details.

## License

BSD-3-Clause
