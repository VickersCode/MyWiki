# Dictionaries

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/)
[https://docs.python.org/3/](https://docs.python.org/3/)
___
## Intro

Dictionaries are ordered and changeable. They are made of key:value pairs. No duplicate keys. 

```python
myDict = {
	"name": "Pikachu"
	"type": "Electric"
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
	"name": "Pikachu"
	"type": "Electric"
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

### Changing Values (Add Values)

There are two ways to change values. For both, if the key does not exist, a new key:value pair will be added.
The first is to use bracket notation
```python
myDict = {
	"name": "Pikachu"
	"type": "Electric"
	"hp": 55
}

myDict["hp"] = 40
```
The second is to use the `update()` method.
```python
myDict = {
	"name": "Pikachu"
	"type": "Electric"
	"hp": 55
}

myDict.update({"hp": 40})
```

## Removing Items
Use `.pop()` to remove key:value pair by key name.
```python
myDict = {
	"name": "Pikachu"
	"type": "Electric"
	"hp": 55
}

myDict.pop("type")
# {"name": "Pikachu", "hp": 55}
```
`.popitem()` will remove the most recently inserted item. No parameter needed.

`del` keyword used with the dict and key is another way to remove specific items. Careful, if we don't specify a key, the whole dict will be deleted.
```python
myDict = {
	"name": "Pikachu"
	"type": "Electric"
	"hp": 55
}

del myDict["type"]
```
`.clear()` will empty everything in the dictionary. 






