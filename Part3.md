# Python Data Structures Documentation

## Table of Contents
- [Python Data Structures Documentation](#python-data-structures-documentation)
  - [Table of Contents](#table-of-contents)
  - [Lists](#lists)
    - [Creating Lists](#creating-lists)
      - [Basic Syntax](#basic-syntax)
    - [Accessing Elements](#accessing-elements)
    - [Modifying Lists](#modifying-lists)
    - [List Methods](#list-methods)
  - [Tuples](#tuples)
    - [Creating Tuples](#creating-tuples)
    - [Accessing Elements](#accessing-elements-1)
    - [Tuple Methods](#tuple-methods)
  - [Sets](#sets)
    - [Creating Sets](#creating-sets)
    - [Set Operations](#set-operations)
    - [Set Methods](#set-methods)
  - [Dictionaries](#dictionaries)
    - [Creating Dictionaries](#creating-dictionaries)
    - [Accessing and Modifying Elements](#accessing-and-modifying-elements)
    - [Dictionary Methods](#dictionary-methods)
  - [Specialized Containers from Collections](#specialized-containers-from-collections)
    - [Counter](#counter)
    - [defaultdict](#defaultdict)
    - [OrderedDict](#ordereddict)
    - [namedtuple](#namedtuple)

---

## Lists

### Creating Lists
A list is a mutable, ordered collection of items. Lists can contain different data types.

#### Basic Syntax
```python
my_list = [1, 2, 3, "apple", "banana"]

```

### Accessing Elements
List elements are accessed using index notation. Python uses zero-based indexing.

```python
my_list = [1, 2, 3, "apple", "banana"]
print(my_list[0])  # Output: 1
print(my_list[-1])  # Output: "banana" (negative indexing starts from the end)
```

### Modifying Lists
Lists are mutable, meaning their elements can be changed after creation.

```python
my_list = [1, 2, 3, 4, 5]
my_list[2] = 10
print(my_list)  # Output: [1, 2, 10, 4, 5]
```

### List Methods
Python provides several built-in methods for list manipulation:

```python
my_list = [1, 2, 3]
my_list.append(4)  # Adds an element to the end
my_list.extend([5, 6])  # Adds multiple elements to the end
my_list.insert(0, 0)  # Inserts an element at a specific index
my_list.remove(3)  # Removes the first occurrence of an element
popped = my_list.pop()  # Removes and returns the last element
my_list.sort()  # Sorts the list in-place
```

## Tuples

### Creating Tuples
Tuples are immutable, ordered collections of elements.

```python
my_tuple = (1, 2, 3, "apple", "banana")
single_element_tuple = (1,)  # Note the comma for single-element tuples
```

### Accessing Elements
Tuple elements are accessed similarly to lists, using index notation.

```python
my_tuple = (1, 2, 3, "apple", "banana")
print(my_tuple[0])  # Output: 1
print(my_tuple[-1])  # Output: "banana"
```

### Tuple Methods
Tuples have fewer methods than lists due to their immutability:

```python
my_tuple = (1, 2, 2, 3, 4)
print(my_tuple.count(2))  # Counts occurrences of an element
print(my_tuple.index(3))  # Returns the index of an element
```

## Sets

### Creating Sets
Sets are unordered collections of unique elements.

```python
my_set = {1, 2, 3, 4, 5}
empty_set = set()  # Creating an empty set
```

### Set Operations
Sets support mathematical set operations:

```python
set1 = {1, 2, 3, 4, 5}
set2 = {4, 5, 6, 7, 8}
print(set1.union(set2))  # Union
print(set1.intersection(set2))  # Intersection
print(set1.difference(set2))  # Difference
```

### Set Methods
Some useful set methods include:

```python
my_set = {1, 2, 3}
my_set.add(4)  # Adds an element
my_set.remove(2)  # Removes an element (raises KeyError if not found)
my_set.discard(5)  # Removes an element if present (no error if not found)
popped = my_set.pop()  # Removes and returns an arbitrary element
```

## Dictionaries

### Creating Dictionaries
Dictionaries are key-value pairs, where each key must be unique.

```python
my_dict = {"name": "John", "age": 30, "city": "New York"}
empty_dict = {}  # Creating an empty dictionary
```

### Accessing and Modifying Elements
Dictionary elements are accessed and modified using keys:

```python
my_dict = {"name": "John", "age": 30, "city": "New York"}
print(my_dict["name"])  # Output: "John"
my_dict["age"] = 31  # Modifying a value
my_dict["country"] = "USA"  # Adding a new key-value pair
```

### Dictionary Methods
Some useful dictionary methods include:

```python
my_dict = {"name": "John", "age": 30, "city": "New York"}
print(my_dict.keys())  # Returns a view of all keys
print(my_dict.values())  # Returns a view of all values
print(my_dict.items())  # Returns a view of all key-value pairs
print(my_dict.get("name", "Not found"))  # Returns value or default if key not found
my_dict.update({"age": 31, "job": "Engineer"})  # Updates multiple key-value pairs
```

## Specialized Containers from Collections

### Counter
A dict subclass for counting hashable objects:

```python
from collections import Counter

my_counter = Counter(['a', 'b', 'c', 'a', 'b', 'b'])
print(my_counter)  # Output: Counter({'b': 3, 'a': 2, 'c': 1})
```

### defaultdict
A dict subclass that calls a factory function to supply missing values:

```python
from collections import defaultdict

dd = defaultdict(list)
dd['key'].append(1)  # No KeyError for missing keys
print(dd)  # Output: defaultdict(<class 'list'>, {'key': [1]})
```

### OrderedDict
A dict subclass that remembers the order entries were added:

```python
from collections import OrderedDict

od = OrderedDict()
od['a'] = 1
od['b'] = 2
od['c'] = 3
print(od)  # Output: OrderedDict([('a', 1), ('b', 2), ('c', 3)])
```

### namedtuple
Returns a tuple subclass with named fields:

```python
from collections import namedtuple

Point = namedtuple('Point', ['x', 'y'])
p = Point(11, y=22)
print(p.x, p.y)  # Output: 11 22
```

This completes the documentation for Python Data Structures, covering lists, tuples, sets, dictionaries, and specialized containers from the collections module. Each section includes explanations and examples to help understand these fundamental data structures in Python.
