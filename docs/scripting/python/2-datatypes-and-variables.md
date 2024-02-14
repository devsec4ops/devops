# Data types and Variables

## Variables

Variables are used to store data in a program. They are like containers that hold values. You can think of them as labels that you can assign to values. In Python, you can create a variable by giving it a name and assigning a value to it using the `=` operator.

```python
# Assigning a value to a variable
x = 10
y = 3.14
name = "Alice"
is_student = True
```

## Data Types

### Numbers
* **Integers (int)**: represent whole numbers (positive, negative, or zero) with unlimited size. Examples: 10, -23, 0.

* **Floats (float)**: represent decimal numbers with limited precision (approximately 15 decimal places). Examples: 3.14, -5.2e10 (scientific notation).

### Strings 
* A string is a sequence of characters enclosed within single or double quotes. Examples: "hello", 'world', "123".

### Boolean
* A boolean value is either `True` or `False`. It is used to represent truth values. Examples: True, False.

### None
* The `None` keyword is used to represent the absence of a value. It is similar to `null` in other programming languages.

## Operators

### Arithmetic Operators
* `+` (addition)
* `-` (subtraction)
* `*` (multiplication)
* `/` (division)
* `%` (modulus)
* `**` (exponentiation)
* `//` (floor division)

```python
# Arithmetic operators
x = 10
y = 3
print(x + y)  # 13
print(x - y)  # 7
print(x * y)  # 30
print(x / y)  # 3.3333333333333335
print(x % y)  # 1
print(x ** y) # 1000
print(x // y) # 3
```

### Comparison Operators
* `==` (equal to)
* `!=` (not equal to)
* `<` (less than)
* `>` (greater than)
* `<=` (less than or equal to)
* `>=` (greater than or equal to)

```python
# Comparison operators
x = 10
y = 5
print(x == y)  # False
print(x != y)  # True
print(x < y)   # False
print(x > y)   # True
print(x <= y)  # False
print(x >= y)  # True
```

### Logical Operators
* `and` (logical and)
* `or` (logical or)
* `not` (logical not)

```python
# Logical operators
x = True
y = False
print(x and y)  # False
print(x or y)   # True
print(not x)    # False
```

### Assignment Operators
* `=` (assign value)
* `+=` (add and assign)
* `-=` (subtract and assign)
* `*=` (multiply and assign)
* `/=` (divide and assign)
* `%=` (modulus and assign)
* `**=` (exponentiate and assign)
* `//=` (floor divide and assign)

```python
# Assignment operators
x = 10
x += 5  # equivalent to x = x + 5
x -= 3  # equivalent to x = x - 3
x *= 2  # equivalent to x = x * 2
x /= 4  # equivalent to x = x / 4
x %= 3  # equivalent to x = x % 3
x **= 2 # equivalent to x = x ** 2
x //= 5 # equivalent to x = x // 5
```

### Identity Operators
* `is` (object identity)
* `is not` (negated object identity)

```python
# Identity operators
x = [1, 2, 3]
y = [1, 2, 3]
z = x
print(x is y)    # False
print(x is not y) # True
print(x is z)    # True
```

### Membership Operators
* `in` (sequence membership)
* `not in` (negated sequence membership)

```python
# Membership operators
x = [1, 2, 3, 4, 5]
print(3 in x)    # True
print(6 not in x) # True
```

## Type Conversion

You can convert between different data types using built-in functions like `int()`, `float()`, `str()`, `bool()`, etc.

```python
# Type conversion
x = 10
y = 3.14
z = "20"
print(float(x))  # 10.0
print(int(y))    # 3
print(int(z))    # 20
print(str(x))    # '10'
print(bool(x))   # True
print(bool(0))   # False
```

## Input and Output

### Input
You can use the `input()` function to take user input from the keyboard. The input is always returned as a string.

```python
# Input
name = input("Enter your name: ")
print("Hello, " + name)
```

### Output
You can use the `print()` function to display output on the screen. You can pass multiple arguments to `print()` separated by commas.

```python
# Output
x = 10
y = 3.14
name = "Alice"
print("The value of x is", x)
print("The value of y is", y)
print("Hello,", name)
```

## Comments

Comments are used to explain the code and make it more readable. In Python, you can use the `#` symbol to write a single-line comment.

```python
# This is a single-line comment
```

For multi-line comments, you can enclose the text within triple quotes.

```python
"""
This is a
multi-line comment
"""
```

