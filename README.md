### After you create your app weither its react or nextjs

## Install prettier first

```
npm install --save-dev --save-exact prettier @typescript-eslint/eslint-plugin eslint-config-prettier
#or
yarn add --save-dev --save-exact prettier @typescript-eslint/eslint-plugin eslint-config-prettier
```

## After installing prettier create a .prettierignore & .prettierrc.json file

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

