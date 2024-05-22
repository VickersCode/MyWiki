# Lists

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/)
[https://docs.python.org/3/](https://docs.python.org/3/tutorial/datastructures.html)
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

However, if we insert more items than we remove, they will just get pushed in to the list. The reverse happens if we input less than we removed.
```python
myList = [1,2,3]
myList[1:2] = [3,1]
# [1,3,1,3]
```

## Add/Remove List Items

use `insert()` to just add something to certain index without replacing.
```python
myList = [4,2,1]
myList.insert(1, 3)
# [4,3,2,1]
```

the `append()` method adds an item to the end of a list.

Use `extend()` to append another list to a list. This can be any iterable object like tuples, dictionaries, etc. 
```python
myList = [1,2,3]
myTuple = (4,5)
myList.extend(myTuple)
# [1,2,3,4,5]
```

Use the `remove()` method to remove a specific item from a list. If there are more than one of the intended item, only the first will be removed. 
```python
myList = [1,1,2,3,4,5]
myList.remove(1)
# [1,2,3,4,5]
```

The `pop()` method can be used to remove specific indices. If no index is provided, the method will remove the last item.
```python
# pop by index
myList = [1,1,2,3,4,5]
myList.pop(1)
# [1,2,3,4,5]

# pop without index
myList = [1,1,2,3,4,5]
myList.pop()
# [1,1,2,3,4]

```

The `del` keyword can delete entire lists, or items by index. 
```python
del myList
del myList[0]
```

Finally, the `clear()` method empties a list. There is still a list, it's just empty. 

## Looping 

Loop through each item in a list:
```python
myList = [1,2,3,4]
for x in myList:
	print(x)
```

Loop by index number. We can use the `range()` and `len()` functions
```python
myList = [1,2,3,4,5]
for i in range(len(myList)):
	print(myList[i])
```

There is an entire while loop chapter, but here is a quick example for lists. Always ensure the loop has a breaking point.
```python
myList = [1,2,3,4,5]
i = 0 #incrementer
while i < len(myList):
	print(myList[i])
	i = i + 1
```

