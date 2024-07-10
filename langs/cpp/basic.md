# Basic cpp

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
https://www.w3schools.com/cpp/cpp_getstarted.asp
https://devdocs.io/cpp/
___
#### Boilerplate

Here's a great boilerplate
```cpp
#include <iostream>  
using namespace std;  
  
int main() {  
  cout << "Hello World!";  
  return 0;  
}
```

- `#include <iostream>` is necessary to allow input/output. The `#` is a preprocessor directive, `include` means files are accessible, and `<iostream>` is the ilbrary.
- `using namespace std;` makes it so we don't have to type `std::` every time. Otherwise, the main() function would look like 
```cpp
int main() {  
  std::cout << "Hello World!";  
  return 0;  
}
```
____
#### Printing to the screen

`cout` is the operator which is used to print objects to the screen. Here's the classic Hello World
```cpp
#include <iostream>
using namespace std;

int main() {
cout << "Hello World";
return 0;
}
```
In C++, we have to put in our line breaks. We can use either `\n` or `endl`
```cpp
#include <iostream>  
using namespace std;  
  
int main() {  
  cout << "Hello World!" << "\n\n";  
  cout << "I am learning C++";  
  return 0;  
}

// OR

#include <iostream>  
using namespace std;  
  
int main() {  
  cout << "Hello World!" << endl;  
  cout << "I am learning C++";  
  return 0;  
}
```
___
#### Comments
Use `//` for single line 
and `/* */` for multi-line
```cpp
// comments

/*
comments
*/
```
___

#### Variables

In C++, variable types need to be declared. 
Here are a few common types. 

| **Variable Type** | **Description**                                                                              |
| ----------------- | -------------------------------------------------------------------------------------------- |
| int               | Used to store any whole number.                                                              |
| float             | Used for storing numbers with decimal point values. It can store up to seven decimal places. |
| double            | Used for storing numbers with decimal point values. It can store up to 15 decimal places.    |
| bool              | Used to store either true or false values.                                                   |
| char              | Used to store a single character, letter, number or ASCII value.                             |
| string            | Used to store a series of characters.                                                        |

And here are a few declaration examples
```cpp
int nums = 15
string name = "coder"
double dollars = 6.99
```

##### Declaring multiple variables

A couple quick examples
```cpp
int x = 5, y = 6, z = 50;

// OR

int x, y, z;
x = y = z = 50;

```

##### Constants
Constants are immutable, read-only. Just put const in front of the declaration, like so: `const int myNum = 43;`

They must be declared with a value, we cannot say `const int daysPerWeek;` and then declare the variable. That would be a mutation.

___

#### User Input

As '`cout <<`' prints to the screen, '`cin >>`' takes input from a keyboard. We declare the variable first, then we ask for input.
```cpp
int userInput;
cout << "Give a number: ";
cin >> userInput;
```

`cin` and `cout` are both part of the `<iostream>` library. For a complete library reference, go [here](https://cplusplus.com/reference/iostream/)

___
### Data Types

Here's a table from w3schools, showing size and description of the most common data types.

| Data Type | Size         | Description                                                                                           |
| --------- | ------------ | ----------------------------------------------------------------------------------------------------- |
| `boolean` | 1 byte       | Stores true or false values                                                                           |
| `char`    | 1 byte       | Stores a single character/letter/number, or ASCII values                                              |
| `int`     | 2 or 4 bytes | Stores whole numbers, without decimals                                                                |
| `float`   | 4 bytes      | Stores fractional numbers, containing one or more decimals. Sufficient for storing 6-7 decimal digits |
| `double`  | 8 bytes      | Stores fractional numbers, containing one or more decimals. Sufficient for storing 15 decimal digits  |

At the [bottom of this page](#DataTable) there is a more in depth table of types with different modifiers.

When deciding whether to use float or double, most people use double because it has a precision of 15 digits, versus the 6-7 digits that float stores.

**C++ allows for scientific notation.** We can use little or big 'E'
```cpp
float sci = 23E4
double sci2 = 23e4
```

##### Booleans

`true` = 1
`false` = 0

```cpp
bool isTrue = true;
bool isFalse = false;
cout << isTrue; // outputs 1
cout << isFalse; // outputs 0
```


##### Character types

The `char` data type only stores a single character. Hence, it's size is only one byte.

ASCII works here
```cpp
char a = 65,
	 b = 66,
	 c = 67;

cout << a << endl; << b << endl; << c << endl;

// A
// B
// C
```

[Here is an ASCII Reference](https://www.w3schools.com/charsets/ref_html_ascii.asp)

___
#### String Types

The header file `<string>` is required. 
Strings must be surrounded by double quotes.

```cpp
string greeting = "Hello";  
cout << greeting;
```
___
#### DataTable

| Type specifier         | Equivalent type                     | Width in bits by data model |        |        |        |        |
| ---------------------- | ----------------------------------- | :-------------------------: | :----: | :----: | :----: | :----: |
| C++ standard           | LP32                                |            ILP32            | LLP64  |  LP64  |        |        |
| signed char            | signed char                         |     at least  <br>**8**     | **8**  | **8**  | **8**  | **8**  |
| unsigned char          | unsigned char                       |                             |        |        |        |        |
| short                  | short int                           |    at least  <br>**16**     | **16** | **16** | **16** | **16** |
| short int              |                                     |                             |        |        |        |        |
| signed short           |                                     |                             |        |        |        |        |
| signed short int       |                                     |                             |        |        |        |        |
| unsigned short         | unsigned short int                  |                             |        |        |        |        |
| unsigned short int     |                                     |                             |        |        |        |        |
| int                    | int                                 |    at least  <br>**16**     | **16** | **32** | **32** | **32** |
| signed                 |                                     |                             |        |        |        |        |
| signed int             |                                     |                             |        |        |        |        |
| unsigned               | unsigned int                        |                             |        |        |        |        |
| unsigned int           |                                     |                             |        |        |        |        |
| long                   | long int                            |    at least  <br>**32**     | **32** | **32** | **32** | **64** |
| long int               |                                     |                             |        |        |        |        |
| signed long            |                                     |                             |        |        |        |        |
| signed long int        |                                     |                             |        |        |        |        |
| unsigned long          | unsigned long int                   |                             |        |        |        |        |
| unsigned long int      |                                     |                             |        |        |        |        |
| long long              | long long int  <br>(C++11)          |    at least  <br>**64**     | **64** | **64** | **64** | **64** |
| long long int          |                                     |                             |        |        |        |        |
| signed long long       |                                     |                             |        |        |        |        |
| signed long long int   |                                     |                             |        |        |        |        |
| unsigned long long     | unsigned long long int  <br>(C++11) |                             |        |        |        |        |
| unsigned long long int |                                     |                             |        |        |        |        |