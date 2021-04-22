Code sample link: <https://replit.com/@jjoco/python-dictionaries>

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
```python
for key in my_map:
  print(my_map[key])
```
### via dict -> each element is a tuple (key, value)
```python
for item in my_map.items():
  print("Item: ", item)
```

```python
for key, value in my_map.items():
    #Do stuff
```

### via .keys()
```python
for key in hello_map.keys():
  print(key)
```
### via .values()
```python
for value in hello_map.values():
  print(value)
```
## delete dict key val pair
```python
del my_map["king"]
```
