Code sample link: <https://replit.com/@jjoco/python-tuples>

Tuples, like lists, contain a record of values. Unlike lists, however, tuples cannot be changed after they have been created; you cannot remove or add more elements into a tuple.

## Why use tuples
When we know what values are going to be in collection, it is generally better to use tuples than lists. Tuples are also generally faster and memory efficient to create and read than lists since tuples have constant size. Unlike lists, in which it is almost mandatory practice to have lists contain only one data type, it is an okay practice to have multiple types in a tuple. This is why each element in a `dictionary.items()` call is a 2-tuple, in which the key and value types may not coincide.

So, if you wanted to maintain a running list of users with fields `age`, `name`, and `id`, you may not need to create a separate class for `User`. The list can look something like 
```python
[(25, "justin", 0), (38, "jack", 1), (35, "jackie", 2)]
```
Since we know that the size of the tuples are constant, we can more easily process them.
## Creating a tuple
You can create a tuple using parentheses like so:
```python
empty_tuple = ()
packed_tuple = (2, 5 , 7, 3, 2, 1, 9)
```
Keep in mind that if you make an empty tuple, you will not be able to change it.

## Accessing a tuple element
Like lists, you can access a value or group of values via indexing:
```python
print(packed_tuple[1])

print(packed_tuple[1:5])
```
## Unpacking a tuple
Though it is not as common for lists and dictionaries to be unpacked, unpacking a tuple (ie assigning values within the tuple to external variables) is much more common due to its immutability:
```python
date_tuple = ("04", "05", "2019")

(month, day, year) = date_tuple
print(month) 
print(day) 
print(year) 
'''
Prints out:
04
05
2019
'''
```

