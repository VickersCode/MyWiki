# Tuples

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/python_tuples.asp)
[https://docs.python.org/3/](https://docs.python.org/3/)
___
## Intro

Tuples are like a list, except they are immutable and ordered. Duplicate values and multiple value types are allowed.

If declaring a tuple with one item, python will only recognize it as a tuple if there is a comma after the item.
`thisTuple = ("John",)`

#### Constructor
```python
myTuple = tuple((1,2,3))
# Yes, the double brackets are necessary
```

`len()` determines number of entries
`count()` returns instances of a specific value
`index()` returns the index of a value

___
## Updating Tuples

#### Unpacking Tuples (This one is kinda common)
When we assign the values into a tuple, we are packing it. Unpacking is a way to assign the values of the tuple to variables using the example: `x, y, z = myTuple` 
```python
myTuple = (5, 8, 3)
HP, ATTCK, DEF = myTuple
```

#### Changing Values
Yes, tuples are immutable, but there is a workaround. We can convert the tuple into a list, change the list, and then change it back into a tuple. Like so
```python
myTuple = (1,2,3,6,5)
tupleList = list(myTuple)
tupleList[3] = 4
myTuple = tuple(tupleList)
# returns (1,2,3,4,5)
```

#### Adding Items
Again, convert to list then back to tuple
```python
myTuple = (1,2,3,4)
tupleList = list(myTuple)
tupleList.append(5)
myTuple = tuple(tupleList)

# returns (1,2,3,4,5)
```

Or concatenate a new tuple
```python
myTuple = (1,2,3,4)
x = (5,) # remember the comma
myTuple += x
```

#### Removing Items
Again, tuple -> list -> tuple
```python
myTuple = (1,2,3,4,5,6)
tupleList = list(myTuple)
tupleList.remove(6)
myTuple = tuple(tupleList)

# returns (1,2,3,4,5)
```

Using `del myTuple` well remove the tuple from memory completely

#### Asterisks
When unpacking a Tuple, if one of the variables has an asterisk, it is meant to take the overflow of the tuple is longer than the amount of variables given. If the variable with the asterisk is not at the end of the "list of variables", python will fill that variable with a list until there are enough for each of the rest of the variables.
```python
myTuple = (1,2,3,4,5,6)
(george, will, (*harry) = myTuple

print(george) # 1
print(will)   # 2
print(harry)  # [3,4,5,6]
```

#### Joining Tuples
This is the same as joining lists. Use concatenation. Can multiply a tuple into a new variable as well.