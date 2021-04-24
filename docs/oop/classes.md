

### Why to create class

## Creating a class
Code sample link: <https://replit.com/@jjoco/python-classes>
```python
class MyClass:
    .
    .
    .

```
Code sample: <https://replit.com/@jjoco/python-fields>

### Constructor and instance methods
```python
class MyClass:
    def __init__(self, *args):
        .
        .
        .

```

```python
class MyClass:
   
    .
    .
    .
    def my_method(self, ...):
        .
        .
        .

```

```python
class Rectangle:
    def __init__(self, width: int, height: int):
        self.width = width
        self.length = length

    def get_area(self) -> int:
        return self.width * self.length
```
### Private methods and fields
```python
class Rectangle:
    def __init__(self, width: int, height: int):
        self._width = width
        self._length = length
        self._area = -1

    def _calculate_area(self):
        return self._width * self._length

    def get_area(self) -> int:
        if self._area <= 0:
            self._area = self._calculate_area()

        return self._area
```

## Creating instance of class (ie object)

```python
rect = MyRectangle(5, 6)

print(rect.get_area())
# Output = 30
```


