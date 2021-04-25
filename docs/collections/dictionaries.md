Code sample link: <https://replit.com/@jjoco/python-dictionaries>
Dictionaries are data structures that maps keys to values. These maintain a running record of key-value pairs. For those familiar in other programming languages, dictionaries are Python's hashtables and hashmaps. For example, a dictionary can contain a record that associates (or maps) playing card cards to their numerical values. For the rest of the tutorial, I will be using `_map` as variable names for dictionary types, as associative key-value structures are generally called `maps` in other languages. In Python 3.6+, dictionaries maintain element insertion order, so you need not use `OrderedDict` to maintain an ordered dictionary, though it may be helpful for readability. 

## Why to use dictionaries?
When you go to the grocery store, each item in the store has an associated price tag to it. You cannot easily associate an item with a price with any other built-in data structure in Python except for a dictionary, which maps an item to a price. With a dictionary, you can quickly find the price of specific item, or update the price of another item without needing to look through the entire grocery inventory. To be more technical, dictionary reads and writes have `O(1)` time complexity. A very simple item-price dictionary can look like the following:

```python
{"banana": 3.99, "bread": 2.99, "salmon": 10.99, "onion": 1.99}
```

## Creating a dictionary
To create a dictionary, use curly braces:
```python
# Empty dictionary
my_map = {}

# Populated dictionary
grocery_map = {"banana": 3.99, "bread": 2.99, "salmon": 10.99, "onion": 1.99}
```

Like any other data structure, you can type-hint a dictionary's keys and values:
```python
from typing import Dict
grocery_map: Dict[str, float] = {"banana": 3.99, "bread": 2.99, "salmon": 10.99, "onion": 1.99}
```

## Setting dictionary elements
Like I alluded to earlier, you can easily add a new key-value pair to the dictionary or update the value of a given key, like the following:
```python
my_map["jack"] = 11
my_map["queen"] = 12
my_map["king"] = 13 
```
## Getting a dictionary element
You can also get the value of a given key:
```python
king_value = my_map["king"] 
king_value_with_get = my_map.get("king") 
```
Note that if a key-value pair does not exist, then `my_map["king"] ` would throw an KeyError exception; whereas, `my_map.get("king")` will return a `None` type.

## Iterate a through dictionary elements
There are several ways to iterate through dictionaries.
### Via simple iteration
Using the following syntax, we can iterate through the keys of a dictionary:
```python
for key in my_map:
  print(my_map[key])
```
### Via .items() -> each element is a tuple (key, value)
Each element in dictionary.items() is a 2-tuple (a tuple containing only two elements), and one can iterate through the 0th and 1st index of that tuple to grab the key and value, respectively.
```python
for item in my_map.items():
  print("Item: ", item)
  key = item[0]
  value = item[1]
```
However, this approach is not readable and more tedious to write than the following:
```python
for key, value in my_map.items():
    #Do stuff to key and value
```
What's happening here is that we're unpacking the tuple element into `key` and `value`, and we can easily process `key` and `value`

### Via .keys()
We can iterate through only the keys of the dictionary.
```python
for key in hello_map.keys():
  print(key)
```
### Via .values()
We can also iterate through only the values of the dictionary.
```python
for value in hello_map.values():
  print(value)
```
## Deleting a dictionary key-value pair
One can delete a key-value pair by only knowing the key.
```python
del my_map["king"]
```
