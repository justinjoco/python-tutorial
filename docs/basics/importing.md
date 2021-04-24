Code sample link: <https://replit.com/@jjoco/python-importing>

If Python does not contain functionality for something you want to do, you can import libraries that implement these functions, assuming such libraries exist.
## Importing a library
To import a library, one can use the `import` keyword. Take the following example, in which`numpy`, a popular scientific computing, library  is imported.
```python
import numpy
```
Then, you can invoke the `array` function within this library, like so:
```python
numpy.array([3.5,2.4,1.0])
```
### Library aliasing
In case the library's name is too long or too vague, one can use alias the library:
```python
import numpy as np
```
Instead of using `numpy` when invoking a function, the dev can use `np` instead.
So, what would originally have been `numpy.array()` would turn into `np.array()`:
```python
np.array([3.5,2.4,1.0])
```
## Importing something from a library
You can import specific functions or constants from the imported libraries, like so
```python
from math import pi

print(pi)
```
```python
import math
print(math.pi)
```
It is a neat feature to use in case you don't want to write the library name every time you invoke a function from it.