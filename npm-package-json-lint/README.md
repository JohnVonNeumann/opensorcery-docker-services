# opensorcery/npm-package-json-lint
## A package.json linter for Node projects.

### Overview

[npm-package-json-lint helps enforce standards for your package.json file. Currently it can check for:](https://www.npmjs.com/package/npm-package-json-lint)
* validity of data types in nodes. Ex: name should always be a string.
* whether a string is a lowercase
* whether a version number is a valid
* the presence of a given module
* the presence of a pre-release version of a module

### Usage

#### Pull image

```
docker pull opensorcery/npm-package-json-lint
```

#### Run container

```
docker run --rm -v ${PWD}:/code opensorcery/npm-package-json-lint /code
```

#### Run from within Travis CI 

```
jobs:
  include:
    - stage: code linting
      script:
        - >
          docker run --rm
          -v ${PWD}:/code
          opensorcery/npm-package-json-lint
          /code
```
