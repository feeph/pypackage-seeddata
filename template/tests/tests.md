# Tests

This directory contains our unittests.

## Manual

There are 3 ways to run the tests. The recommended order is:

- __`pdm run pytest`__
  - Run the unit tests and nothing else.  (pytest)
- __`scripts/validate_code`__
  - Lint the code. (flake8, mypy)
  - Provide improvement recommendations. (pylint)
  - Run the unit tests. (pytest)
- __`tox`__
  - Lint the code. (flake8, mypy)
  - Run the unit tests on all Python versions this package supports. (pyenv+tox+pytest)
  - Measure test coverage.

## Automated

In addition there are the following automated processes:

- commit validation (pre-commit hook)
- Pull-Request validation (GitHub Action)

Please note: 
 - Compliance with PEP8 is enforced via flake8.
 - Opinionated tools like `black`, `pylint`, `ruff` that intend to enforce
   a specific code style but don't affect the correctness of the code are
   NOT part of any pre-commit hook or GitHub Action and are not enforced.
