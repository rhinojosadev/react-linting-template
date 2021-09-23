# react-linting-template

The use of these steps are intended to create an initial approach to have linting for a react typescript project. 

1. Install the following dev dependencies:
```
yarn add -D concurrently eslint eslint-config-airbnb eslint-config-airbnb-typescript eslint-config-prettier eslint-plugin-flowtype eslint-plugin-import 
```
```
yarn add -D eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks @typescript-eslint/eslint-plugin @typescript-eslint/parser prettier
```
2. Create a file in the root folder with the name .eslintrc.js 

```
module.exports = {
  env: {
    browser: true,
    commonjs: true,
    es6: true,
    node: true,
  },
  parser: '@typescript-eslint/parser',
  extends: ['airbnb-typescript'],
  globals: {
    Atomics: 'readonly',
    SharedArrayBuffer: 'readonly',
  },
  parserOptions: {
    project: 'tsconfig.json',
    tsconfigRootDir: __dirname,
    ecmaFeatures: {
      jsx: true,
    },
    ecmaVersion: 2018,
    sourceType: 'module',
  },
  settings: {
    react: {
      pragma: 'React',
      version: '17',
    },
  },
  plugins: ['react', 'import'],
  rules: {
    'react/jsx-filename-extension': [1, { extensions: ['.js', '.jsx', '.tsx'] }],
    'react/prop-types': 'off',
    "react/jsx-uses-react": "off",
    'react/react-in-jsx-scope': 'off',
    'react/require-default-props': 'off',
    'import/no-unresolved': 'off',
    'import/prefer-default-export': 'off',
    'no-param-reassign': 'off',
    'arrow-parens': [0, { requireForBlockBody: false }],
    'jsx-quotes': 'off',
    'react/jsx-one-expression-per-line': 'off',
  },
};
```

3. Create a file in the root folder with the name .prettier.js

```
module.exports = {
    semi: true,
    trailingComma: 'all',
    singleQuote: true,
    printWidth: 120,
    tabWidth: 2,
};
```

4. Open the terminal and type  ``` yarn run start```
