# Lists

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/)
[https://docs.python.org/3/](https://docs.python.org/3/)
___

## Lil Intro

Brackets are used to denotes lists
Mixed data types are allowed in Python

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

Use index notation:
(negative numbers start with the last entry, beginning with -1. There is no -0.)

```python 
myList = ['a','b','c','d','e']
print(myList[0]) #prints 'a'
```

#### Using Ranges

If we used `print(myList[1:3])` on myList, we would get the list `['b','c']` because the 1 is inclusive and the 3 is not.

#### Checking Existance
Use an if in.

```python
myList = ["turtle", "bear", "dog"]
if "dog" in myList:
	print("True")
```


## Changing List Items

For a single item, just use the index:
```python
myList = [1,2,3]
myList[0] = 3 #[3,1,3]
```

For multiple, grouped together changes, use a range of indexes:
```python
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]  
thislist[1:3] = ["blackcurrant", "watermelon"]  
#['apple', 'blackcurrant', 'watermelon', 'orange', 'kiwi', 'mango']
```

However, if we insert more items than we remove, they will just get pushed in to the list.
```python
myList = [1,2,3]
myList[1:2] = [3,1]
# [1,3,1,3]
```

