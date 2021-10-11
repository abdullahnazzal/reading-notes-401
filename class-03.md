
# FileIO & Exceptions
## **Reading and Writing Files in Python (Guide)**:

One of the most common tasks that you can do with Python is reading and writing files.

**Files on most modern file systems are composed of three main parts:**

1- Header: metadata about the contents of the file (file name, size, type, and so on)

2- Data: contents of the file as written by the creator or editor

3- End of file (EOF): special character that indicates the end of the file


**File Paths**

When you access a file on an operating system, a file path is required. The file path is a string that represents the location of a file. It’s broken up into three major parts:

**Folder Path:** the file folder location on the file system where subsequent folders are separated by a forward slash / (Unix) or backslash \ (Windows)

**File Name:** the actual name of the file

**Extension:** the end of the file path pre-pended with a period (.) used to indicate the file type.

Here’s a quick example:

```bash
/
│
├── path/
|   │
│   ├── to/
│   │   └── cats.gif
│   │
│   └── dog_breeds.txt
|
└── animals.csv
```

<br>

**Opening and Closing a File in Python**

```bash
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```

**Reading and Writing Opened Files**
```bash

with open('dog_breeds.txt', 'r') as reader:
    # Note: readlines doesn't trim the line endings
    dog_breeds = reader.readlines()

with open('dog_breeds_reversed.txt', 'w') as writer:
    # Alternatively you could use
    # writer.writelines(reversed(dog_breeds))

    # Write the dog breeds to the file in reversed order
    for breed in reversed(dog_breeds):
        writer.write(breed)
```

--------
**To know more please 
[visit this page](https://realpython.com/read-write-files-python/)**
----------
----------------



## **Python Exceptions: An Introduction**

A Python program terminates as soon as it encounters an error. In Python, an error can be a syntax error or an exception.

**Syntax errors** occur when the parser detects an incorrect statement.

**exception error** This type of error occurs whenever syntactically correct Python code results in an error. 

### **Raising an Exception**

We can use raise to throw an exception if a condition occurs. The statement can be complemented with a custom exception.

```bash
x = 10
if x > 5:
    raise Exception('x should not exceed 5. The value of x was: {}'.format(x))
```
**The AssertionError Exception**
Instead of waiting for a program to crash midway, you can also start by making an assertion in Python. We assert that a certain condition is met. If this condition turns out to be True, then that is excellent! The program can continue. If the condition turns out to be False, you can have the program throw an `AssertionError` exception.

```bash
import sys
assert ('linux' in sys.platform), "This code runs on Linux only."

```

**The try and except Block: Handling Exceptions**

The try and except block in Python is used to catch and handle exceptions.

Python executes code following the try statement as a “normal” part of the program.

The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.

```bash
def linux_interaction():
    assert ('linux' in sys.platform), "Function can only run on Linux systems."
    print('Doing something.')
try:
    linux_interaction()
except:
    print('Linux function was not executed')
```
Another Example:
```bash
try:
    with open('file.log') as file:
        read_data = file.read()
except FileNotFoundError as fnf_error:
    print(fnf_error)
```

--------
**To know more please 
[visit this page](https://realpython.com/python-exceptions/)**
-------
-----------
