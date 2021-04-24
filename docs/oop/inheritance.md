Code sample link: <https://replit.com/@jjoco/python-inheritance>

## Why use inheritance

## Example parent class
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
## Example child class
```python
class Square(Rectangle):
  def __init__(self, side):
    super().__init__(side, side)
    self.side = side

  def get_side(self):
    return self.side
```

```python
my_sq = Square(5)
print(my_sq.get_area()) 
print(my_sq.get_dimensions()) 
print(my_sq.get_side()) 
```

