Code sample link: <https://replit.com/@jjoco/python-functional>

These functions help the developer take a more functional approach to some problems.

Let's say we have an `items` list:
```python
items = [0 , -1, -5, 3, 5, 6, 2, 1]
```
## `map`
The `map` function allows the developer to apply a function to all items in a list, and returns an iterator that contains the output values.

Syntax
```python
map_iterator = map(map_func, base_list)
```

Check out the following:
```python
squared = list(map(lambda x: x**2, items))
print(squared) #[0, 1, 25, 9, 25, 36, 4, 1]
```
Note that `list` is needed to cast the iterator into a list. In this example, we create multiply each value in `items` by 2, and put the output results in a new list. FYI, you could also do the above using list comprehensions.

## `filter`
`filter` creates a new list that contains the values of some base list based on some condition function.

Syntax
```python
filtered_iter = filter(condition_func, items)
```

For example,
```python
filtered = list(filter(lambda x: x < 0, items))
print(filtered) # 11
```
Here, we filter out anything in `items` that is not negative. 
## `reduce`
`reduce` is used to do some computation on an entire list, instead of each element separately. It performs a rolling computation on sequential pairs in the list in order to accumulate the elements into a single value.

Firstly, we need to import `reduce` from the `functools` library and use the following syntax:
```python
from functools import reduce
result = reduce(reduce_func, items)
```

Consider the following:
```python
from functools import reduce

total = reduce(lambda acc, nextVal : acc + nextVal, items)
print(total) # 11
```
In the above example, we use `reduce` to get the sum of the given `items` list. 
