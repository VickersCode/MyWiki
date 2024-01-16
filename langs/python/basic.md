# Basic Python

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)
___

### Print statements are great for debugging
```python
print("Hello World")
```
Gotta stick with the cliche.

#### Variables and Data Types
```python
var = "string"
var = 1
var = 1.234
var = True or False
var = [list]
```

We can also use one line to assign multiple variables
```python
x, y, z = 1, 2, 3
i, j, k = 0 #Assigns 0 to all three variables
```

We can get the variable's data type using
```python
print(type(var))
```

###### Data Types

| Category | Type |
| ---- | ---- |
| Text | `str` |
| Numeric | `int, float, complex` |
| Sequence | `list, tuple, range` |
| Mapping | `dict` |
| Set | `set, frozenset` |
| Boolean | `bool` |
| Binary | `bytes, bytearray, memoryview` |
| None | `NoneType` |

Complex numbers are exactly what we think, usually denoted 'i' for the square root of negative one. In python, we use 'j'

```python
x = 3 + 5j #Complex number 'j'
```

We can convert from one type to another
```python
x = 1
y = 4.20
z = 69j

a = float(x) # 1.0
b = int(y) # 4
c = complex(x) # (1+0j)
```

I plan on having a section for libs, but we can use the random library to generate random numbers
```python
import random

x = random.randrange(1,10)
```
### Comment using '#'

```python
# This is a comment
This is not a comment
```

For multiline comments, '#' is still used for each line or we can use triple quotes, like so
```python
"""
This is 
a multiline
comment
"""
```

### Loops

In python, indentation is very impotant.

```python
for i in data:
	statement
```
```python
while True:
	statement

while i < 10:
	statement
	i ++
```

