## why to use dictionaries
## create dict
```python
my_map = {}
```
## setting dict elements
```python
my_map["jack"] = 11
my_map["queen"] = 12
my_map["king"] = 13 
```
## getting dict element
```python
king_value = my_map["king"] 
king_value_with_get = my_map.get("king") 
```
## iterate through dict elements

### via dict -> each element is a tuple (key, value)

### via .items()
```python
for key, value in my_map.items():
    #Do stuff
```

### via .keys()

### via .values()

## delete dict key val pair

