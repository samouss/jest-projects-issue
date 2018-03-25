## Jest projects

See [#XXX]()

```sh
cd single-project && yarn && yarn test --listTests

.../jest-projects-issue/single-project/packages/package-a/index.spec.js
.../jest-projects-issue/single-project/examples/example-a/index.spec.js # Should not be listed
```

```sh
cd single-project && yarn && yarn test --listTests --projects packages/*

.../jest-projects-issue/single-project/packages/package-a/index.spec.js
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
