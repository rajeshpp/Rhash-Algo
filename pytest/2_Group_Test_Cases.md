# Grouping multiple test cases in a class
In this section, we will dive deep into grouping the test cases in a class.

Make sure to prefix your class with Test otherwise the class will be skipped. 

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
