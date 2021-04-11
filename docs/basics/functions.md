Code sample link: <https://replit.com/@jjoco/python-functions>

Functions are like any mathematical function: you put something in, the function does something with your input, and you get something out. In Python, the keyword for defining a function is `def`, followed by a function name with parameters.
## Defining a function
```python
def function_name(input1 , ...):
    Do stuff
```

Function inputs and outputs need not have type hints; however, it is generally good code convention to have types hinted, anyway.
## Type hinting
```python
def function_name(input1:type1 , input2: type2 ...) -> return_type:
    Do stuff
```

To call a function, use the following syntax
## Calling a function
```python
function_name(input1, input2)
```
What this is doing is invoking a function to do work on the given inputs. If the function is set to return some output, then the calling function can retrieve the output value like so:
## Calling a function
```python
var_1 = function_name(input1, input2)
```
Then, the dev can use the value set in var_1 to do whatever they want.

Let's go through a more concrete example.