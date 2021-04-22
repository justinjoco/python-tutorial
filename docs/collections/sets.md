Code sample link: <https://replit.com/@jjoco/python-sets>

## why to use set
## Creating set
```python
#Create empty set
init_set = set()
print(init_set)

#Create a set from an initial list
set_from_list = set(["hello", "world", "set"])
print(set_from_list)
```
## Checking contains
```python
#Check if element exists in set
if "hello" in set_from_list:
  print("hello is seen" )
```
## Pushing to set
```python
set_from_list.add("added_elem")
print(set_from_list)
```

## Iterating
```python
for elem in set_from_list:
  print(elem)
```

## Clear set
```python
set_from_list.clear()
```
