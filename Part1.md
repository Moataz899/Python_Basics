# Topics Part 1

- [Topics Part 1](#topics-part-1)
  - [What is a Variable ?](#what-is-a-variable-)
  - [Variable Assignment](#variable-assignment)
  - [Variable Types](#variable-types)
  - [Variable Names](#variable-names)
  - [Multi Words Variable Names](#multi-words-variable-names)
  - [Python Data Types](#python-data-types)
    - [Examples:](#examples)
  - [Setting the Specific Data Type](#setting-the-specific-data-type)
  - [Basic Operation](#basic-operation)
  - [Python Arithmetic Operators](#python-arithmetic-operators)
  - [Python Arithmetic Operators Examples](#python-arithmetic-operators-examples)
  - [Python Assignment Operators](#python-assignment-operators)
  - [Python Comparison Operators](#python-comparison-operators)
  - [Python Logical Operators](#python-logical-operators)
  - [Python Identity Operators](#python-identity-operators)
  - [Python Identity Operators](#python-identity-operators-1)
  - [Python Membership Operators](#python-membership-operators)
  - [Python Bitwise Operators](#python-bitwise-operators)
  - [Python Casting](#python-casting)
    - [Examples:](#examples-1)


## What is a Variable ?
*A variable in Python is a name that is used to refer to a memory location. Variables are used to store data and can be updated to hold different values.*

## Variable Assignment

*In Python, you assign a value to a variable using the equals sign (`=`). For example:*

```python
x = 5  
```
## Variable Types
*In Python, there are three main types of variables: integers, floats, and strings. Integers
are whole numbers, floats are decimal numbers, and strings are sequences of characters, booleans represent True or False values.*
```python
x = 5 # Integer

y = "Hello, World!" # String

f = 5.5 # float

p = True #bool
```
## Variable Names

 *Avariable can have a short name (like x and y) or a more descriptive name (age, carname, total_volume). Rules for Python variables :*

* A variable name must start with a letter or the underscore character
* A variable name cannot start with a number
* A variable name can only contain alpha-numeric characters and underscores (A-z, 0-9, and _ )
* Variable names are case-sensitive (age, Age and AGE are three different variables)
* A variable name cannot be any of the Python keywords.
Examples :


```python
myvar = "John"
my_var = "John"
_my_var = "John"
myVar = "John"
MYVAR = "John"
myvar2 = "John"
```

## Multi Words Variable Names

* Variable names with more than one word can be difficult to read.
* There are several techniques you can use to make them more readable:
* *`Camel Case`* : Each word, except the first, starts with a capital letter:
```python
myVariableName = "John"
```
* *`Pascal Case`* : Each word starts with a capital letter:
```
MyVariableName = "John"
```
* *`Snake Case`* : Each word is separated by an underscore character:
```
my_variable_name = "John"
```
## Python Data Types

*In programming, data type is an important concept,
Variables can store data of different types, and different types can do different things.
Python has the following data types built-in by default, in these categories:*
```
Text Type:	str 

Numeric Types:	int, float, complex

Sequence Types:	list, tuple, range

Mapping Type:	dict

Set Types:	set, frozenset

Boolean Type:	bool

Binary Types: bytes, bytearray, memoryview

None Type:	NoneType
```
### Examples:

| Example                                | Data Type   |
|----------------------------------------|-------------|
| `x = "Hello World"                     ` | str         |
| `x = 20                                ` | int         |
| `x = 20.5                              ` | float       |
| `x = 1j                                ` | complex     |
| `x = ["apple", "banana", "cherry"]     ` | list        |
| `x = ("apple", "banana", "cherry")     ` | tuple       |
| `x = range(6)                          ` | range       |
| `x = {"name" : "John", "age" : 36}     ` | dict        |
| `x = {"apple", "banana", "cherry"}     ` | set         |
| `x = frozenset({"apple", "banana", "cherry"})` | frozenset |
| `x = True                  `             | bool        |
| `x = b"Hello"             `              | bytes       |
| `x = bytearray(5)  `                     | bytearray   |
| `x = memoryview(bytes(5))`               | memoryview  |
| `x = None `                              | NoneType    |


## Setting the Specific Data Type

*If you want to specify the data type, you can use the following constructor functions:*

| Example                                       | Data Type   |
|-----------------------------------------------|-------------|
| `x = str("Hello World")                       ` | str         |
| `x = int(20)                                 `  | int         |
| `x = float(20.5)                             `  | float       |
| `x = complex(1j)                             `  | complex     |
| `x = list(("apple", "banana", "cherry"))     `  | list        |
| `x = tuple(("apple", "banana", "cherry"))    `  | tuple       |
| `x = range(6)                                `  | range       |
| `x = dict(name="John", age=36)               `  | dict        |
| `x = set(("apple", "banana", "cherry"))     `   | set         |
| `x = frozenset(("apple", "banana", "cherry"))`  | frozenset   |
| `x = bool(5)             `                      | bool        |
| `x = bytes(5)           `                       | bytes       |
| `x = bytearray(5)       `                       | bytearray   |
| `x = memoryview(bytes(5))`                      | memoryview  |


## Basic Operation
*Operators are used to perform operations on variables and values,*
*Python divides the operators into the following groups:*
* Arithmetic operators
* Assignment operators
* Comparison operators
* Logical operators
* Identity operators
* Membership operators
* Bitwise operators

## Python Arithmetic Operators
*Arithmetic operators are used with numeric values to perform common mathematical operations:*
| Operator | Name           | Example  |
|----------|----------------|----------|
| `+`        | Addition       | `x + y `  |
| `- `       | Subtraction    | `x - y  ` |
| `* `       | Multiplication | `x * y `  |
| `/ `       | Division       | `x / y  ` |
| `% `       | Modulus        | `x % y `  |
| `**`       | Exponentiation | `x ** y ` |
| `//`       | Floor division | `x // y ` |

## Python Arithmetic Operators Examples
```python
# Addition
x = 5
y = 3
result = x + y
print("Addition: ", result)

# Subtraction
result = x - y
print("Subtraction: ", result)

# Multiplication
result = x * y
print("Multiplication: ", result)

# Division
result = x / y
print("Division: ", result)

# Modulus
result = x % y
print("Modulus: ", result)

# Exponentiation
result = x ** y
print("Exponentiation: ", result)

# Floor division
result = x // y
print("Floor division: ", result)
```
## Python Assignment Operators
*Assignment operators are used to assign values to variables:*

| Operator | Example        | Same As       |
|----------|----------------|---------------|
| `=`        | x = 5          |` x = 5`       |
| `+=`       | x += 3         | `x = x + 3 `   |
| `-=`       | x -= 3         | `x = x - 3  ` |
| `*=`       | x *= 3         | `x = x * 3  ` |
| `/=`       | x /= 3         | `x = x / 3 `  |
| `%=`       | x %= 3         | `x = x % 3  ` |
| `//=`      | x //= 3        | `x = x // 3 ` |
| `**=`      | x **= 3        | `x = x ** 3  `|
| `&=`       | x &= 3         | `x = x & 3  ` |
| `^=`       | x ^= 3         | `x = x ^ 3 `  |
| `>>=`      | x >>= 3        | `x = x >> 3 ` |
| `<<=`      | x <<= 3        | `x = x << 3`  |


## Python Comparison Operators
*Comparison operators are used to compare two values:*

| Operator | Name                        | Example  |
|----------|-----------------------------|----------|
| `==`       | Equal                       | `x == y `  |
| `!=`       | Not equal                   | `x != y`   |
| `>`        | Greater than                | `x > y`    |
| `<`       | Less than                   | `x < y`    |
| `>=`      | Greater than or equal to    | `x >= y `  |
| `<=`       | Less than or equal to       | `x <= y`   |


## Python Logical Operators
*Logical operators are used to combine conditional statements:*

| Operator | Description                                    | Example                              |
|----------|------------------------------------------------|--------------------------------------|
| `and `     | Returns True if both statements are true       | `x < 5 and x < 10`                   |
| `or`       | Returns True if one of the statements is true  | `x < 5 or x < 4`                    |
| `not`      | Reverses the result, returns False if the result is true | `not(x < 5 and x < 10)`  |


## Python Identity Operators
*Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:*

## Python Identity Operators
| Operator | Description                                | Example       |
|----------|--------------------------------------------|---------------|
| `is`       | Returns True if both variables are the same object | `x is y`      |
| `is not`   | Returns True if both variables are not the same object | `x is not y`  |


## Python Membership Operators
*Membership operators are used to test if a sequence is presented in an object:*

| Operator | Description                                          | Example     |
|----------|------------------------------------------------------|-------------|
| `in`      | Returns True if a sequence with the specified value is present in the object | `x in y`    |
| `not in`   | Returns True if a sequence with the specified value is not present in the object | `x not in y`|


## Python Bitwise Operators
*Bitwise operators are used to compare (binary) numbers:*


| Operator | Name | Description                                                                                   | Example     |
|----------|------|-----------------------------------------------------------------------------------------------|-------------|
| `&`  | AND  | Sets each bit to 1 if both bits are 1                                                         | `x & y`     |
| `\|`  | OR   | Sets each bit to 1 if one of two bits is 1|`x \|  y`     |
| `^  `      | XOR  | Sets each bit to 1 if only one of two bits is 1                                               | `x ^ y`     |
| `~ `       | NOT  | Inverts all the bits                                                                          | `~x`        |
| `<<  `     | Zero fill left shift | Shift left by pushing zeros in from the right and let the leftmost bits fall off | `x << 2`    |
| `>>`       | Signed right shift | Shift right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off | `x >> 2`    

## Python Casting

*There may be times when you want to specify a type on a variable. This can be done with casting. Python is an object-oriented language, and as such, it uses classes to define data types, including its primitive types.*

*Casting in Python is done using constructor functions:*

- **`int()`**: Constructs an integer number from an integer literal, a float literal (by removing all decimals), or a string literal (providing the string represents a whole number).
- **`float()`**: Constructs a float number from an integer literal, a float literal, or a string literal (providing the string represents a float or an integer).
- **`str()`**: Constructs a string from a wide variety of data types, including strings, integer literals, and float literals.

### Examples:

```python
# Casting to integer
x = int(3.14)    # x will be 3
y = int("42")    # y will be 42

# Casting to float
a = float(7)     # a will be 7.0
b = float("3.14")# b will be 3.14

# Casting to string
m = str(10)      # m will be '10'
n = str(3.14)    # n will be '3.14'
```