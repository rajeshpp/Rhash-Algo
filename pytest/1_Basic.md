# pytest basics
The `pytest` framework makes it easy to write small, readable tests, and can scale to support complex functional testing for applications and libraries.

`pytest` will run all files of the form `test_*.py` or `*_test.py` in the current directory and its subdirectories. 

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
