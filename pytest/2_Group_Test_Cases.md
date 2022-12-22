# Grouping multiple test cases in a class
In this section, we will dive deep into grouping the test cases in a class.

Make sure to prefix your class with Test otherwise the class will be skipped. 

Also, remember that the method names within the class should follow the pytest standards as `test_%` or `%_test`

```
# content of 3_group_tests.py
class TestClass:
    def test_method_one(self):
        x = "group"
        assert "r" in x

    def test_method_two(self):
        x = "hello"
        assert hasattr(x, "check")
```
<img width="726" alt="image" src="https://user-images.githubusercontent.com/19406666/209077514-0849aa6a-a38c-4dad-b680-839284440e1b.png">


Grouping test cases in classes can be beneficial for the following reasons:
- Organizing test cases.
- Sharing fixtures for tests only in that particular class.
- Applying marks at the class level and having them implicitly apply to all tests.

Though, you group multiple test cases within the same class, each test has a unique instance of the class.

```
# content of 4_class_isolation.py
class TestClassInstanceIsolation:
    value = 0

    def test_method_one(self):
        self.value = 5
        assert self.value == 5

    def test_method_two(self):
        assert self.value == 5
```
<img width="854" alt="image" src="https://user-images.githubusercontent.com/19406666/209102269-eba94986-b85e-469e-b31c-4e6d87024d5f.png">

Note that attributes added at class level are class attributes, so they will be shared between tests.
