Code sample link: <https://replit.com/@jjoco/python-lambdas>

Lambda functions can be thought of short-term, concise, impromptu functions that are intended to be thrown away after one or a couple of uses.
## Why use lambda functions
Lambdas are commonly used in other functions that have functions as parameters (ie higher-order functions).
## Creating a standalone-lambda function
You can create lambda functions to implement very concise one-line functions. Use the keyword `lambda` to create a function.
Syntax:
```python
lamdba_func = lambda args: return_value
```

Let's go over a more concrete example:
```python
double_funct = lambda x: x * 2
print(double_funct(5))

add_funct = lambda x, y: x + y
print(add_funct(5, 7))
```
In the above, we create two lambda functions, whose names are `double_funct` and `add_funct`. These lambda functions are used like any other function. In this example, we're using `lambda` to implement very short functions, whose scope is narrowed to the current code block.

## Creating a lambda generator function
What is cool is that we can create a lambda generator, which we can use to easily create more lambda functions on demand:
```python
def exp_funct(n):
  return lambda x : x ** n

square_funct = exp_funct(2)
print(square_funct(5))

cube_funct = exp_funct(3)
print(cube_funct(5))
```
Here, we are using `exp_funct` to generate lambda functions that raise an input to the n-th power.

## Using lambda functions as inputs to other functions
Lambda functions are commonly used as inputs to functions, whose required (or optional) parameters are also functions.

Take the following example:
```python
card_map = {"king": 13, "jack": 11, "queen": 12, "ace": 1}
print(card_map) # {'king': 13, 'jack': 11, 'queen': 12, 'ace': 1}

sorted_list = sorted(card_map.items(), key=lambda item: item[1])
print(sorted_list) # [('ace', 1), ('jack', 11), ('queen', 12), ('king', 13)]

sorted_map = dict(sorted_list)
print(sorted_map) # {'ace': 1, 'jack': 11, 'queen': 12, 'king': 13}
```
Here, we are using a lambda function in `sorted` to define how to sort the key values pairs in `card_map`. Specifically, we're sorting key-value pairs in `card_map` by the values. Then we're taking the list of 2-tuples in `sorted_list` and turning it into a dictionary.