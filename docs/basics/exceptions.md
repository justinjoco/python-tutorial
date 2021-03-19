## Basic try-except
```python
try:
    #Do stuff
except:
    #Do when an exception is thrown
```

```python
try:
    #Do stuff
except Exception as err: #Creates alias for Exception object, which dev can do stuff with
    #Do when an exception is thrown
```
## Try-except with muiltiple excepts
```python
try:
    #Do stuff
except ValueError:
    #Do when ValueError exception is thrown
except KeyError:
    #Do when KeyError exception is thrown
```

### Try-except with multiple exception types on one line
```python
try:
    #Do stuff
except ValueError, KeyError:
    #Do when ValueError or a KeyError exception is thrown
except ZeroDivisionError:
    #Do when ZeroDivisionError exception is thrown
except Exception:
    #Do when any other exception is thrown
```


### Finally
```python
try:
    #Do stuff
except ValueError, KeyError:
    #Do when ValueError or a KeyError exception is thrown
except ZeroDivisionError:
    #Do when ZeroDivisionError exception is thrown
finally:
    #Do stuff when try or except is finished
```