
Code links: <https://replit.com/@jjoco/python-fields>
 
Classes are blueprints of objects or data structures. Objects of a class contain their own attributes(or fields) and functions (or methods).

Python supplies many basic types and data structures; however, these are all very generic and would not be useful by themselves if the developer wants to do something specific for in their program. This is where classes come in.

Let's say I wanted to create a program involving basic shapes and their operations. We can create a blueprint for shapes by creating a new class, and when we want to create new shapes for our program, we can create new instances (or objects) of that `Shape` class. Each `Shape` object would have common field names and common methods, which makes code implementation easier and reusable.

The programming paradigm of creating and manipulating objects and classes is called "object-oriented programming" (OOP).

## Creating a class

To create a new class, you can use the `class` keyword:
```python
class MyClass:
    .
    .
    .

```
### Constructor and instance methods
Though it's not mandatory, most classes contain a constructor method, which sets the initial state of a newly created object of a given class:

```python
class MyClass:
    def __init__(self, *args):
        .
        .
        .
```

The dev can create other methods for the class in addition to the constructor:
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
You may have noticed that first argument of any class's instance method is `self`. This argument references the current instance of the class, and `self` is Python's naming convention for this parameter.


Let's go through a more thorough example. In the following example, we create a `Rectangle` class:
```python
class Rectangle:
    def __init__(self, width: int,  length: int):
        self.width = width
        self.length = length

    def get_area(self) -> int:
        return self.width * self.length
```
This class contains the blueprint for creating a `Rectangle` object. In our constructor, we're setting the initial width and length of the `Rectangle` object to whatever the caller has specified. We have a `get_area()` function that calculates the `Rectangle` object's area based upon the object's `width` and `length` field values.

## Creating instance of class (ie object)
To create a new object (or instance) of the `Rectangle` class, we can do the following:
```python
rect = Rectangle(5, 6)

print(rect.get_area())
# Output = 30
```
In the above code block, we create a new `Rectangle`, whose initial width and length are 5 and 6, respectively. Then, we invoke the `.get_area()` function, which returns us the calculated area of the rectangle, which in this case is `30`.

## Private methods and fields
Unlike other object-oriented programming (OOP) languages, all class fields and functions are public (ie can be read or written directly by external callers). The dev can write the fields and methods as if to treat them like they are private (ie cannot be read or written directly by external callers) by prepending an underscore `_` to field names and methods. Take the following `Rectangle` class rewritten to have "private" fields and methods:
```python
class Rectangle:
    def __init__(self, width: int,  length: int):
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
This class is written such that external callers should only be able to `get_area()`; however, Python does not stop an external caller from calling `_calculate_area()` or changing `_width` or `_length`.

However, if the class is written to have private fields or methods, the dev can write setters and getters to indirectly access those fields:
```python
class Rectangle:
    def __init__(self, width: int,  length: int):
        self._width = width
        self._length = length

    def set_width(self, width: int) -> None:
        self._width = width
    
    def set_length(self, length: int) -> None:
        self._length = length

    def get_width(self) -> int:
        return self._width
    
    def get_length(self) -> int:
        return self._length

# Calling
rect = Rectangle(5, 7)
print(rect.get_width()) # width == 5
rect.set_width(8)
print(rect.get_width()) # width == 8
```
As you can see, it can be a bit verbose to write setters and getters this way. Luckily, Python has some handy annotations that'll allow you to write setters and getters more cleanly, but that's outside the scope of this tutorial.

