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
You can create a tuple using parentheses `()` like so:
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
## Getting the length of a tuple
To get the number of elements in a tuple (ie. its length), use the `len` function:
```python
tuple_length = len(my_tuple)
```
So, if `my_tuple = (2, True, False, "hello")`, then `len(my_tuple)` would be `4`.

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
To continue on the example from before about a user_list, we can use unpacking to more easily process the user list:
```python
user_list = [(25, "justin", 0), (38, "jack", 1), (35, "jackie", 2)]
for age, name, id in user_list:
  print(age)
  print(name)
  print(id)
  print()
'''
Prints out:
25
justin
0

38
jack
1

35
jackie
2
'''
```
Here, we unpack all three elements of the 3-tuple and can process them separately.


Recall that when we process a dictionary's items using `dictionary.items()`, we use syntax:
```python
for some_key, some_val in some_map.items():
    .
    .
    .
```
This shows that the return value of `.items()` is a list of 2-tuples, and we're unpacking each 2-tuple item into `some_key` and `some_val`.
