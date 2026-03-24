# Kreoza Tooling

Centralized, maintainable repository for managing code formatting, linting, and tooling configurations across all Kreoza projects and languages.

## Repository Structure

- `packages/`: NPM packages for shareable configurations.
  - `prettier-config`: Shareable Prettier configuration.
  - `eslint-config`: Shareable ESLint configuration.
  - `stylelint-config`: CSS/SCSS linting.
  - ...
- `.pre-commit-hooks.yaml`: Centralized pre-commit hook definitions.
- `docs/`: Integration and setup guides.

## Quick Start

### For JavaScript/TypeScript projects

1. Install the desired configuration:

   ```bash
   pnpm add -D @kreozalabs/prettier-config @kreozalabs/eslint-config
   ```

2. Reference it in your project:
   - `.prettierrc.js`: `module.exports = require("@kreozalabs/prettier-config");`
   - `.eslintrc.js`: `module.exports = { extends: ["@kreozalabs/eslint-config"] };`

## License

BSD-3-Clause
