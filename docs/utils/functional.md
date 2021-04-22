Code sample link: <https://replit.com/@jjoco/python-functional>

## why use functional functions
```python
items = [0 , -1, -5, 3, 5, 6, 2, 1]

```
## map
```python
from functools import reduce
squared = list(map(lambda x: x**2, items))
print(squared)
```
## reduce
```python
from functools import reduce

total = reduce(lambda acc, nextVal : acc + nextVal, items)
print(total)
```
## filter
```python
filtered = list(filter(lambda x: x < 0, items))
print(filtered)
```