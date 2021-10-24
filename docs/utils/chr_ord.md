Code sample link: <https://replit.com/@justinjoco/python-chr-ord>

These utility functions are useful for coverting unicode characters to and from their code point values. This table contains some, but not all, of the character-code point mappings: <https://www.rapidtables.com/code/text/ascii-table.html>

## `chr`
The `chr` function takes an integer argument and returns the appropriate unicode character for that number. 
```python
chr(61) == '='
chr(100) == 'd'
chr(101) == 'e'
chr(102) == 'f'
chr(103) == 'g'

```

## `ord`
The `ord` function takes a unicode string argument and returns the corresponding code point value.
```python
ord("(") == 40
ord("<") == 60
ord("A") == 65
ord("9") == 57
```