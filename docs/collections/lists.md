Code sample link: <https://replit.com/@jjoco/python-lists>

In Python, arrays are `lists` and function similarly to `ArrayLists` in Java. They are used to keep a number of values to be used later on for processing.

## Empty list
To create an empty list, one can use square brackets `[]`, like so:
```python
my_list = []
```
This empty list, as the name suggests, contains no elements within it. This is can be used to initalize a list that will be modified later on.

One can also type hint a list; to type hint the list of strings, one can write the following
```python
from typing import List

.
.
.
my_list : List[str] = []
```
## populated list
A list need not have to be empty every time when intialized. Lists can be initialized with elements inside, like so:
```python
my_list = ["hello", "there", "my", "name", "is"]
```

Unlike strictly typed languages, Python allows lists to contain more than one type. For example, the following multi-type list is valid in Python:
```python
my_list = ["hello", 0, 1.5 , "name", True]
```
The above example contains strings, an integer, a float, and a boolean; strictly-typed languages forbid multi-type arrays and will throw a compile time error (if an array is initalized like above) or during runtime (if an element to be added is not of the same type as that already in the array).

Even if a developer type hints, the multi-type list is still a valid list, like so:
```python
my_list: List[str] = ["hello", 0, 1.5 , "name", True]
```
If it is critical that a list is not to contain multiple types, do not rely on the Python interpreter out-of-the-box to prevent multi-type lists.
## iterate through list
The Python way of iterating through a list is very similar to how other languages use iterator looping.

```python
for elem in my_list:
    #Do stuff to elem
```

Let's say I wanted to print out the elements in a given list. You can do the following:
```python
hello_list = ["hello", "world", "!"]
for elem in hello_list:
  print(elem)
'''
STDOUT:
hello
world
!
'''
```


## Iterate via enumerate 
Sample: <https://replit.com/@jjoco/python-enumerate>
Python has a special function called `enumerate`. `enumerate`'s parameter is a list, and it returns an *enumeration* of the list that allows a dev to loop through a list's indicies and elements simultaneously. 

```python
my_list = [2, 21, 7, 8, 65 ,9 , 0]

for index, value in enumerate(my_list):
  print("Index: ", index)
  print("Value: ", value)
'''
STDOUT:
Index:  0
Value:  2
Index:  1
Value:  21
Index:  2
Value:  7
Index:  3
Value:  8
Index:  4
Value:  65
Index:  5
Value:  9
Index:  6
Value:  0
'''
```

In case the value of an element does not matter, a dev can use an underscore `_` in place of the value to denote a `dont-care`.
```python
for jndex, _ in enumerate(my_list):
  print("jndex: ", jndex)
'''
STDOUT:
jndex:  0
jndex:  1
jndex:  2
jndex:  3
jndex:  4
jndex:  5
jndex:  6
'''
```

Likewise if the index of an element does not matter, use an underscore in place of the index.
```python
for _, walue in enumerate(my_list):
  print("Value: ", walue)
'''
Value:  2
Value:  21
Value:  7
Value:  8
Value:  65
Value:  9
Value:  0
'''
```
## Setting list element
A dev can set the value of an element as a given index like the following.

```python
my_list = [2, 21, 7, 8, 65 ,9 , 0]
my_list[3] = 5
```
The above line sets the element at index 3 (whose value is 8) to 5. Keep in mind that if the input index is outside the scope of the list, then Python will throw an `IndexOutOfRangeException`. 
## Get list element
To get an element at a given index, use the following syntax:
```python
elem = my_list[index]
```
Let's say we wanted to print the value of `my_list = [2, 21, 7, 8, 65 ,9 , 0]` at index 2, we can write:
```python
print(my_list[2])
#Output = 7
```


## iterate through list via range
Devs can also iterate through a list via indices, but they still need to use the iterator syntax mentioned earlier using a special function `range(n)`. `range(n)` returns a sequence of numbers from `0` to `n-1`. Like most languages, Python list indexing starts from `0`.
To iterate through an entire list using `range`, input the length of the list as its parameter.
```python
bigger_list = [1,5,8,3,8,0,3]

for i in range(len(bigger_list)):
  print(bigger_list[i])
```
Try not to iterate through lists like this too often unless using the array indicies are used meaningfully.

## Append list element
To append to the end of a list, use the list method `append(elem)` function to add  `elem` to the end of a given list.
```python
bigger_list = [1,5,8,3,8,0,3]

bigger_list.append(7)
# bigger_list == [1,5,8,3,8,0,3,7]
```
## Insert list element
To insert an element at a given index, use list method `insert(index, value)` to insert `value` at index `index`:
```python
bigger_list = [1,5,8,3,8,0,3]

bigger_list.insert(1,4)
# bigger_list == [1,4,5,8,3,8,0,3]
```

## Pop list element
To remove the last element of a given list (or "pop" it), use the `pop()` function. Note that this function also returns the item popped.
```python
bigger_list = [1,5,8,3,8,0,3]

popped_item = bigger_list.pop()
# bigger_list == [1,5,8,3,8,0]
# popped_item == 3
```