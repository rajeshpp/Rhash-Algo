# pytest basics
The `pytest` framework makes it easy to write small, readable tests, and can scale to support complex functional testing for applications and libraries.

`pytest` will run all files of the form `test_*.py` or `*_test.py` in the current directory and its subdirectories. 

### Different ways of using pytest
#### Run tests in a module
`pytest test_mod.py`

#### Run tests in a directory
`pytest testing/`

#### Run tests by keyword expressions
`pytest -k "MyClass and not method"`

This will run tests which contain names that match the given string expression (case-insensitive), which can include Python operators that use filenames, class names and function names as variables. 

The example above will run TestMyClass.test_something but not TestMyClass.test_method_simple.

#### Run tests by node ids
`pytest test_mod.py::test_func`

Another example specifying a test method in the command line:

`pytest test_mod.py::TestClass::test_method`

#### Run tests by marker expressions
`pytest -m slow`
Will run all tests which are decorated with the @pytest.mark.slow decorator.

#### Run tests from packages
`pytest --pyargs pkg.testing`

This will import pkg.testing and use its filesystem location to find and run tests from.

### A very basic example:
```
# content of 1_sample_test.py
def addition(x, y):
    return x + y


def test_fail():
    assert addition(3, 4) == 5


def test_success():
    assert addition(3, 4) == 7
```
<img width="690" alt="image" src="https://user-images.githubusercontent.com/19406666/208868549-ab83a7c4-c7bc-403d-a31f-d0945b50d18e.png">

### Raise certain exception
```
# content of 2_sysexit_test.py
import pytest


def fun():
    raise SystemExit(1)


def test_mytest():
    with pytest.raises(SystemExit):
        fun()
```
<img width="331" alt="image" src="https://user-images.githubusercontent.com/19406666/208875321-fe29d437-020d-4376-9e65-7094ee8d0ec2.png">
