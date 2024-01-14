# Basic Python

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)
___

### Print statements are great for debugging
```python
print("Hello World")
```
Gotta stick with the cliche.

#### Variables
```python
var = "string"
var = 1
var = 1.234
var = True or False
var = [list]
```

We can get the variable's data type using
```python
print(type(var))
```

These are all of the built in data types

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


We can also use one line to assign multiple variables
```python
x, y, z = 1, 2, 3
i, j, k = 0 #Assigns 0 to all three variables
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

