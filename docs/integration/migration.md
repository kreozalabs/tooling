# Migration Guide

If your project currently has its own formatting/linting configurations, follow these steps to migrate to the centralized `tooling` repository.

## 1. Remove Local Configs

Delete existing configurations to avoid conflicts:

```bash
rm .prettierrc .eslintrc.js .stylelintrc.json
```

## 2. Update dependencies

Ensure you don't have conflicting versions of formatters/linters in your `package.json`. It's recommended to let the shared configs manage their own sub-dependencies where possible.

## 3. Follow Integration Guides

Refer to the language-specific integration guides:

- [JavaScript/TypeScript](javascript.md)
- [Go](go.md)
- [Python](python.md)

## 4. Set up Pre-commit

If you don't have `pre-commit` installed, install it:

```bash
pip install pre-commit
# or
brew install pre-commit
```

Then create/update `.pre-commit-config.yaml` as per the [template](../../examples/.pre-commit-config.yaml).
Run `pre-commit install` to set up the git hooks.
