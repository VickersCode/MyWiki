# Working with Strings

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)
___
### Slicing
```python
string_to_slice = "I want this slice string sliced"
sliced_string = string_to_slice[12:17] # becomes "slice"
```

Using the bracket notation, we "get" the characters we are asking for.
If we leave the first field blank, we are asking for all characters up to the position of the second field.
```python
wrong_string = "new world new"
correct_string = wrong_string[:10] # becomes "new world"
```

And then using the second field blank allows us to grab the rest of the characters from the point in the first field.
```python
wrong_string = "new world new"
correct_string = wrong_string[4:] # becomes "world new"
```

### Modifying Strings

To make all characters upper or lowercase
```python
s = "string"
upper = s.upper() # becomes "STRING"
lower = upper.lower() # becomes "string"
```

To remove all whitespace from beginning or end
```python
s = "  some string  "
d = s.strip() # "some string"
```
