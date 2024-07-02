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
for multiline