# Sets

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/)
[https://docs.python.org/3/](https://docs.python.org/3/)
___
## Common Methods
| Method                                                                                                    | Shortcut                                                                       | Description                                                                    |
| --------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| [add()](https://www.w3schools.com/python/ref_set_add.asp)                                                 |                                                                                | Adds an element to the set                                                     |
| [clear()](https://www.w3schools.com/python/ref_set_clear.asp)                                             |                                                                                | Removes all the elements from the set                                          |
| [copy()](https://www.w3schools.com/python/ref_set_copy.asp)                                               |                                                                                | Returns a copy of the set                                                      |
| [difference()](https://www.w3schools.com/python/ref_set_difference.asp)                                   | [-](https://www.w3schools.com/python/ref_set_difference.asp)                   | Returns a set containing the difference between two or more sets               |
| [difference_update()](https://www.w3schools.com/python/ref_set_difference_update.asp)                     | [-=](https://www.w3schools.com/python/ref_set_difference_update.asp)           | Removes the items in this set that are also included in another, specified set |
| [discard()](https://www.w3schools.com/python/ref_set_discard.asp)                                         |                                                                                | Remove the specified item                                                      |
| [intersection()](https://www.w3schools.com/python/ref_set_intersection.asp)                               | [&](https://www.w3schools.com/python/ref_set_intersection.asp)                 | Returns a set, that is the intersection of two other sets                      |
| [intersection_update()](https://www.w3schools.com/python/ref_set_intersection_update.asp)                 | [&=](https://www.w3schools.com/python/ref_set_intersection_update.asp)         | Removes the items in this set that are not present in other, specified set(s)  |
| [isdisjoint()](https://www.w3schools.com/python/ref_set_isdisjoint.asp)                                   |                                                                                | Returns whether two sets have a intersection or not                            |
| [issubset()](https://www.w3schools.com/python/ref_set_issubset.asp)                                       | [<=](https://www.w3schools.com/python/ref_set_issubset.asp)                    | Returns whether another set contains this set or not                           |
|                                                                                                           | [<](https://www.w3schools.com/python/ref_set_issubset.asp)                     | Returns whether all items in this set is present in other, specified set(s)    |
| [issuperset()](https://www.w3schools.com/python/ref_set_issuperset.asp)                                   | [>=](https://www.w3schools.com/python/ref_set_issuperset.asp)                  | Returns whether this set contains another set or not                           |
|                                                                                                           | [>](https://www.w3schools.com/python/ref_set_issuperset.asp)                   | Returns whether all items in other, specified set(s) is present in this set    |
| [pop()](https://www.w3schools.com/python/ref_set_pop.asp)                                                 |                                                                                | Removes an element from the set                                                |
| [remove()](https://www.w3schools.com/python/ref_set_remove.asp)                                           |                                                                                | Removes the specified element                                                  |
| [symmetric_difference()](https://www.w3schools.com/python/ref_set_symmetric_difference.asp)               | [^](https://www.w3schools.com/python/ref_set_symmetric_difference.asp)         | Returns a set with the symmetric differences of two sets                       |
| [symmetric_difference_update()](https://www.w3schools.com/python/ref_set_symmetric_difference_update.asp) | [^=](https://www.w3schools.com/python/ref_set_symmetric_difference_update.asp) | Inserts the symmetric differences from this set and another                    |
| [union()](https://www.w3schools.com/python/ref_set_union.asp)                                             | [\|](https://www.w3schools.com/python/ref_set_union.asp)                       | Return a set containing the union of sets                                      |
| [update()](https://www.w3schools.com/python/ref_set_update.asp)                                           | [\|=](https://www.w3schools.com/python/ref_set_update.asp)                     | Update the set with the union of this set and others                           |
## Intro
Sets are *unordered, unchangeable, and unindexed*. This means we can never be sure in which order items appear. Sets are declared with curly brackets. Can have multiple data types.
```python
mySet = {1,2,3}
```
**Duplicate Values are not allowed and will be ignored**
**In Python, True and 1 are considered the same value, so will treated as duplicates**
**False and 0 will also be treated as duplicates**
```python
mySet = {1, 2, 3, True, 1, 2}

print(mySet)
# {1,2,3}
```

Like list comprehension, we can use set comprehension for conciseness.
```python
a = {x for x in 'abracadabra' if x not in 'abc'}
print(a)
# {'r', 'd'}
```

Since sets are unordered, we cannot access items by index. A common way to access items is through a for loop. We also check existence with the `in` or `not in` keywords.
```python
mySet = {1, 2, 3}
print(2 not in mySet)
# prints "False"
```
Items cannot be changed, but can be added.
___
## Add-Remove Items
Use the `add()` method to add a single item. `mySet.add("blue")`

The `update()` method adds items from one set to another. This can be done with any iterable (list, tuple, dictionary, etc.).
```python
mySet = {1,2,3}
anotherSet = {4,5,6}

mySet.update(anotherSet)

# {1,2,3,4,5,6}
```

To remove specific items, use the `remove()` or `discard()` methods.  If the item in the parameter does not exist, python will throw an error.
The `pop()` method will remove a random item. 
```python
mySet.remove(1)
mySet.discard(1)
mySet.pop()
```

The `clear()` method empties the set and the `del` keyword deletes the set completely. 
```python
mySet.clear()
del mySet
```
___
## Joining Sets

There are a few ways to join two or more sets.

| Method                                                                                      | Shortcut                                                               | Description                                                      |
| ------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------- | ---------------------------------------------------------------- |
| [difference()](https://www.w3schools.com/python/ref_set_difference.asp)                     | [-](https://www.w3schools.com/python/ref_set_difference.asp)           | Returns a set containing the difference between two or more sets |
| [intersection()](https://www.w3schools.com/python/ref_set_intersection.asp)                 | [&](https://www.w3schools.com/python/ref_set_intersection.asp)         | Returns a set, that is the intersection of two other sets        |
| [symmetric_difference()](https://www.w3schools.com/python/ref_set_symmetric_difference.asp) | [^](https://www.w3schools.com/python/ref_set_symmetric_difference.asp) | Returns a set with the symmetric differences of two sets         |
| [union()](https://www.w3schools.com/python/ref_set_union.asp)                               | [\|](https://www.w3schools.com/python/ref_set_union.asp)               | Return a set containing the union of sets                        |
| [update()](https://www.w3schools.com/python/ref_set_update.asp)                             | [\|=](https://www.w3schools.com/python/ref_set_update.asp)             | Update the set with the union of this set and others             |

#### Union
`union()` returns a new set with all items from both sets, except duplicates.
```python
set1 = {1,2,3}
set2 = {4,5,6}
set3 = set1.union(set2)
```
We can `union()` multiple sets as well
```python
set1 = {1,2,3}
set2 = {4,5,6}
set3 = {7,8,9}
set4 = set1.union(set2, set3)
```

The `|` operator also works. 
```python
set1 = {1,2,3}
set2 = {4,5,6}
set3 = set1 | set2

set1 = {1,2,3}
set2 = {4,5,6}
set3 = {7,8,9}
set4 = set1 | set2 | set3
```
The `|` operator only works with other sets, but `union()` can take other data types. 

#### Update
`update()` places items from one set into another. It updates a set, does not create a new one.
```python
set1 = {1,2,3}
set2 = {4,5,6}

set1.update(set2)
# {1,2,3,4,5,6}
```

#### Intersection
Keep only the duplicates
```python
set1 = {1,2,3,4,5}
set2 = {3,4,5,6,7}

set3 = set1.intersection(set2)
# {3,4,5}
```
The `&` operator also works, but only with other sets.
```python
set1 = {1,2,3,4,5}
set2 = {3,4,5,6,7}

set3 = set1 & set2
```

`intersection_update()` is like `update()`, instead of creating a new variable, we update an already existing set.
```python
set1 = {1,2,3,4,5}
set2 = {3,4,5,6,7}

set1.intersection_update(set2)
```

#### Difference
Returns a new set that contains only items from the first set that are not present in the second. 
```python
set1 = {1,2,3,4,5}
set2 = {4,5,6,7,8}

set3 = set1.difference(set2)
# {1,2,3}
```

The `-` operator also works, but only with other sets
```python
set1 = {1,2,3,4,5}
set2 = {4,5,6,7,8}

set3 = set1 - set2
```
`difference_update()` is like `update()`, instead of creating a new variable, we update an already existing set.
```python
set1 = {1,2,3,4,5}
set2 = {4,5,6,7,8}

set1.difference_update(set2)
```

#### Symmetric Difference
Keeps only the elements **not** present in both sets
```python
set1 = {1,2,3,4,5,6}
set2 = {2,4,6,8,10,12}

set3 = set1.symmetric_difference(set2)
# {1,3,5,8,10,12}
```

The `^` operator also works, but only with other sets
```python
set1 = {1,2,3,4,5,6}
set2 = {2,4,6,8,10,12}

set3 = set1 ^ set2
```
`symmetric_difference_update()` is like `update()`, instead of creating a new variable, we update an already existing set.
```python
set1 = {1,2,3,4,5,6}
set2 = {2,4,6,8,10,12}

set1.symmetric_difference_update(set2)
print(set1)
# {1,3,5,8,10,12}
```







