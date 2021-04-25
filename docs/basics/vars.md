## Primitive data types
Python includes many primitive data types like many other languages.

- String
    - `str`
- Number types
    - `int`
    - `float`
    - `complex`
- Boolean types
    - `bool`

Notice that there is no `char` data type to represent a character-type.
## Assigning variables 
Code sample link: <https://replit.com/@jjoco/python-vars>

Like in all other programming languages, data types can be assigned to variables. Since Python is not statically typed, there is no need to type a variable before running Python code. Consider the following:
```python
countNoType = 5
```
If a variable is assigned to a literal, the interpreter will figure out the type of the variable based on the literal used, an integer in this case.
### Type hinting
Starting from Python 3.5, developers can *hint* to the data type used for a variable, like so:
```python
countWithType: int = 3
```
However, this is not exactly the same as static typing; Python3 will not enforce that the literal assigned to a variable will be the same as the type hint. For example, a valid statement that can run with no Python interpreter errors can be
```python
countWithType: int = "hello"
```
## Operators
Code sample link: <https://replit.com/@jjoco/python-operators>

In Python, there are different operators between two operands: arithmetic, logical, and assignment.
### Arithmetic
Python supports arithmetic between two variables:

- Addition: `+` : `x + y` --> `(5 + 2) == 7` 
- Subtraction: `-`:  `x - y` --> `(5 - 2) == 3` 
- Multiplication: `*`:  `x * y` --> `(5 * 2) == 10` 
- Division: `/`: `x / y` --> `(5 / 2) == 2.5`  
- Floor (Integer) Division `//`: `x // y` --> `(5 // 2) == 2` 
- Modulo (Remainder) `%`: `x % y` --> `(5 % 2) == 1`  
- Exponent `**`: `x**y` --> `(5 ** 3) == 125` 

### Logical 
Comparison operators between two operands are supported

- Less than `<`: `x < y` --> `(5 < 2) == False` 
- Less than or equal to `<=`: `x <= y` --> `(5 <= 2) == False` 
- Equal to `==`: `x == y` --> `(5 == 2) == False` 
- Greater than or equal to `>=`: `x >= y` --> `(5 >= 2) == True` 
- Greater than `>`: `x > y` --> `(5 > 2) == True` 
- Not equal `!=`: `x != y` --> `(5 != 2) == True` 

### Arithmetic assignment operators
Assigning a variable the result of an arithmetic operation between the variable's previous value and another operand is supported.

- Add, then assign: `+=`: `x += y` 
- Subtract, then assign `-=`: `x -= y`
- Multiply, then assign `*=`: `x *= y`
- Divide, then assign `/=`: `x /= y`
- Modulo, then assign: `%=`: `x %= y`

Unlike other languages, Python does not support the increment (ie `++`) or decrement (`--`) operators. You need to use `+=1` or `-=1` on the accumulator.
### Bitwise
Operations between numbers on a bit-level are supported.

- Bitwise AND `&`
- Bitwise OR `|`
- Bitwise XOR `^`
- Bitwise NOT `~`
- Bitwise left shift `<<`
- Bitwise right shift `>>`
