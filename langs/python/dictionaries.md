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

