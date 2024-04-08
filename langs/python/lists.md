# Lists

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/)
[https://docs.python.org/3/](https://docs.python.org/3/)
___

## Lil Intro

Brackets are used to denotes lists
Mixed data types are allowed

```python
thisList = [1, 2, "apple"]
```

Items are 0-indexed:

```python
print(thisList.index(1)) #prints 0
```

Duplicates are allowed:

```python
dubs = [1, 1, 1]
```

Use the `len()` function to find out how many items are in a list:

```python
myList = [5,6,8]
print(len(myList))

# prints 3
```

## Accessing Elements

