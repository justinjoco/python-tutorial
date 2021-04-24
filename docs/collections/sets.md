Code sample link: <https://replit.com/@jjoco/python-sets>

## Why to use set
## Creating a set
```python
#Create empty set
init_set = set()
print(init_set)

#Create a set from an initial list
set_from_list = set(["hello", "world", "set"])
print(set_from_list)
```
## Checking if a set contains an element
```python
#Check if element exists in set
if "hello" in set_from_list:
  print("hello is seen" )
```
## Pushing an element into a set
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
