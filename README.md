# Syntax check

Licence: [MIT](https://opensource.org/licenses/MIT)

---

[![npm version](https://badge.fury.io/js/%40superhero%2Fsyntax-check.svg)](https://badge.fury.io/js/%40superhero%2Fsyntax-check)

A "syntax check test" module that utilizes the `node -c` command through a bash script.

## Install

`npm install @superhero/syntax-check`

...or just set the dependency in your `package.json` file:

```json
{
  "dependencies":
  {
    "@superhero/syntax-check": "*"
  }
}
```

## Example

```js
{
  "name": "Super Duper App",
  "scripts": {
    "test": "syntax-check"
  },
  "devDependencies": {
    "@superhero/syntax-check": "0.0.1"
  }
}
```

## Example | with mocha, or any other test script

```js
{
  "name": "Super Duper App",
  "scripts": {
    "test": "syntax-check && mocha"
  },
  "devDependencies": {
    "@superhero/syntax-check": "0.0.1",
    "mocha": "5.1.0",
  }
}
```

## Output

```
  Syntax check of files:

  ✔ ./index.js
  ✔ ./model/auth/aggregate.js
  ✔ ./model/auth/index.js
  ✔ ./model/auth/error/invalid-token.js
  ✔ ./model/auth/error/unauthorized.js
  ✔ ./model/log/index.js
  ✔ ./model/redis/gateway.js
  ✔ ./model/redis/index.js
  ✔ ./model/redis/error/key-conflict.js
  ✔ ./model/redis/gateway-fallback.js
  ✔ ./model/mysql/gateway.js
  ✔ ./model/mysql/gateway/transaction.js
  ✔ ./config.js
  ✔ ./controller/endpoint/index.js
  ✔ ./controller/endpoint/v1.leads.js
  ✔ ./controller/middleware/authenticate.js
  ✔ ./controller/middleware/authorize.js

  Successful syntax check of 30 files
```
