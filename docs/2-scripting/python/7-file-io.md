# File IO

## Reading Files

Python has a built-in function called `open()` that allows you to open and read files. The `open()` function takes two arguments: the name of the file and the mode in which you want to open the file. The mode can be `r` for reading, `w` for writing, or `a` for appending.

```python
# Syntax
file = open("filename", "mode")
```

```python
# Example
file = open("example.txt", "r")
```

In the example above, we open a file called `example.txt` in read mode.

### Reading the Entire File

You can read the entire contents of a file using the `read()` method.

```python
# Syntax
file.read()
```

```python
# Example
file = open("example.txt", "r")
content = file.read()
print(content)
```

In the example above, we read the entire contents of the file `example.txt` and store it in a variable called `content`. We then print the contents of the file to the console.

### Reading Line by Line

You can also read the contents of a file line by line using the `readline()` method.

```python
# Syntax
file.readline()
```

```python
# Example
file = open("example.txt", "r")
line1 = file.readline()
line2 = file.readline()
print(line1)
print(line2)
```

In the example above, we read the first two lines of the file `example.txt` and store them in variables called `line1` and `line2`. We then print the contents of the variables to the console.

### Closing Files

After you have finished working with a file, you should close it using the `close()` method.

```python
# Syntax
file.close()
```

```python
# Example
file = open("example.txt", "r")
content = file.read()
file.close()
```

In the example above, we open the file `example.txt`, read its contents, and then close the file.

Alternatively, you can use the `with` statement to open and close files automatically.

```python
# Example
with open("example.txt", "r") as file:
    content = file.read()
```

In the example above, the file is automatically closed when the `with` block is exited.

## Writing to Files

You can write to files using the `write()` method.

```python
# Syntax
file.write("text")
```

```python
# Example
with open("example.txt", "w") as file:
    file.write("Hello, world!")
```

In the example above, we open the file `example.txt` in write mode and write the text "Hello, world!" to the file.

### Appending to Files

You can append to files using the `write()` method with the `a` mode.

```python
# Example
with open("example.txt", "a") as file:
    file.write("Hello, again!")
```

In the example above, we open the file `example.txt` in append mode and write the text "Hello, again!" to the file.

## Working with CSV Files

Python has a built-in module called `csv` that allows you to read and write CSV files.

```python
# Example
import csv

with open("example.csv", "r") as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
```

In the example above, we use the `csv` module to read the contents of a CSV file called `example.csv` and print each row to the console.

You can also write to CSV files using the `csv.writer` class.

```python
# Example
import csv

with open("example.csv", "w") as file:
    writer = csv.writer(file)
    writer.writerow
    writer.writerow(["Name", "Age"])
    writer.writerow(["Alice", 25])
    writer.writerow(["Bob", 30])
```

In the example above, we use the `csv.writer` class to write data to a CSV file called `example.csv`. We first write the column headers, and then write the data for each row.

## Other File Formats

Python has built-in support for working with other file formats such as JSON, XML, and more. You can use third-party libraries to work with these file formats as well.

```python
# Example
import json

data = {
    "name": "Alice",
    "age": 25
}

with open("example.json", "w") as file:
    json.dump(data, file)
```

In the example above, we use the `json` module to write a Python dictionary to a JSON file called `example.json`.

