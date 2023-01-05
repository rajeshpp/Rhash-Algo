# Write & Report Assertions

## Asserting with `assert`
We can use assert to expectations and values in Python.
```
# Sample of test_assert

def f():
    return 5


def test_function_success():
    assert f() == 5, "Value is not returned as expected."


def test_function_failure():
    assert f() == 4, "Value is not returned as expected."

```
<img width="863" alt="image" src="https://user-images.githubusercontent.com/19406666/210780168-b40fe787-fd09-4475-86c1-8c530d68ab43.png">

If the assertion fails, we can see the return value of the function call.

## Asserting `exceptions`
## Asserting `warnings`
## context-sensitive comparisons
## own explanation for failed assertions
