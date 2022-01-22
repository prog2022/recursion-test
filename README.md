## Test the Recursion Lab using Pytest

Pytest is a Python plugin.  My tests also use the pytest-timeout plugin 
to prevent tests from running forever.

To install both packages using pip3:
```
pip3 install --upgrade pytest pytest-timeout
```
I prefix this command with "sudo " (Linux cmd) to install plugins globally (not in my home dir).


### Run doctests using Pytest

Run all doctests (from the starter code) and print nicely formatted results:
```
pytest --doctest-modules
```

Run doctests for just one module, say, groupsum:
```
pytest --doctect-modules groupsum.py
```
but its more informative to run doctest directly:
```
python3 -m doctest -v groupsum.py
```

### Run My Pytests

This repo contains parameterized pytests for each problem in the lab:

| File               | Tests for |
|--------------------|-----------|
| `test_all.py`      | All problems **except** groupsum |
| `test_groupsum.py` | groupsum |


Copy these files to the student's code dir. Run all tests with verbose output:
```
pytest -v
```

Run tests for only the `split_array` problem:
```
pytest -v -k split_array
```

Run only the tests in a particular file, e.g. `test_groupsum.py`:
```
pytest -v test_groupsum.py
```

### Code Inspection

Student solutions should **not** use 
- for loop
- while loop
- list comprehensions, or 
- `sum()`, `sum()` is OK in groupsum and `split_array` if the solution relies on recursion.


### Note to TAs

You can combine `test_groupsum` into `test_all` if that's more convenient.

I separated them in case students make syntax errors in groupsum.

Also, if you add any more test cases please commit them back to the repo!
