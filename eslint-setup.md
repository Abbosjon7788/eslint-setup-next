!!! Eslint and Prettier extensions should be installed in your vs code !!!

1. npx create-next-app@latest your_app_name (without typescript)
2. npx eslint --init
3. your custom .eslint.json like this

```
{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": [
    "eslint:recommended",
    "plugin:react/recommended",
    "prettier",
    "next/core-web-vitals"
  ],
  "overrides": [],
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": ["react", "prettier"],
  "rules": {
    "react/react-in-jsx-scope": "off",
    "react/prop-types": "off",
    "react/jsx-props-no-spreading": "off",
    "react/display-name": "off",
    "no-unused-vars": "warn",
    "no-console": "warn",
    "prefer-const": "warn",
    "semi": ["warn", "always"],
    "quotes": ["warn", "single"],
    "jsx-quotes": ["warn", "prefer-double"]
  }
}

```

4. Install prettier eslint-config-prettier eslint-plugin-prettier --save-dev
