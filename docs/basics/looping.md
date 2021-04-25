Code sample link: <https://replit.com/@jjoco/python-looping>

Looping in Python is used to execute a given set of code repeatedly. There are two ways to loop in Python: `for` loops and `while` loops.

## For loop
The `for` keyword is used to iterate over an sequence or some iterable type. 

The general syntax for simple `for` loops is the following:
```python
for elem in <iterable>:
    #Do stuff to elem
```
When the `for` loop iterates through the iterable, the value at a given point in the iterable is written into `elem` (which you can name to whatever you want, by the way). On each iteration, you'll be able to process each element in the iterable.

Let's go through several examples.
### Iterate through string
We can process each character in a given string:
```python
string_var = "asdfjk;"
for char in string_var:
    print(char)
'''
Prints out:
a
s
d
f
j
k
;
'''
```

### Iterate through list
Think of lists as an ordered sequence of values, like `1, 5, 6, 7` in that order. We'll go over lists in-depth in the `Lists` section under the `Collections` header.

We can iterate through each value in the list like the following:
```python
list_var = [4, 5, 6, 7]
for element in list_var:
    #Process element
```

### Iterate through a range of ints
In other languages, to iterate through lists or arrays, the most common way is to use array indices to access array values. The key is to use Python's in-built `range()` function, which returns a sequence of integers for `0` to `n-1` if you use the `range(n)` signature:
```python
for i in range(n):
    #Process i
```
But in case you want to set the sequence's start value, you can use the signature `range(start, stop)`, in which a sequence of numbers from `start` to `stop-1` is returned. If you want to include the step, as well, use `range(start, stop, step)`, which returns a sequence of numbers from `start` to `stop-1` in steps of `step`.

So, to iterate through all elements in a list via indices, you'll have to input the length of the list as the argument in the `range(n)` function:
```python
for i in range(len(list_var)):
  #  Do stuff to listVar[i]
  print(list_var[i])
```



## While loop
One can use `while` loops to execute code repeatedly. The syntax is follows:
```python
while condition:
   # Do stuff
```

So, let's say we have a counter that continues incrementing from `0` until `5`. We can write:
```python
counter = 0

while counter < 5:
    print(counter)
    counter+=1
'''
Prints out:
0
1
2
3
4
'''
```
The while continues to execute the increment statement until the counter becomes `5`, at which the program exits the while loop.

For those wondering, you can write the same `for` loop as a `while` or vice-versa. Generally, I use for-loops when iterating through something or the number of iterations can be known ahead of time; on the other hand, I use while-loops when my looping is dependent on some condition or the number of iterations is variable. For example, you shouldn't use a for-loop to write an infinite loop.
### Infinite loop
The easiest way to write an infinite loop is via a while loop:
```python
while True:
   # Do stuff forever or until break
```
You would want to use an infinite loop if your program is intended to run forever, like a server. However, you can write your infinite loop to end prematurely if some condition is met during the loop execution. In this case, you would use the `break` statement to exit the loop. You can use `break` in either a for-loop or a while-loop to exit the current loop block.

```python
while True:
   # Do stuff forever or until break
   x = int(input("Enter a number: "))

   if x == -1:
       break
```
In the above example, the while-loop executes forever, asking the user to input a number. Assuming the user always inputs a number, the while-loop ends if the user inputs a `-1`.