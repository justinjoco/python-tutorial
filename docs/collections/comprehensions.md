Code sample link: <https://replit.com/@jjoco/python-comprehensions>

### Why use comprehensions

### List comprehensions
```
def pow(x: float, n: int) -> float:
  return x ** n

base_list = [2, 3, 4, 6, 7, 3, 2]

pow_list = [pow(num, 2) for num in base_list]
print(pow_list)

doubled_list = [num*2 for num in base_list]
print(doubled_list)
```

### Dictionary comprehensions
```
#From list
cubed_map = {x : x**3 for x in base_list}
print(cubed_map)

#From dict
base_map = {"ace": 11, "king": 12, "queen": 13, "jack": 14}
card_rev_map = { card[:-1] : value+4 for card, value in base_map.items()}
print(card_rev_map)
```

### Set comprehensions
```python
#From list or set
cubed_set = {x**3 for x in base_list}
print(cubed_set)

#From dict
my_map = {1:4, 3:6, 2:8}
add_set = {key+value for key, value in my_map.items()}
print(add_set)
```