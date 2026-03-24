# JavaScript/TypeScript Integration

Follow these steps to integrate Kreoza's JS/TS standards into your project.

## 1. Install Dependencies

```bash
pnpm add -D @kreozalabs/prettier-config @kreozalabs/eslint-config
```

## 2. Configure Prettier

Create a `.prettierrc.js` file in your root:

```javascript
module.exports = require("@kreozalabs/prettier-config");
```

## 3. Configure ESLint

Create a `.eslintrc.js` file in your root:

```javascript
module.exports = {
  extends: ["@kreozalabs/eslint-config"],
};
```

## 4. (Optional) Configure Stylelint

If your project uses CSS/SCSS:

```bash
pnpm add -D @kreozalabs/stylelint-config
```

Create `.stylelintrc.js`:

```javascript
module.exports = {
  extends: ["@kreozalabs/stylelint-config"],
};
```
