# After you create your app weither its react or nextjs

## Install prettier first

```
npm install --save-dev --save-exact prettier @typescript-eslint/eslint-plugin eslint-config-prettier
#or
yarn add --save-dev --save-exact prettier @typescript-eslint/eslint-plugin eslint-config-prettier
```

## After installing prettier let's setup our prettier config. Create a .prettierignore & .prettierrc.json file

```
// .prettierignore
# Dependencies
node_modules

# Configs
commitlint.config.js

# Caches
.eslintcache
.vscode

# Testings
coverage

# Builds
build
dist

# Miscellaneous
.DS_Store
.env
.env.*
.npmrc
*-lock.json
*.lock
.idea
*.suo
*.ntvs*
*.njsproj
*.sln
*.sw?

# Logs
logs
*.log
npm-debug.log*
yarn-debug.log*
yarn-error.log*
pnpm-debug.log*
lerna-debug.log*

# Types

# Ignores

```

```
// .prettierrc.json

#this is basic config of our prettier you can look for more here https://prettier.io/docs/en/configuration.html
{
  "singleQuote": true,
  "jsxSingleQuote": false,
  "tabWidth": 2,
  "trailingComma": "es5",
  "printWidth": 100,
  "semi": true,
  "arrowParens": "avoid",
  "endOfLine": "auto"
}
```
## As for our eslint to work with prettier and override some next.js/react.js default eslint config;
## Install @typescript-eslint/eslint-plugin

```
npm i --save-dev @typescript-eslint/eslint-plugin
#or
yarn add --save-dev @typescript-eslint/eslint-plugin
```

## After our install go and look into our folder the .eslintrc.json file

```
#Put this config for our .eslintrc.json

{
  "env": {
    "node": true,
    "browser": true,
    "es2021": true
  },
  "plugins": ["@typescript-eslint"],
  "extends": ["next/core-web-vitals", "plugin:@typescript-eslint/recommended", "prettier"],
  "rules": {
    "react/prop-types": "off",
    "react/display-name": "off",
    "react-hooks/rules-of-hooks": "error",
    "react-hooks/exhaustive-deps": "warn",
    "no-prototype-builtins": "off",
    "class-methods-use-this": "off",
    "linebreak-style": "off",
    "no-undef": "error",
    "no-console": "error",
    "prefer-default-export": "off",
    "import/prefer-default-export": "off",
    "import/no-cycle": "off",
    "@typescript-eslint/no-unsafe-call": "off",
    "@typescript-eslint/no-explicit-any": "off",
    "@typescript-eslint/no-unsafe-return": "off",
    "@typescript-eslint/explicit-module-boundary-types": "off",
    "@typescript-eslint/no-floating-promises": "off"
  }
}

```
