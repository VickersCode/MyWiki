# Dictionaries

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/)
[https://docs.python.org/3/](https://docs.python.org/3/)
___
#### Quick Links (on this page)
- [Common Methods](#Common-Methods)
- [Intro](#Intro)
- [Accessing Items](#Accessing-Items)
- [Changing/Adding Values](#Changing-or-Adding-Values)
- [Removing Items](#Removing-Items)
- [Loops](#Looops)
- [Copying Dictionaries](#Copying-Dictionaries)
- [Nested Dictionaries](#Nested-Dictionaries)
___
## Common Methods
|Method|Description|
|---|---|
|[clear()](https://www.w3schools.com/python/ref_dictionary_clear.asp)|Removes all the elements from the dictionary|
|[copy()](https://www.w3schools.com/python/ref_dictionary_copy.asp)|Returns a copy of the dictionary|
|[fromkeys()](https://www.w3schools.com/python/ref_dictionary_fromkeys.asp)|Returns a dictionary with the specified keys and value|
|[get()](https://www.w3schools.com/python/ref_dictionary_get.asp)|Returns the value of the specified key|
|[items()](https://www.w3schools.com/python/ref_dictionary_items.asp)|Returns a list containing a tuple for each key value pair|
|[keys()](https://www.w3schools.com/python/ref_dictionary_keys.asp)|Returns a list containing the dictionary's keys|
|[pop()](https://www.w3schools.com/python/ref_dictionary_pop.asp)|Removes the element with the specified key|
|[popitem()](https://www.w3schools.com/python/ref_dictionary_popitem.asp)|Removes the last inserted key-value pair|
|[setdefault()](https://www.w3schools.com/python/ref_dictionary_setdefault.asp)|Returns the value of the specified key. If the key does not exist: insert the key, with the specified value|
|[update()](https://www.w3schools.com/python/ref_dictionary_update.asp)|Updates the dictionary with the specified key-value pairs|
|[values()](https://www.w3schools.com/python/ref_dictionary_values.asp)|Returns a list of all the values in the dictionary|
___
## Intro

Dictionaries are ordered and changeable. They are made of key:value pairs. No duplicate keys. 

```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}
```

Yes, we can use dict comprehension :)
```python
myDict = {x: x**2 for x in (2, 4, 6)}

print(myDict)
# {2: 4, 4: 16, 6: 36}
```

if each key is a simple string, use keyword arguments
```python
dict(sape=4139, guido=4127, jack=4098)
{'sape': 4139, 'guido': 4127, 'jack': 4098}
```

Get the number of entries using the `len()` method.

Values can be any data type.

If you want to use a constructor, use the `dict()` constructor
```python
myDict = dict(name = "Pikachu", type = "Electric", hp = 55)

print(myDict)
# {'name': 'Pikachu', 'type': 'Electric', 'hp': 55}
```

> [!warning]
> As of Python 3.7, dictionaries are ordered. Previous versions are unordered.

___

## Accessing Items

To get the value, refer to the dictionary putting the key in brackets
```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}

x = myDict["name"]
```

Or use the `.get()` method: `x = myDict.get("name")`

##### Return a list of keys
by using `x = myDict.keys()`
This will be all the keys stored in the dictionary

##### Return a list of values
by using `x = myDict.values()`

##### Return a list of key:value pairs in tuples
using the `.items()` method
```python
myDict = {
  "name": "Charles",
  "profession": "Driver",
  "year": 2024
}

x = myDict.items()

print(x)

# dict_items([('name', 'Charles'), ('profession', 'Driver'), ('year', 2024)])
```
___
## Changing or Adding Values

There are two ways to change values. For both, if the key does not exist, a new key:value pair will be added.
The first is to use bracket notation
```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}

myDict["hp"] = 40
```
The second is to use the `update()` method.
```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}

myDict.update({"hp": 40})
```
___
## Removing Items
Use `.pop()` to remove key:value pair by key name.
```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}

myDict.pop("type")
# {"name": "Pikachu", "hp": 55}
```
`.popitem()` will remove the most recently inserted item. No parameter needed.

`del` keyword used with the dict and key is another way to remove specific items. Careful, if we don't specify a key, the whole dict will be deleted.
```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}

del myDict["type"]
```
`.clear()` will empty everything in the dictionary. 
___
## Loops

We can use for loops to get all keys, values, or pairs. 

Keys (Two Methods)
```python
for x in myDict:
	print(x)

#OR

for x in myDict.keys():
	print(x)
```

Values (Two Methods)
```python
for x in myDict:
	print(myDict[x])

# OR

for x in thisdict.values():
	print(x)
```

Pairs
```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}

for x, y in myDict.items():
	print(x, y)

# name Pikachu
# type Electric
# hp   55
```
___
## Copying Dictionaries

>[!Warning]
>Do not uses `dict1 = dict2` to copy a dictionary. Changes made in dict1 will be made in dict2

Use `.copy()` or `.dict()`
```python
myDict = {
	"name": "Pikachu",
	"type": "Electric",
	"hp": 55
}

newDict = myDict.copy()

# OR

newDict = dict(myDict)
```
___
## Nested Dictionaries

Yes, we can have dictionaries within dictionaries.
```python
myDict = {
	"Pikachu" : {
		"type": "electric",
		"hp": 55
	}
	"Squirtle" : {
		"type": "water",
		"hp": 55
	}
	"Bulbasaur" : {
		"type": "grass",
		"hp": 55
	}
}


# Can also be written like so, to create dictionaries out of existing dictionaries.


pikachu = {
	"type": "electric",
	"hp": 55
}
squirtle = {
	"type": "water",
	"hp": 55
}
bulbasaur = {
	"type": "grass",
	"hp": 55
}

myDict = {
	"Pikachu" : pikachu,
	"Squirtle" : squirtle,
	"Bulbasaur" : bulbasaur
}
```

To access nested items, use double brackets like `print(myDict["Pikachu"]["type"])`

Here is a quick way to print each key and value of the nested dictionary
```python
for x, obj in myDict.items():
	print(x)
	for y in obj:
		print(y + ":", obj[y])

# Pikachu
# type: electric
# hp: 55
# Squirtle
# type: water
# hp: 55
# Bulbasaur
# type: grass
# hp: 55
```








