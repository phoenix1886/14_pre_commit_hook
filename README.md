# Quadratic Equations Solver

This script calculates root of quadratic equation.

# How to use

To use the script one should import quadratic_equation module, and use get_roots(a, b, c) function, where a, b, c are coefficients of equation.

```python
from quadratic_equation import get_roots


root1, root2 = get_roots(a,b,c)
```

# How to use auto-test

For auto-test usage one should:
* make pre-comit file executable, executing the following command:
```bash
chmod +x pre-comit
```
* copy pre-comit file to `.git/hooks` directory of your local repository.

Auto-test executes `tests.py` before commit, and if failed, it rejects commitment.

## Example of failed test

```bash
$ git commit -m 'your comment'
=====================================
.E..
======================================================================
ERROR: test_returns_none_for_complex_solution (__main__.QuadraticEquationTestCase)
----------------------------------------------------------------------
Traceback (most recent call last):
  File "tests.py", line 22, in test_returns_none_for_complex_solution
    root1, root2 = get_roots(1, 2, 3)
  File "/Users/User/devman/problem14/14_pre_commit_hook/quadratic_equation.py", line 6, in get_roots
    root1 = (-b - sqrt(discriminant)) / (2 * a)
ValueError: math domain error
----------------------------------------------------------------------
Ran 4 tests in 0.001s

FAILED (errors=1)
> Tests DID NOT pass. Commit rejected!
```

This project includes pre-commit script, which makes pre-commit tests.

# Requirements

To use script one should have Python 3.5 installed.

# Project Goals

The code is written for educational purposes. Training course for web-developers - [DEVMAN.org](https://devman.org)
