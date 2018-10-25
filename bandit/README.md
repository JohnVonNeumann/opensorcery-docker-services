# opensorcery/bandit
## Bandit is a tool designed to find common security issues in Python code.

### Overview

[Bandit is a tool designed to find common security issues in Python code. To do this Bandit processes each file, builds an AST from it, and runs appropriate plugins against the AST nodes. Once Bandit has finished scanning all the files it generates a report.](https://github.com/PyCQA/bandit#overview)

Bandit was originally developed within the OpenStack Security Project and later rehomed to PyCQA.

### Usage

#### Pull image

```
docker pull opensorcery/bandit
```

#### Run container

```
docker run --rm -v ${PWD}:/code opensorcery/bandit -r /code
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
          opensorcery/bandit -r
          /code
```
