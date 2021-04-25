Code sample link: <https://replit.com/@jjoco/python-conditionals>

Conditionals are used to decide whether to run different codeblocks given some condition(s). In Python, this can be accomplished using `if-else` statements. For those familiar with other languages, Python does not support `switch-case`, unfortunately.

## If statement
If-statements in Python are slightly different from other language syntax. Take the following example:
```python
if condition:
    #Do stuff
```
If the `condition` is satisifed (ie is `True`), then its code block is executed.

There are no parentheses surrounding the condition statement, and there are no curly braces wrapping the conditional code block. 
Code statements that belong to the `if` code block must be indented once more with respect to the `if` statement.
The following is a valid if-statement:
```python
count = 6
if count > 4:
    print("Above 4")
'''
STDOUT:
Above 4
'''
```
In the following example, since `count` is greater than `4`, the program goes into the `if` code block to execute the print statement. However, in the following example:
```python
count = 3
if count > 4:
    print("Above 4")

'''
Nothing is printed to standard output
'''
```
the program will simply skip the `if` statement since the `if` condition was not satisfied.
## Elif 
Python does not use `else if`; it uses `elif`, instead.
```python
.
.
.
elif condition:
    #Do stuff
```

An `elif` block must be after an `if` block, or else there will be runtime errors. Here's an example `if-elif` block:

```python
count = 3
if count > 4:
    print("Above 4")
elif count == 3:
    print("Equal to 3")

'''
STDOUT:
"Equal to 3"
'''
```

Here, count does not satisfy the initial `if` condition; fortunately, the `elif` condition is satisfied, and its respective code block is executed. Of course, if neither the `if` nor `elif` conditions are satisfied, any code within those blocks will be skipped.

## Else
The `else` block the block executed in a bigger `if-else` block in case neither the initial `if` condition nor the subsequent `elif` conditions are met.
The syntax for `else` is the following: 
```python
.
.
.
else:
    #Do stuff
```
Like `elif`,  an `else` block must be after an `if` block, or else there will be runtime errors. Here's an example `if-else` block:

```python
count = 3
if count > 4:
    print("Above 4")
else:
    print("Not above 4")
'''
STDOUT:
"Not above 4"
'''
```
Since the `if` condition was not satisfied, the `else` block is executed.
## Combined if-else
`if`, `elif` and `else` can be combined like so:
```python
if condition_1:
.
.
.
elif condition_2:
.
.
.
else condition_n:
    #Do stuff
```

 Here's an example of a combined `if-elif-else` block:

```python
count = 3
if count > 4:
    print("Above 4")
elif count == 4:
    print("Equal to 4")
else:
    print("Less than 4")
```
Since neither the `if` nor the `elif` conditions are satisfied, the else block is executed.

Note that `elif` and `else` blocks cannot exist on their own without belonging to a bigger `if` block.

Keep in mind that you can chain several `elif` blocks:
```python
if condition_1:
.
.
.
elif condition_2:
.
.
.
elif condition_3:
.
.
.
elif condition_4:
.
.
.
else condition_n:
    #Do stuff
```
Here's an example with multiple `elif`'s choosing what letter grade to print out given a test grade:
```python
test_grade = 70
if test_grade >= 90:
    print("A")
elif test_grade >= 80:
    print("B")
elif test_grade >= 70:
    print("C")
elif test_grade >= 60:
    print("D")
else:
    print("F")
'''
STDOUT:
C
'''
```

## Multiple condition checking
In Python, you can check multiple conditions in an `if` or `elif` before deciding to execute its respective code block. Important keywords are logical operators `and`, `or`, and `not`. 

### `and`
If you want two conditions to be met before executing a block, use the `and` keyword (`&&` in other languages).

Syntax:
```python
if condition_1 and condition_2:
    #Do stuff
```
Let's say we wanted if I should order takeout based on my energy levels and the amount of food I already have in my fridge:
```python
energy_levels = 20
fridge_content = 10
if energy_levels < 30 and fridge_content < 30 :
    print("Order delivery")

'''
STDOUT
Order delivery
'''
```
Since both conditions are satisfied, the `if` block is executed. Because I'm too low energy and don't have enough stuff in my fridge, I decide to order takeout. 

### `or`
If you want either of two conditions to meet before executing a code block, use `or`  (`||` in other languages). 

Syntax:
```python
if condition_1 or condition_2:
    #Do stuff
```
In the following example, I decide if I should rest depending on the period of the day and my energy levels.
```python
energy_levels = 5
period_of_day = "afternoon"
if period_of_day == "midnight" or energy_levels < 10 :
    print("Go rest")
'''
STDOUT
Go rest
'''
```
In the above example, even though only one of the conditions was satisfied, the `if` block is executed. Even though it's the afternoon, my energy levels are low enough, such that I decide to rest.
### `not`
If you don't want a condition to be met before executing a code block, use `not`  (`!` in other languages).

Syntax:
```python
if not condition:
    #Do stuff
```
To translate the decision to go outside only if the weather condition is not raining, we can do the following:
```python
weather = "sunny"
if not weather == "raining":
    print("Go outside")
'''
STDOUT
Go outside
'''
```
Obviously, if I initially set `weather = "raining"`, then that code block would not execute.

### Mixing multiple logical operators
You can have multiple logical operators in the same conditional line; use parentheses to denote which logical comparisons should take priority over others; an abstract example can look like:
```python
if (condition_1 or condition_2) and (condition_3 or condition_4):
    #Do stuff
```
Or look like 
```python
if (condition_1 and condition_2) or (condition_3 or condition_4):
    #Do stuff
```
In both of these examples, the result of the parentheses are calculated first, then the results are compared:
```python
if condition_1_2 or condition_3_4:
    #Do stuff
```
 This example can continue ad infintum.