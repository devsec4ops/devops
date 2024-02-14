# Exception Handling

In Python, exceptions are used to handle errors and other exceptional events. When an error occurs, Python raises an exception, which can be caught and handled by the programmer. This allows you to write code that gracefully handles errors and prevents the program from crashing.

## Try-Except Blocks

You can use the `try` and `except` keywords to catch and handle exceptions in Python. The `try` block contains the code that may raise an exception, and the `except` block contains the code to handle the exception.

```python
# Syntax
try:
    # code that may raise an exception
except ExceptionType:
    # code to handle the exception
```

```python
# Example
try:
    x = 10 / 0
except ZeroDivisionError:
    print("Error: Division by zero")
```

In the example above, we attempt to divide 10 by 0, which raises a `ZeroDivisionError` exception. We catch the exception using the `except` block and print an error message to the console.

You can also catch multiple exceptions using a single `except` block.

```python
# Example
try:
    x = 10 / 0
except (ZeroDivisionError, ValueError):
    print("Error: Division by zero or invalid value")
```

In the example above, we catch both `ZeroDivisionError` and `ValueError` exceptions using a single `except` block.

## Finally Block

You can use the `finally` block to execute code that should always run, regardless of whether an exception is raised or not. This is useful for releasing resources or cleaning up after an operation.

```python
# Syntax
try:
    # code that may raise an exception
except ExceptionType:
    # code to handle the exception
finally:
    # code that always runs
```

```python
# Example
try:
    file = open("example.txt", "r")
    content = file.read()
except FileNotFoundError:
    print("Error: File not found")
finally:
    file.close()
```

In the example above, we attempt to open and read the contents of a file. If the file is not found, a `FileNotFoundError` exception is raised, and we print an error message to the console. The `finally` block ensures that the file is closed, regardless of whether an exception is raised or not.

## Raising Exceptions

You can raise exceptions using the `raise` keyword. This allows you to signal that an error has occurred and provide information about the error.

```python
# Syntax
raise ExceptionType("error message")
```

```python
# Example
def divide(x, y):
    if y == 0:
        raise ZeroDivisionError("Division by zero")
    return x / y

try:
    result = divide(10, 0)
except ZeroDivisionError as e:
    print("Error:", e)
```

In the example above, we define a function called `divide` that raises a `ZeroDivisionError` exception if the second argument is 0. We then call the function and catch the exception using the `except` block.

## Custom Exceptions

You can create your own custom exceptions by defining a new class that inherits from the `Exception` class.

```python
# Example
class CustomError(Exception):
    pass

try:
    raise CustomError("An error occurred")
except CustomError as e:
    print("Error:", e)
```

In the example above, we define a new class called `CustomError` that inherits from the `Exception` class. We then raise an instance of the `CustomError` class and catch it using the `except` block.

## Common Exceptions in Python

Python has a wide range of built-in exceptions that are raised for various error conditions. Some of the most commonly used exceptions include:

- `ZeroDivisionError`: Raised when division or modulo by zero is encountered.
- `ValueError`: Raised when a function receives an argument of the correct type but an inappropriate value.
- `TypeError`: Raised when an operation or function is applied to an object of inappropriate type.
- `FileNotFoundError`: Raised when a file or directory is requested but cannot be found.
- `KeyError`: Raised when a dictionary key is not found.
- `IndexError`: Raised when a sequence subscript is out of range.
- `NameError`: Raised when a local or global name is not found.
- `ImportError`: Raised when an import statement fails to find the module definition.
- `SyntaxError`: Raised when the parser encounters a syntax error.
- `IndentationError`: Raised when the indentation is incorrect.
- `RuntimeError`: Raised when an error is detected that doesn't fall into any of the other categories.