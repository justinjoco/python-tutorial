Code sample link: <https://replit.com/@jjoco/python-syntax>

One of Python's main features is its readability. Consider the following pseudocode:

```{r, eval = FALSE}
if there is no milk and the store is open,
  buy milk
```
The above pseudocode can be translated into the following Python code:
```python
if not have_milk and is_store_open:
  buy_milk()
```

Compared to to other languages, there is no curly brackets to wrap code code blocks; instead, Python interprets code blocks via colons and indentation.
## Indentation
Statements are interpreted in Python based on how indented they are. Unlike other programming languages in which indentation is technically optional, indentation in Python is used to interpret blocks of code. Take the following example:
```python
if True:
  print("Outside true")
  if True:
    print("Nested true")
    if True:
      print("Nested nested true")
```
As you can see, nested indentation shows nested blocks of code. Running improperly indented code will cause Python interpreter errors.


## Comments
Like in other languages, comments are implemented in Python to denote statements that are not to be interpreted and are for developer documentation. Single line comments are written like the following with the `#` prefix:
```python
# This is a single line comment
```
Multiline comments are wrapped with triple single or double quotes:
```python
'''
This is a multiline
comment with single quotes
'''
"""
This is a multiline
comment with double quotes
"""
```

