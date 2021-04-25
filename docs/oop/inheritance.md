Code sample link: <https://replit.com/@jjoco/python-inheritance>

Class inheritance is how we can derive a class (called the derived, child, or subclass) from another class (called the base, parent, or superclass). Classes dervied from some base class maintain some, if not many, characteristics of the base class, but does something a bit differently that warrants the creation of a whole new class.
## Why use inheritance
Let's say we have a `Rectangle` class that has fields `width` and `length`. Let's say we wanted to create a rectangle whose width and length are the same.
```python
rect = Rectangle(6 , 6)
```
There's nothing wrong with setting a rectangle with equivalent width and height; however, it will be annoying for the caller to keep on writing `Rectangle(some_number , some_number)` if there will be a lot of these type of rectangles. To resolve this, we can write a new `Square` class, which is a rectangle with equivalent `width` and `height`.

## Inheritance at work
Let's take the simple implementation of the `Rectangle` class from the previous section:
```python
class Rectangle:
  def __init__(self, width: float, length: float) -> None:
    self.width = width
    self.length = length

  def get_area(self) -> float:
    return self.width * self.length

  def get_dimensions(self) -> tuple:
    return (self.width, self.length)
```
We can create a child class `Square` using the following syntax:
```python
class DerivedClass(BaseClass):
  .
  .
  .
```

We will need to use the `super()` function in the derived class's constructor to gain access to the base class's fields and methods:
```python
class Square(Rectangle):
  def __init__(self, side):
    super().__init__(side, side)
    self.side = side

  def get_side(self):
    return self.side
```
Here, we are feeding the `side` parameter of the `Square` as both parameters of the base class's constructor. This allows us to call `Rectangle`'s `get_dimensions()` and `get_area()` methods without needing to re-implement them.

We also add a `get_side()` method to access the `side` field of the square.

Take the following calling example:
```python
my_sq = Square(5)
print(my_sq.get_area()) # Returns 25
print(my_sq.get_dimensions()) # Returns (5, 5)
print(my_sq.get_side())  # Returns 5
```
Even though we didn't re-implement `get_area()` or `get_dimensions()` we could still call those functions since `Square` is a `Rectangle` and `Square` can access `Rectangle`'s methods. However, we can re-implement a base class method, if we want:
```python
class Square(Rectangle):
  def __init__(self, side):
    super().__init__(side, side)
    self.side = side

  def get_dimensions(self):
    return self.side
```
Here, I rename the original `get_side()` method into `get_dimensions()`, allowing `Square`'s implementation to take precendence over `Rectangle`'s:
```python
my_sq = Square(6)
print(my_sq.get_area()) # Returns 
print(my_sq.get_dimensions()) # Returns 6
```
