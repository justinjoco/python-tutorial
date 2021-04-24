Code sample link: <https://replit.com/@jjoco/python-dictionaries>

## Why to use dictionaries?
## Creating a dictionary
```python
my_map = {}
```
## Setting dictionary elements
```python
my_map["jack"] = 11
my_map["queen"] = 12
my_map["king"] = 13 
```
## Getting a dictionary element
```python
king_value = my_map["king"] 
king_value_with_get = my_map.get("king") 
```
## Iterate a through dictionary elements

### Via simple iteration
```python
for key in my_map:
  print(my_map[key])
```
### Via .items() -> each element is a tuple (key, value)
```python
for item in my_map.items():
  print("Item: ", item)
```

```python
for key, value in my_map.items():
    #Do stuff
```

### Via .keys()
```python
for key in hello_map.keys():
  print(key)
```
### Via .values()
```python
for value in hello_map.values():
  print(value)
```
### Deleting a dictionary key-value pair
```python
del my_map["king"]
```
