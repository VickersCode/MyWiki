# Advanced Operators

[Table of Contents](../../README.md) | [Markdown Cheatsheet](../../Markdown%20Cheatsheet.md)

credit: 
[https://www.w3schools.com/python/](https://www.w3schools.com/python/python_operators.asp)
[https://docs.python.org/3/](https://docs.python.org/3/library/operator.html)
___
#### Quick Links (on this page)
- [Arithmetic Operators](#Arithmetic-Operators)
- [Order of Operations](#Order-of-Operations)
- [Assignment Operators](#Assignment-Operators)
- [Comparison Operators](#Comparison-Operators)
- [Logical Operators](#Logical-Operators)
- [Identity Operators](#Identity-Operators)
- [Membership Operators](#Membership-Operators)
- [Bitwise Operators](#Bitwise-Operators)
___
## Arithmetic Operators
Used to perform mathematical computations

| Operator | What it do     | Example |
| -------- | -------------- | ------- |
| +        | Addition       | x + y   |
| -        | Subtraction    | x - y   |
| *        | Multiplication | x * y   |
| /        | Division       | x / y   |
| %        | Modulus        | x % y   |
| **       | Exponentiation | x ** y  |
| //       | Floor division | x // y  |
___
## Order of Operations
Maths will be evaluated in this order. If two operators have the same precedence, it will be evaluated from left to right.

| Operator                                                         | Description                                           |
| ---------------------------------------------------------------- | ----------------------------------------------------- |
| `()`                                                             | Parentheses                                           |
| `**`                                                             | Exponentiation                                        |
| `+x`  `-x`  `~x`                                                 | Unary plus, unary minus, and bitwise NOT              |
| `*`  `/`  `//`  `%`                                              | Multiplication, division, floor division, and modulus |
| `+`  `-`                                                         | Addition and subtraction                              |
| `<<`  `>>`                                                       | Bitwise left and right shifts                         |
| `&`                                                              | Bitwise AND                                           |
| `^`                                                              | Bitwise XOR                                           |
| `\|`                                                             | Bitwise OR                                            |
| `==`  `!=`  `>`  `>=`  `<`  `<=`  `is`  `is not`  `in`  `not in` | Comparisons, identity, and membership operators       |
| `not`                                                            | Logical NOT                                           |
| `and`                                                            | AND                                                   |
| `or`                                                             | OR                                                    |
___
## Assignment Operators
Used to assign values to variables

| Operator | Example | Same As    |
| -------- | ------- | ---------- |
| =        | x = 5   | x = 5      |
| +=       | x += 3  | x = x + 3  |
| -=       | x -= 3  | x = x - 3  |
| *=       | x *= 3  | x = x * 3  |
| /=       | x /= 3  | x = x / 3  |
| %=       | x %= 3  | x = x % 3  |
| //=      | x //= 3 | x = x // 3 |
| **=      | x **= 3 | x = x ** 3 |
| &=       | x &= 3  | x = x & 3  |
| \|=      | x \|= 3 | x = x \| 3 |
| ^=       | x ^= 3  | x = x ^ 3  |
| >>=      | x >>= 3 | x = x >> 3 |
| <<=      | x <<= 3 | x = x << 3 |

The `<<` and `>>` operators are bitwise operators and will be described [below](#Bitwise-Operators)

Operators like `x += 3` are a quicker way of writing `x = x + 3`
___
## Comparison Operators

Comparison Operators return boolean.

| Operator | Name                     | Example |
| -------- | ------------------------ | ------- |
| ==       | Equal                    | x == y  |
| !=       | Not equal                | x != y  |
| >        | Greater than             | x > y   |
| <        | Less than                | x < y   |
| >=       | Greater than or equal to | x >= y  |
| <=       | Less than or equal to    | x <= y  |
___
## Logical Operators

| Operator | Description                                             | Example               |
| -------- | ------------------------------------------------------- | --------------------- |
| and      | Returns True if both statements are true                | x < 5 and  x < 10     |
| or       | Returns True if one of the statements is true           | x < 5 or x < 4        |
| not      | Reverse the result, returns False if the result is true | not(x < 5 and x < 10) |
___
## Identity Operators
These guys don't check if objects are equal, but if they have the same memory location, like a list.

| Operator | Description                                            | Example    |
| -------- | ------------------------------------------------------ | ---------- |
| is       | Returns True if both variables are the same object     | x is y     |
| is not   | Returns True if both variables are not the same object | x is not y |
___
## Membership Operators
Checks to see if something is in an object

| Operator | Description                                                                      | Example |
| -------- | -------------------------------------------------------------------------------- | ------- |
| in       | Returns True if a sequence with the specified value is present in the object     | x in y  |
| not in   | Returns True if a sequence with the specified value is not present in the object | x       |
___
## Bitwise-Operators
Used to do operations on numbers at the bit-level. Go to the [Python Docs](https://wiki.python.org/moin/BitwiseOperators) for more information.

| Operator | Name                 | Description                                                                                             | Example |
| -------- | -------------------- | ------------------------------------------------------------------------------------------------------- | ------- |
| &        | AND                  | Sets each bit to 1 if both bits are 1                                                                   | x & y   |
| \|       | OR                   | Sets each bit to 1 if one of two bits is 1                                                              | x \| y  |
| ^        | XOR                  | Sets each bit to 1 if only one of two bits is 1                                                         | x ^ y   |
| ~        | NOT                  | Inverts all the bits                                                                                    | ~x      |
| <<       | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off                        | x << 2  |
| >>       | Signed right shift   | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | x >> 2  |
