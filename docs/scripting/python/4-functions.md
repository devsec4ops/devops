# Functions

## Defining Functions

A function is a block of code that performs a specific task. It can take input, perform operations, and return a result. Functions are used to organize code into reusable blocks, which can be called from different parts of a program.

In Python, you can define a function using the `def` keyword followed by the function name and a pair of parentheses. The function body is indented and contains the code to be executed.

```python
# Syntax
def function_name(parameters):
    # function body
    # code block
```

```python
# Example
def greet(name):
    print("Hello, " + name)
```

In the example above, we define a function called `greet` that takes a single parameter `name`. The function body contains a single statement that prints a greeting message to the console.

## Arguments and Parameters

A function can take zero or more parameters as input. These parameters are specified in the function definition and are used to pass values to the function. When a function is called, the values passed to it are called arguments.

```python
# Syntax
def function_name(param1, param2, ...):
    # function body
    # code block
```

```python
# Example
def add(x, y):
    return x + y
```

In the example above, we define a function called `add` that takes two parameters `x` and `y`. The function body contains a single statement that returns the sum of the two parameters.

## Returning Values

A function can return a value using the `return` statement. The returned value can be used in the calling code.

```python
# Syntax
def function_name(parameters):
    # function body
    # code block
    return value
```

```python
# Example
def add(x, y):
    return x + y
```

In the example above, the `add` function returns the sum of the two parameters `x` and `y`. The calling code can use the returned value as needed.

## Scope and Lifetime of Variables

Variables defined inside a function are local to that function and cannot be accessed from outside. They have a limited scope and lifetime, which is determined by the function's execution.

```python
# Example
def greet(name):
    message = "Hello, " + name
    print(message)

greet("Alice")
print(message)  # NameError: name 'message' is not defined
```

In the example above, the `message` variable is defined inside the `greet` function and cannot be accessed from outside. Attempting to access it from the calling code results in a `NameError`.

Variables defined outside any function are global and can be accessed from any part of the program. However, it is good practice to avoid using global variables as much as possible, as they can lead to unexpected behavior and make the code harder to understand and maintain.