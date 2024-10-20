# Python Functions, Exception Handling, and File Manipulation Documentation

## Table of Contents
- [Python Functions, Exception Handling, and File Manipulation Documentation](#python-functions-exception-handling-and-file-manipulation-documentation)
  - [Table of Contents](#table-of-contents)
  - [Functions](#functions)
    - [Defining Functions](#defining-functions)
      - [Basic Syntax](#basic-syntax)
    - [Function Parameters](#function-parameters)
      - [Default Parameters](#default-parameters)
    - [Return Values](#return-values)
    - [Lambda Functions](#lambda-functions)
  - [Exception Handling](#exception-handling)
    - [Try-Except Blocks](#try-except-blocks)
    - [Raising Exceptions](#raising-exceptions)
    - [Finally Clause](#finally-clause)
  - [File Manipulation](#file-manipulation)
    - [Opening and Closing Files](#opening-and-closing-files)
    - [Reading from Files](#reading-from-files)
    - [Writing to Files](#writing-to-files)
    - [Working with CSV Files](#working-with-csv-files)

---

## Functions

### Defining Functions
A function is a reusable block of code that performs a specific task. It can take inputs, called parameters, and return an output.

#### Basic Syntax
```python
def my_function():
    print("Hello, World!")

```

### Function Parameters
Functions can accept parameters, which are values passed to the function when it's called.

````python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Output: Hello, Alice!
````

#### Default Parameters
You can set default values for parameters:

````python
def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")

greet("Bob")  # Output: Hello, Bob!
greet("Charlie", "Hi")  # Output: Hi, Charlie!
````

### Return Values
Functions can return values using the `return` statement:

````python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
````

### Lambda Functions
Lambda functions are small, anonymous functions defined using the `lambda` keyword:

````python
square = lambda x: x ** 2
print(square(4))  # Output: 16
````

## Exception Handling

### Try-Except Blocks
Try-except blocks are used to handle exceptions (errors) that may occur during program execution:

````python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Error: Division by zero!")
````

### Raising Exceptions
You can raise exceptions using the `raise` keyword:

````python
def validate_age(age):
    if age < 0:
        raise ValueError("Age cannot be negative")
    return age

try:
    validate_age(-5)
except ValueError as e:
    print(e)  # Output: Age cannot be negative
````

### Finally Clause
The `finally` clause is executed regardless of whether an exception occurred:

````python
try:
    file = open("example.txt", "r")
    # File operations
except FileNotFoundError:
    print("File not found")
finally:
    file.close()  # This will always be executed
````

## File Manipulation

### Opening and Closing Files
Use the `open()` function to open files and always close them when done:

````python
# Using a context manager (recommended)
with open("example.txt", "r") as file:
    # File operations
    pass  # File is automatically closed after this block

# Manual opening and closing
file = open("example.txt", "r")
# File operations
file.close()
````

### Reading from Files
There are several methods to read from files:

````python
with open("example.txt", "r") as file:
    # Read entire file
    content = file.read()
    
    # Read line by line
    for line in file:
        print(line.strip())
    
    # Read all lines into a list
    lines = file.readlines()
````

### Writing to Files
You can write to files using the write modes:

````python
with open("example.txt", "w") as file:
    file.write("Hello, World!\n")
    file.writelines(["Line 1\n", "Line 2\n", "Line 3\n"])
````

### Working with CSV Files
Python's `csv` module provides functionality for reading and writing CSV files:

````python
import csv

# Reading CSV
with open("data.csv", "r") as file:
    csv_reader = csv.reader(file)
    for row in csv_reader:
        print(row)

# Writing CSV
data = [["Name", "Age"], ["Alice", 30], ["Bob", 25]]
with open("output.csv", "w", newline="") as file:
    csv_writer = csv.writer(file)
    csv_writer.writerows(data)
````

This completes the documentation for Python Functions, Exception Handling, and File Manipulation. Each section includes explanations and examples to help understand these important concepts in Python programming.
