# Python Loops and Conditions Documentation

## Table of Contents
- [Python Loops and Conditions Documentation](#python-loops-and-conditions-documentation)
  - [Table of Contents](#table-of-contents)
  - [Conditions](#conditions)
    - [if Condition](#if-condition)
      - [Basic Syntax](#basic-syntax)
      - [Example](#example)
    - [else Statement](#else-statement)
      - [Basic Syntax](#basic-syntax-1)
      - [Example](#example-1)
    - [elif Statement](#elif-statement)
      - [Basic Syntax](#basic-syntax-2)
      - [Example](#example-2)
    - [Nested if Statements](#nested-if-statements)
      - [Example](#example-3)
    - [Logical Operators](#logical-operators)
      - [Example](#example-4)
  - [Loops](#loops)
    - [For Loop](#for-loop)
      - [Basic Syntax](#basic-syntax-3)
      - [Example](#example-5)
    - [Break and Continue](#break-and-continue)
      - [Example](#example-6)
    - [Nested Loops](#nested-loops)
      - [Example](#example-7)
    - [While Loop](#while-loop)
      - [Basic Syntax](#basic-syntax-4)
      - [Example](#example-8)
    - [Infinite Loops](#infinite-loops)
      - [Example](#example-9)
  - [General Examples](#general-examples)

---

## Conditions

### if Condition
**Identification**  
The `if` statement is used for conditional execution of code. It allows the program to execute certain blocks of code based on whether a condition is true or false.

#### Basic Syntax
```python
if condition:  
    # code to execute if condition is true
```

#### Example
```python
age = 18
if age >= 18:
    print("You are eligible to vote.")
```

### else Statement
The `else` statement is used in conjunction with `if` to execute code when the condition is false.

#### Basic Syntax
```python
if condition:
    # code to execute if condition is true
else:
    # code to execute if condition is false
```

#### Example
```python
age = 16
if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote yet.")
```

### elif Statement
The `elif` statement allows you to check multiple conditions in sequence.

#### Basic Syntax
```python
if condition1:
    # code to execute if condition1 is true
elif condition2:
    # code to execute if condition2 is true
else:
    # code to execute if all conditions are false
```

#### Example
```python
score = 75
if score >= 90:
    print("A")
elif score >= 80:
    print("B")
elif score >= 70:
    print("C")
else:
    print("D")
```

### Nested if Statements
You can use if statements inside other if statements to create nested conditions.

#### Example
```python
x = 10
y = 5
if x > 0:
    if y > 0:
        print("Both x and y are positive")
    else:
        print("x is positive, but y is not")
else:
    print("x is not positive")
```

### Logical Operators
Python uses `and`, `or`, and `not` as logical operators to combine conditions.

#### Example
```python
age = 25
income = 50000
if age > 18 and income > 30000:
    print("Eligible for premium credit card")
```

## Loops

### For Loop
The `for` loop is used to iterate over a sequence (like a list, tuple, or string) or other iterable objects.

#### Basic Syntax
```python
for item in sequence:
    # code to execute for each item
```

#### Example
```python
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)
```

### Break and Continue
- `break` is used to exit a loop prematurely
- `continue` is used to skip the rest of the current iteration and move to the next one

#### Example
```python
for i in range(10):
    if i == 3:
        continue
    if i == 7:
        break
    print(i)
```

### Nested Loops
You can use loops inside other loops to create nested loops.

#### Example
```python
for i in range(3):
    for j in range(3):
        print(f"({i}, {j})")
```

### While Loop
The `while` loop repeats a block of code as long as a condition is true.

#### Basic Syntax
```python
while condition:
    # code to execute while condition is true
```

#### Example
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Infinite Loops
Loops that run indefinitely unless interrupted. Be cautious when using these.

#### Example
```python
while True:
    user_input = input("Enter 'quit' to exit: ")
    if user_input.lower() == 'quit':
        break
```

## General Examples

1. Combining loops and conditions:
```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
sum_even = 0
for num in numbers:
    if num % 2 == 0:
        sum_even += num
print(f"Sum of even numbers: {sum_even}")
```

2. Using a while loop with conditions:
```python
import random

target = random.randint(1, 100)
guess = 0
attempts = 0

while guess != target:
    guess = int(input("Guess the number (1-100): "))
    attempts += 1
    if guess < target:
        print("Too low!")
    elif guess > target:
        print("Too high!")

print(f"Correct! You guessed it in {attempts} attempts.")
```
