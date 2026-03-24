# Go Integration

Go standards at Kreoza rely on `gofmt` and `golangci-lint`.

## 1. Using Golangci-lint

Copy the standard configuration from the tooling repo or reference it:

```bash
curl -O https://raw.githubusercontent.com/kreozalabs/tooling/main/packages/go-standards/.golangci.yml
```

## 2. Using Pre-commit

Add the following to your `.pre-commit-config.yaml`:

```yaml
repos:
  - repo: https://github.com/kreozalabs/tooling
    rev: v1.0.0
    hooks:
      - id: kreoza-gofmt
```
