# Indentation in Python

In Python, indentation is used to define a block of code. The standard indentation is 4 spaces. 

```python
# Example
x = 10
if x > 5:
    print('x is greater than 5')
```

If you use a different number of spaces or tabs, Python will raise an `IndentationError`.

```python
# Example
x = 10
if x > 5:
    print('x is greater than 5') # IndentationError
```

# Control Flow

## Conditional Statements

Conditional statements are used to execute a block of code based on a condition. 

### `if` Statements

The `if` statement is the most basic form of a conditional statement. It is used to execute a block of code if a condition is true.

```python
# Syntax
if condition:
    # code block
```

The `if` statement is followed by a condition. If the condition is true, the code block is executed. If the condition is false, the code block is skipped.

```python
# Example
x = 10
if x > 5:
    print('x is greater than 5')
```

### `if`-`else` Statements

The `if` statement can be followed by an `else` statement. The `else` statement is used to execute a block of code if the condition is false.

```python
# Syntax
if condition:
    # code block
else:
    # code block
```

```python
# Example
x = 3
if x > 5:
    print('x is greater than 5')
else:
    print('x is less than or equal to 5')
```

### `if`-`elif`-`else` Statements

The `if` statement can be followed by one or more `elif` (else if) statements. The `elif` statement is used to check additional conditions if the previous conditions are false.

```python
# Syntax
if condition:
    # code block
elif condition:
    # code block
else:
    # code block
```

```python
# Example
x = 3
if x > 5:
    print('x is greater than 5')
elif x == 5:
    print('x is equal to 5')
else:
    print('x is less than 5')
```

### Nested `if` Statements

`if` statements can be nested inside other `if` statements. This is useful when you want to check for additional conditions.

```python
# Example
x = 10
y = 5
if x > 5:
    if y > 5:
        print('x and y are greater than 5')
    else:
        print('x is greater than 5, but y is less than or equal to 5')
else:
    print('x is less than or equal to 5')
```

## Loops

Loops are used to execute a block of code multiple times.

### `for` Loops

The `for` loop is used to iterate over a sequence (e.g., a list, tuple, string).

```python
# Syntax
for item in sequence:
    # code block
```

```python
# Example
fruits = ['apple', 'banana', 'cherry']
for fruit in fruits:
    print(fruit)
```

### `while` Loops

The `while` loop is used to execute a block of code as long as a condition is true.

```python
# Syntax
while condition:
    # code block
```

```python
# Example
x = 0
while x < 5:
    print(x)
    x += 1
```

### Nested Loops

Loops can be nested inside other loops. This is useful when you want to iterate over multiple sequences.

```python
# Example
adj = ['red', 'big', 'tasty']
fruits = ['apple', 'banana', 'cherry']
for a in adj:
    for f in fruits:
        print(a, f)
```

## Exercises

1. Write a program to check if a number is positive, negative, or zero.
2. Write a program to find the sum of all numbers in a list.
3. Write a program to find the factorial of a number.
4. Write a program to print the Fibonacci series up to `n` terms.
5. Write a program to check if a number is prime or not.
6. Write a program to check if a string is a palindrome.
