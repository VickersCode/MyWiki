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
## Common Methods

|Method|Description|
|---|---|
|[append()](https://www.w3schools.com/python/ref_list_append.asp)|Adds an element at the end of the list|
|[clear()](https://www.w3schools.com/python/ref_list_clear.asp)|Removes all the elements from the list|
|[copy()](https://www.w3schools.com/python/ref_list_copy.asp)|Returns a copy of the list|
|[count()](https://www.w3schools.com/python/ref_list_count.asp)|Returns the number of elements with the specified value|
|[extend()](https://www.w3schools.com/python/ref_list_extend.asp)|Add the elements of a list (or any iterable), to the end of the current list|
|[index()](https://www.w3schools.com/python/ref_list_index.asp)|Returns the index of the first element with the specified value|
|[insert()](https://www.w3schools.com/python/ref_list_insert.asp)|Adds an element at the specified position|
|[pop()](https://www.w3schools.com/python/ref_list_pop.asp)|Removes the element at the specified position|
|[remove()](https://www.w3schools.com/python/ref_list_remove.asp)|Removes the item with the specified value|
|[reverse()](https://www.w3schools.com/python/ref_list_reverse.asp)|Reverses the order of the list|
|[sort()](https://www.w3schools.com/python/ref_list_sort.asp)|Sorts the list|
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

## List Comprehension

Syntax
```python
myList = [expression for item in iterable if condition == True]
```

Use list comprehension for short syntax
```python
myList = [1,2,3,4,5]
[print(x) for x in myList]
```

## Sorting Lists

Using `myList.sort()` will sort the list alphanumerically, ascending.

To sort descending, use `myList.sort(reverse = True`

Be careful with case sensitivity, use `.sort(key = str.lower)` if there is more than one case. 

`list.reverse()` is the quickest way to reverse the order of a list. 
##### Custom Sorting

By using the argument, `key = function`, we can sort in an unlimited amount of ways
This example was grabbed from w3schools.
Notice the function sorts the list and keeps the original values. It does not sort the evaluated values of `abs(n - 50)` into the list
```python
def myfunc(n):
  return abs(n - 50)

thislist = [100, 50, 65, 82, 23]

thislist.sort(key = myfunc)

print(thislist)
# [50, 65, 23, 82, 100]
```

## Copying Lists

> [!warning]
> Do not copy lists by using `list2 = list1`

This points the memory address of list2 to the memory address of list1. So, whenever you change list1, list2 will also change. Instead, we use the `copy()` method. 
```python
myList = [1,2,3,4,5]
newList = myList.copy()
```

or the `list()` method. 
```python
myList = [1,2,3,4,5]
newList = list(myList)
```

## Joining Lists

Or, concatenation
```python
list1 = [1,2,3]
list2 = [4,5,6]

list3 = list1 + list2
# [1,2,3,4,5,6]
```

`append()` adds an item to this list, so we can use a for loop to add one list to another
```python
list1 = [1,2,3]
list2 = [4,5,6]

for x in list2:
	list1.append(x)
```

`extend()` does not need a for loop
```python
list1 = [1,2,3]
list2 = [4,5,6]

list1.extend(list2)
```

