Code sample link: <https://replit.com/@jjoco/python-comprehensions>

Comprehensions is neat Python feature that allows the creation of new collections from previously-made collections in a syntactically concise way.

## List comprehensions
List comprehensions allows the creation of new lists from other collections. The general syntax is the following:
```python
#From list
new_list = [some_function(elem) for elem in some_list if condition]

#From dictionary
new_list_from = [some_function(key, value) for key, value in some_map.items() if condition]
```
What's happening is that elements in a base collection (that satisfy the given condition) are passed into a function, and the output values of the function become the elements of the new list.

In the following example, we use list comprehension syntax to create a list of integers that contains cubed values of even numbers of a base list, and another that contains doubled values of the same list:
```python
def pow(x: float, n: int) -> float:
  return x ** n

base_list = [2, 3, 4, 6, 7, 3, 2]

pow_list = [pow(num, 2) for num in base_list if num%2 ==0]
print(pow_list) # [4, 16, 36, 4]

doubled_list = [num*2 for num in base_list]
print(doubled_list) # [4, 6, 8, 12, 14, 6, 4]
```

## Dictionary comprehensions
Similarly to list comprehensions, we can create a new dictionary from a collection using the following syntax:
```python
#From list
my_map = {key_func(elem) : value_func(elem) for elem in some_list if condition}

#From dict
my_map = {key_func(prev_key) : value_func(prev_value) for prev_key, prev_value in base_map.items() if condition}
```
What's happening here is that we use the items (that satsify a given condition, if provided) in the given collection to create the key-value pairs in our new dictionary.

Take the following example:
```python
#From list
base_list = [2, 3, 4, 6, 7, 3, 2]
cubed_map = {x : x**3 for x in base_list}
print(cubed_map) # {2: 8, 3: 27, 4: 64, 6: 216, 7: 343}

#From dict
base_map = {"ace": 11, "king": 12, "queen": 13, "jack": 14}
card_rev_map = { card[:-1] : value+4 for card, value in base_map.items() if len(key) >= 4}
print(card_rev_map) # {'kin': 16, 'quee': 17, 'jac': 18}
```
In the dictionary comprehension that is based off a list, we create a dictionary that maps the numbers of `base_list` to their cubed values. In the dictionary-based dictionary comprehension, we create a new map that contains the shortened face card names their incremented card values, given the original card names were at least 4 characters long.

## Set comprehensions
Set comprehension syntax is the same as that of list comprehension, except with curly braces.
```python
#From list
my_set = {some_func(elem) for elem in some_list if condition}

#From dict
my_set = {some_func(key, value) for key, value in base_map.items() if condition}
```

Consider the following:
```python
#From list or set
base_list = [2, 3, 4, 6, 7, 3, 2]
cubed_set = {x**3 for x in base_list}
print(cubed_set) #{64, 8, 343, 216, 27}

#From dict
my_map = {5:7, 3:6, 2:8}
add_set = {key+value for key, value in my_map.items() if value % key == 0}
print(add_set) #{9, 10}
```
In the first exapmle, we create a set of cubed values based on values of `base_list`. In the second, we create a new set, whose values are the sum of key-value pairs in `my_map`, given that a pair's value is a multiple of its key.
## Generator comprehensions
Generator comprehension syntax is the same as that of list/set comprehension, except with parentheses.
