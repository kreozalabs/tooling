# Python Integration

We use **Ruff** for formatting and linting Python code.

## 1. Using Ruff

Copy the standard configuration:

```bash
curl -O https://raw.githubusercontent.com/kreozalabs/tooling/main/packages/python-standards/ruff.toml
```

## 2. Using Pre-commit

Add the following to your `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/kreozalabs/tooling
    rev: v1.0.0
    hooks:
      - id: kreoza-ruff
```
