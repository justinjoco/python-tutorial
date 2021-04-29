Code sample link: <https://replit.com/@jjoco/python-dictionaries>

When you go to the grocery store, each item in the store has an associated price tag to it. You can easily associate an item with a price Python's in-built data structure: the dictionary. 

Dictionaries are data structures that maps keys to values. Like lists, these maintain a running record of elements. Unlike lists, these store key-value pairs, and keys cannot be duplicated, but multiple keys can have the same value. For those familiar in other programming languages, dictionaries are Python's hashtables and hashmaps.

With a dictionary, you can quickly find the price of specific item, or update the price of another item without needing to look through the entire grocery inventory. To be more technical, dictionary reads and writes have `O(1)` time complexity. A very simple item-price dictionary can look like the following:
```python
{"banana": 3.99, "bread": 2.99, "salmon": 10.99, "onion": 1.99}
```


For the rest of the tutorial, I will be using `_map` as variable names for dictionary types, as associative key-value structures are generally called `maps` in other languages. In Python 3.6 and later versions, dictionaries maintain element insertion order, so you need not use `OrderedDict` to maintain an ordered dictionary, though it may be helpful for readability. 

## Creating a dictionary
To create a dictionary, use curly braces:
```python
# Empty dictionary
my_map = {}

# Populated dictionary
grocery_map = {"banana": 3.99, "bread": 2.99, "salmon": 10.99, "onion": 1.99}
```

Like any other data structure, you can type-hint a dictionary's keys and values using syntax `some_map: Dict[KeyType, ValueType]`:
```python
from typing import Dict
grocery_map: Dict[str, float] = {"banana": 3.99, "bread": 2.99, "salmon": 10.99, "onion": 1.99}
```

## Setting dictionary elements
Like I alluded to earlier, you can easily add a new key-value pair to the dictionary or update the value of a given key, like the following:
```python
grocery_map["chicken_breast"] = 5.99
grocery_map["banana"] = 1.00
grocery_map["bread"] = 9.00
```
## Getting a dictionary element
You can also get the value of a given key:
```python
banana_price = grocery_map["banana"]
banana_price_with_get = grocery_map.get("banana") 
```
Note that if a key-value pair does not exist, then `grocery_map["banana"] ` would throw an KeyError exception; whereas, `grocery_map.get("banana")` will return a `None` type.

## Getting the length of a dictionary
You can use `len` to get the number of key-value pairs in a dictionary (ie. its length) .
```python
dictionary_length = len(my_dictionary)
```
So, if `grocery_map = {"banana": 3.99, "bread": 2.99, "salmon": 10.99, "onion": 1.99}`, then `len(grocery_map)` would be `4`.

## Iterate through dictionary elements
There are several ways to iterate through dictionaries.
### Via simple iteration
Using the following syntax, we can iterate through the keys of a dictionary:
```python
for key in grocery_map:
  print(grocery_map[key])
```
### Via `.items()`
Fortunately in Python, we can iterate through a dictionary's keys and values more cleanly via dictionary.items() (the function name is completely unrelated to the grocery store theme):
```python
for key, value in grocery_map.items():
    #Do stuff to key and value
```
Here, we can process the key and value of a pair simultaneously.
Note that those variables need not be named `key`, `value`; since we're using a grocery store theme, we can rewrite the above as the following:
```python
for item, price in grocery_map.items():
    #Do stuff to key and value
```

To be a bit more technical, elements in dictionary.items() are 2-tuples (immutable array data structures with only two elements), and one can iterate through the 0th and 1st index of that tuple to grab the key and value, respectively.
```python
for item in grocery_map.items():
  key = item[0]
  value = item[1]
  print("Item: ", item) # Item: (<key>, <value>)
```
However, this approach is not readable and more tedious to write than the ealier `key, value` syntax, in which we're unpacking the tuple element into `key` and `value`.

### Via `.keys()`
We can iterate through only the keys of the dictionary.
```python
for key in grocery_map.keys():
  print(key)
```
### Via `.values()`
We can also iterate through only the values of the dictionary.
```python
for value in grocery_map.values():
  print(value)
```
## Deleting a dictionary key-value pair
One can delete a key-value pair by only knowing the key.
```python
del grocery_map["banana"]
```
