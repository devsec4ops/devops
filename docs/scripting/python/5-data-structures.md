# Data Structures

## Lists

A list is a collection of items, which can be of different types. Lists are mutable, meaning that you can change the elements of a list after it has been created. Lists are created using square brackets `[]` and elements are separated by commas.

```python
# Syntax
list_name = [item1, item2, ...]
```

```python
# Example
fruits = ["apple", "banana", "cherry"]
```

In the example above, we define a list called `fruits` that contains three string elements.

### Accessing Elements

You can access individual elements of a list using their index. The index of the first element is 0, the index of the second element is 1, and so on. You can also use negative indices to access elements from the end of the list.

```python
# Syntax
element = list_name[index]
```

```python
# Example
fruits = ["apple", "banana", "cherry"]
print(fruits[0])  # Output: apple
print(fruits[-1])  # Output: cherry
```

In the example above, we access the first and last elements of the `fruits` list using their indices.

### Modifying Elements

You can modify the elements of a list by assigning new values to them using their indices.

```python
# Syntax
list_name[index] = new_value
```

```python
# Example
fruits = ["apple", "banana", "cherry"]
fruits[1] = "orange"
print(fruits)  # Output: ['apple', 'orange', 'cherry']
```

In the example above, we change the second element of the `fruits` list from "banana" to "orange".

### Adding and Removing Elements

You can add new elements to a list using the `append` method, and remove elements using the `remove` method.

```python
# Syntax
list_name.append(new_item)
list_name.remove(item)
```

```python
# Example
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
print(fruits)  # Output: ['apple', 'banana', 'cherry', 'orange']
fruits.remove("banana")
print(fruits)  # Output: ['apple', 'cherry', 'orange']
```

In the example above, we add "orange" to the `fruits` list using the `append` method, and remove "banana" from the list using the `remove` method.

## Tuples

A tuple is a collection of items, similar to a list. However, tuples are immutable, meaning that you cannot change the elements of a tuple after it has been created. Tuples are created using parentheses `()` and elements are separated by commas.

```python
# Syntax
tuple_name = (item1, item2, ...)
```

```python
# Example
colors = ("red", "green", "blue")
```

In the example above, we define a tuple called `colors` that contains three string elements.

### Accessing Elements

You can access individual elements of a tuple using their index, similar to lists.

```python
# Syntax
element = tuple_name[index]
```

```python
# Example
colors = ("red", "green", "blue")
print(colors[0])  # Output: red
print(colors[-1])  # Output: blue
```

In the example above, we access the first and last elements of the `colors` tuple using their indices.

### Modifying Elements

Since tuples are immutable, you cannot modify the elements of a tuple after it has been created.

```python
# Example
colors = ("red", "green", "blue")
colors[1] = "yellow"  # TypeError: 'tuple' object does not support item assignment
```

In the example above, attempting to change the second element of the `colors` tuple results in a `TypeError`.

## Dictionaries

A dictionary is a collection of key-value pairs. Each key is associated with a value, and you can use the key to access the corresponding value. Dictionaries are mutable and can contain elements of different types. Dictionaries are created using curly braces `{}` and key-value pairs are separated by commas.

```python
# Syntax
dict_name = {key1: value1, key2: value2, ...}
```

```python
# Example
person = {"name": "Alice", "age": 25, "city": "New York"}
```

In the example above, we define a dictionary called `person` that contains three key-value pairs.

### Accessing Elements

You can access the value associated with a key in a dictionary using the key.

```python
# Syntax
value = dict_name[key]
```

```python
# Example
person = {"name": "Alice", "age": 25, "city": "New York"}
print(person["name"])  # Output: Alice
print(person["age"])  # Output: 25
```

In the example above, we access the values associated with the "name" and "age" keys in the `person` dictionary.

### Modifying Elements

You can modify the value associated with a key in a dictionary by assigning a new value to it.

```python
# Syntax
dict_name[key] = new_value
```

```python
# Example
person = {"name": "Alice", "age": 25, "city": "New York"}
person["age"] = 26
print(person)  # Output: {'name': 'Alice', 'age': 26, 'city': 'New York'}
```

In the example above, we change the value associated with the "age" key in the `person` dictionary from 25 to 26.

### Adding and Removing Elements

You can add new key-value pairs to a dictionary by assigning a value to a new key, and remove key-value pairs using the `pop` method.

```python
# Syntax
dict_name[new_key] = new_value
dict_name.pop(key)
```

```python
# Example
person = {"name": "Alice", "age": 25, "city": "New York"}

# Add a new key-value pair
person["email"] = "alice@example.com"
print(person)  # Output: {'name': 'Alice', 'age': 25, 'city': 'New York', 'email': 'alice@example.com'}

# Remove a key-value pair
person.pop("age")
print(person)  # Output: {'name': 'Alice', 'city': 'New York', 'email': 'alice@example.com'}
```

In the example above, we add an "email" key-value pair to the `person` dictionary, and then remove the "age" key-value pair using the `pop` method.

## Sets

A set is an unordered collection of unique elements. Sets are mutable and can contain elements of different types. Sets are created using curly braces `{}` and elements are separated by commas.

```python
# Syntax
set_name = {item1, item2, ...}
```

```python
# Example
fruits = {"apple", "banana", "cherry"}
```

In the example above, we define a set called `fruits` that contains three string elements.

### Adding and Removing Elements

You can add new elements to a set using the `add` method, and remove elements using the `remove` method.

```python
# Syntax
set_name.add(new_item)
set_name.remove(item)
```

```python
# Example
fruits = {"apple", "banana", "cherry"}
fruits.add("orange")
print(fruits)  # Output: {'apple', 'banana', 'cherry', 'orange'}

fruits.remove("banana")
print(fruits)  # Output: {'apple', 'cherry', 'orange'}
```

In the example above, we add "orange" to the `fruits` set using the `add` method, and remove "banana" from the set using the `remove` method.

### Set Operations

You can perform various set operations such as union, intersection, and difference using built-in methods.

```python
# Example
set1 = {1, 2, 3}
set2 = {3, 4, 5}

# Union
print(set1 | set2)  # Output: {1, 2, 3, 4, 5}

# Intersection
print(set1 & set2)  # Output: {3}

# Difference
print(set1 - set2)  # Output: {1, 2}
```

In the example above, we perform the union, intersection, and difference operations on two sets `set1` and `set2`.

## Exercises

1. Write a program to count the frequency of elements in a list.
2. Write a program to remove duplicates from a list.
3. Write a program to find the intersection of two lists.
4. Write a program to check if a set is a subset of another set.
5. Write a program to perform the symmetric difference of two sets.


