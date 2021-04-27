Code sample link: <https://replit.com/@jjoco/python-sets>

Sets are unordered (ie does not remember the insertion order) and unindexed (ie cannot read or write an element via an index) records of values. Python sets can be utilized like mathematical sets, as operations between sets are similar to that of mathematical sets (eg. intersections, unions, etc.). Each item in a set is unique, and fortunately, one can iterate through a set and can add items into it.
## Why use sets
Sets in Python are highly optimized for reading and writing speed. When you check if a list contains some certain value, Python, at worst, would need to search through the entire list. On other hand, Python, at worst, would need to use a lookup table to figure out if an item exists in the set. To be more technical, time complexities for reading and writing values in a set is `O(1)`.

## Creating a set
To create an empty set, you can use the `set()` function, or use curly braces like dictionaries. Keep in mind that Python will interpret empty curly braces as a dictionary; however, populated curly braces with items (that are not key-value pairs) will be interpreted as sets.
```python
#Create empty set
init_set = set()
print(init_set)
'''
Prints out:
set()
'''

#Create a set using curly braces
set_with_curly_braces = {"hi", "there", "hello"}

#Create a set from an initial list
set_from_list = set(["hello", "world", "set"])
print(set_from_list)
'''
Prints out:
{'set', 'world', 'hello'}
'''
```
## Checking if a set contains an element
Use keyword `in` to check to see if a value exists in a set:
```python
#Check if element exists in set
target = "hello"
if target in set_with_curly_braces:
  print("target is seen")
'''
Prints out:
target is seen
'''
```
## Pushing an element into a set
Use the `.add(elem)` method to add an item into a set:
```python
set_with_curly_braces.add("added_elem")
print(set_with_curly_braces)
'''
Prints out:
{'there', 'hi', 'hello', 'added_elem'}
'''
```

## Iterating
You can interate through a set like any other collection:
```python
for elem in set_with_curly_braces:
  print(elem)
'''
Prints out:
there
hi
hello
added_elem
'''
```
Since sets are unordered, elements may be printed in a different order each time the for-loop is run.
## Clear set
Use `.clear()` to remove all items in the set
```python
set_with_curly_braces.clear()
print(set_with_curly_braces)
'''
Prints out:
set()
'''
```

## Set operations
Like I alluded to before, set operations can be used between set operands. The following subsections will use the following sets in their examples:
```python
set_a = {5, 7, 3, 6 ,2 ,4, 1, 0}
set_b = {5, 7, 3, 6 , 1, 0, 19}
set_c = {5, 7, 3, 6 ,2 , 0}
```

### Union
Given sets `A` and `B`, use `|` or `A.union(B)` to get the union of the two sets (ie a set of all distinct elements common or not common in the two sets) 
```python
print(set_a | set_b)
print(set_a.union(set_b))
# Both print {0, 1, 2, 3, 4, 5, 6, 7, 19}
```

### Intersection
Given sets `A` and `B`,  use `&` or `A.intersection(B)` to get the intersection of the two sets (ie a set of all distincts elements common in the two sets) 
```python
print(set_a & set_b)
print(set_a.intersection(set_b))
# Both print {0, 1, 3, 5, 6, 7}
```
### Difference
Given sets `A` and `B`, use `-` or `A.difference(B)` to get the union of the two sets (ie a set of all elements in `A`, but not in `B`). 
```python
print(set_a - set_b)
print(set_a.difference(set_b))
# Both print {2, 4}
```
### Is Subset
Given sets `A` and `B`, use `<=` or `A.issubset(B)` to check if `A` is a subset of `B` (ie. all elements in `A` are contained in `B`)
```python
print(set_c <= set_a)
print(set_c.issubset(set_a))
# Both print True
```
### Is Superset
Given sets `A` and `B`, use `>=` or `A.issuperset(B)` to check if `A` is a superset of `B` (ie. `A` contains all elements in `B`)
```python
print(set_a >= set_c)
print(set_a.issuperset(set_c))
# Both print True
```