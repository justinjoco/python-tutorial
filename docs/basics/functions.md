Code sample link: <https://replit.com/@jjoco/python-functions>

Functions are like any mathematical function: you put something in, the function does something with your input, and you get something out. In Python, the keyword for defining a function is `def`, followed by a function name with parameters.
## Defining a function
```python
def function_name(input1 , ...):
   # Do stuff
```

Function inputs and outputs need not have type hints; however, it is generally good code convention to have types hinted, anyway:
```python
def function_name(input1: type1 , input2: type2 ...) -> return_type:
   # Do stuff
```


## Calling a function
To call a function, use the following syntax
```python
function_name(input1, input2)
```
What this is doing is invoking a function to do work on the given inputs. If the function is set to return some output, then the calling function can retrieve the output value like so:
```python
var_1 = function_name(input1, input2)
```
Then, the dev can use the value set in var_1 to do whatever they want.

Let's go through a more concrete example. Let's say I wanted to create a function that doubled the original value inputted. It's obviously bad practice to have a function name be something vague like 
```python
def a():
    #Do stuff
```

It is very good coding practice to be precise with your function names, especially in bigger projects. Let's implement the doubling function:
```python
def double(x):
    return x*2
```
We take an input `x` value and return `x` multipled by two. We can call `double` somewhere else, like the following:
```python
doubled = double(5)
# doubled == 10
```
For those wondering, you can call a given function within itself:
```python
def some_function(x):
    .
    .
    .
    some_function(x)
```
This is called a recursive function, in which a function calls itself at some point within its implementation. However, I will not be going over these type of functions in this tutorial.