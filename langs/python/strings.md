# Working with Strings

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/)
[https://docs.python.org/3/](https://docs.python.org/3/)
___

A good reference for string methods can be found [here](https://www.w3schools.com/python/python_ref_string.asp)
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

We can replace a string with another
```python
a = "Hello, World!"
print(a.replace("H", "J")) # "Jello World"
```

Or split the words into a list
```python
a = "let's split this into a list"
d = a.split(" ") 

# ["let's", 'split', 'this', 'into', 'a', 'list']
```

##### Concatenation
We can "combine" strings using the '+' operator.
```python
a = "Hello"  
b = "World"  
c = a + b  
print(c)
```

#### Format Strings
A table of formatting types for the `.format()` method can be found [here](https://www.w3schools.com/python/ref_string_format.asp#:~:text=The%20format()%20method%20formats,method%20returns%20the%20formatted%20string.)

Strings cannot be combined with int() data types, so we use the `format()` method

```python
candles = 28
txt = "I have {} candles on my birthday cake."
print(txt.format(candles))  # prints "I have 28 candles on my birthday cake."
```

The `format()` method can take unlimited arguments

```python
quantity = 3  
itemno = 567  
price = 49.95  
myorder = "I want to pay {2} dollars for {0} pieces of item {1}."  
print(myorder.format(quantity, itemno, price))

# prints "I want to pay 49.95 dollars for 3 pieces of item 567."
```

These are some of the formatting types found [here](https://www.w3schools.com/python/ref_string_format.asp#:~:text=The%20format()%20method%20formats,method%20returns%20the%20formatted%20string.)

| Type | Description |
| ---- | ---- |
| :b | Binary Format |
| :d | Decimal Format |
| :% | Percentage Format |
And this is how we use these few examples

```python
#Use "b" to convert the number into binary format:

txt = "The binary version of {0} is {0:b}"

print(txt.format(5)) 
# prints "The binary version of 5 is 101"

```

```python
#Use "d" to convert a number, in this case a binary number, into decimal number format:

txt = "We have {:d} chickens."
print(txt.format(0b101)) 
# prints "We have 5 chickens."

```

```python
#Use "%" to convert the number into a percentage format:

txt = "You scored {:%}"
print(txt.format(0.75)) # prints "You scored 75.000000%"

#Or, without any decimals:

txt = "You scored {:.0%}"
print(txt.format(0.75)) # prints "You scored 75%"

```

We can tell the program how many decimal places to display

```python
piNum = 3.1415
print("Pi is %f" %piNum) # prints "Pi is 3.141500"

print("Pi is %.3f" %piNum) # prints "Pi is 3.142"
```

### String Methods Table
|Method|Description|
|---|---|
|capitalize() |Converts the first character to upper case|
|casefold() |Converts string into lower case|
|center() |Returns a centered string|
|count() |Returns the number of times a specified value occurs in a string|
|encode() |Returns an encoded version of the string|
|endswith() |Returns true if the string ends with the specified value|
|expandtabs() |Sets the tab size of the string|
|find() |Searches the string for a specified value and returns the position of where it was found|
|format() |Formats specified values in a string|
|format_map()|Formats specified values in a string|
|index() |Searches the string for a specified value and returns the position of where it was found|
|isalnum() |Returns True if all characters in the string are alphanumeric|
|isalpha() |Returns True if all characters in the string are in the alphabet|
|isascii() |Returns True if all characters in the string are ascii characters|
|isdecimal() |Returns True if all characters in the string are decimals|
|isdigit() |Returns True if all characters in the string are digits|
|isidentifier() |Returns True if the string is an identifier|
|islower() |Returns True if all characters in the string are lower case|
|isnumeric() |Returns True if all characters in the string are numeric|
|isprintable() |Returns True if all characters in the string are printable|
|isspace() |Returns True if all characters in the string are whitespaces|
|istitle() |Returns True if the string follows the rules of a title|
|isupper() |Returns True if all characters in the string are upper case|
|join() |Joins the elements of an iterable to the end of the string|
|ljust() |Returns a left justified version of the string|
|lower() |Converts a string into lower case|
|lstrip() |Returns a left trim version of the string|
|maketrans() |Returns a translation table to be used in translations|
|partition() |Returns a tuple where the string is parted into three parts|
|replace() |Returns a string where a specified value is replaced with a specified value|
|rfind() |Searches the string for a specified value and returns the last position of where it was found|
|rindex() |Searches the string for a specified value and returns the last position of where it was found|
|rjust() |Returns a right justified version of the string|
|rpartition() |Returns a tuple where the string is parted into three parts|
|rsplit() |Splits the string at the specified separator, and returns a list|
|rstrip() |Returns a right trim version of the string|
|split() |Splits the string at the specified separator, and returns a list|
|splitlines() |Splits the string at line breaks and returns a list|
|startswith() |Returns true if the string starts with the specified value|
|strip() |Returns a trimmed version of the string|
|swapcase() |Swaps cases, lower case becomes upper case and vice versa|
|title() |Converts the first character of each word to upper case|
|translate() |Returns a translated string|
|upper() |Converts a string into upper case|
|zfill() |Fills the string with a specified number of 0 values at the beginning|
