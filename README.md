See [#5866](https://github.com/facebook/jest/issues/5866)

### From the configuration file (not working)

```sh
yarn && yarn test --listTests

jest-projects-issue/packages/package-a/index.spec.js
jest-projects-issue/examples/example-a/index.spec.js # SHOULD NOT BE RUN
```

```json
{
  "jest": {
    "projects": [
      "packages/*"
    ]
  }
}
```


### From the CLI (working)

```sh
yarn && yarn test --listTests --projects packages/*

jest-projects-issue/packages/package-a/index.spec.js
```

```json
{
  "jest": {
    "projects": [
      "packages/*"
    ]
  }
}
```
