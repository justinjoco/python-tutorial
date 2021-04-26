Code sample link: <https://replit.com/@jjoco/python-lambdas>

Lambda functions can be thought of short-term, concise, impromptu functions that are intended to be thrown away after one or a couple of uses.
## Why use lambda functions

## Lambdas are anonymous functions
```python
double_funct = lambda x: x * 2
print(double_funct(5))


add_funct = lambda x, y: x + y
print(add_funct(5, 7))
```
## Creating a lambda generator function
```python
def exp_funct(n):
  return lambda x : x ** n

square_funct = exp_funct(2)
print(square_funct(5))

cube_funct = exp_funct(3)
print(cube_funct(5))

```
## Using lambda as key in collection sort
```python
card_map = {"king": 13, "jack": 11, "queen": 12, "ace": 1}
print(card_map)

sorted_list = sorted(card_map.items(), key=lambda item: item[1])
print(sorted_list)

sorted_map = dict(sorted_list)
print(sorted_map)
```