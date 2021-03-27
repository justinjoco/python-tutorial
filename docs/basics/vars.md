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
Notice that there is no `char` data type.
## Assigning variables
Like in all other programming languages, data types can be assigned to variables. Since Python is not statically typed, there is no need to type a variable before running Python code. Consider the following:
```python
countNoType = 5
```
If a variable is assigned to a literal, the interpreter will figure out the type of the variable based on the literal used, an integer in this case.
### Type hinting
In Python 3, developers can *hint* to the data type used for a variable, like so:
```python
countWithType: int = 3
```
However, this is not exactly the same as static typing; Python3 will not enforce that the literal assigned to a variable will be the same as the type hint. For example, a valid statement that can run with no Python interpreter errors can be
```python
countWithType: int = "hello"
```
## Operators
In Python, there are different operators between two operands: arithmetic, logical, and assignment.
### Arithmetic
Python supports arithmetic between two variables:

- Addition: `+` : `x + y`
- Subtraction: `-`:  `x - y`
- Multiplication: `*`:  `x * y`
- Division: `/`: `x / y`
- Floor (Integer) Division `//`: `x // y`
- Modulo `%`: `x % y`
- Exponent `**`: `x**y`

### Logical 
Comparison operators between two operands are supported

- Less than `<`: `x < y`
- Less than or equal to `<=`: `x <= y`
- Equal to `==`: `x == y`
- Greater than or equal to `>=`: `x >= y`
- Greater than `>`: `x > y`
- Not equal `!=`: `x != y`

### Arithmetic assignment operators
Assigning a variable the result of an arithmetic operation between the variable's previous value and another operand is supported.

- Add, then assign: `+=`: `x += y`
- Subtract, then assign `-=`: `x -= y`
- Multiply, then assign `*=`: `x *= y`
- Divide, then assign `/=`: `x /= y`
- Modulo, then assign: `%=`: `x %= y`

Unlike other languages, Python does not support the increment (ie `++`) or decrement (`--`) operators.
### Bitwise
Operations between numbers on a bit-level are supported.

- Bitwise AND `&`
- Bitwise OR `|`
- Bitwise XOR `^`
- Bitwise NOT `~`
- Bitwise left shift `<<`
- Bitwise right shift `>>`
