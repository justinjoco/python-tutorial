Code sample link: <https://replit.com/@jjoco/python-exceptions>
Let's say you wanted to execute some block of code, that could potentially throw an error (specifically called Exceptions). Normally, if a block of code throws an error, the currently executing program would crash. To prevent this from happening, one can wrap such block of code using `try-except` blocks, which are `try-catch` blocks in many other languages.

## Basic try-except
The syntax for `try-except` is the following:
```python
try:
    #Do stuff
except:
    #Do when an exception is thrown
```
The idea is that if a block of code within the `try` block throws an Exception, then the program will execute an `except` block to handle the Exception.

If the dev wants to do something with the Exception caught, then they can use the following syntax:
```python
try:
    #Do stuff
except Exception as err: #Creates alias for Exception object, which dev can do stuff with
    #Do when an exception is thrown
```

If it's possible that the try block can throw different types of Exceptions, then the `try-except` can have multiple `except` blocks, which execute when a specific Exception type is thrown:
## Try-except with muiltiple excepts
```python
try:
    #Do stuff
except ValueError:
    #Do when ValueError exception is thrown
except KeyError:
    #Do when KeyError exception is thrown
```

The dev can also handle different Exceptions in the same `except` block like the following:
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

## Finally

Finally, there's the `finally` block, which generally executes right before the `try` statement completes:
```python
try:
    #Do stuff
except ValueError, KeyError:
    #Do when ValueError or a KeyError exception is thrown
except ZeroDivisionError:
    #Do when ZeroDivisionError exception is thrown
finally:
    #Do stuff before try finishes
```

So if a `try-finally` block looks like this:
```python
try:
    raise Exception
finally:
    print("Finally clause here")
```
Then, standard output would show `Finally clause here` followed by the `Exception`.

There are other complexities involving this `finally` block, but that's out of the scope of this tutorial.
