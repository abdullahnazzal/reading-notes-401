
# Game of Greed 3

## **List Comprehensions**:

List comprehension is a powerful and concise method for creating lists in Python that becomes essential the more you work with lists, and lists of lists.

**Syntax:**
my_new_list = [ expression for item in list ]


**Create a List with range()**

Let’s start by creating a list of numbers using Python list comprehensions. We’ll take advantage of Python’s **range()** method as a way to create a list of digits.

-   **Example 1: Creating a list with list comprehensions**


 ```bash
# construct a basic list using range() and list comprehensions
# syntax
# [ expression for item in list ]
digits = [x for x in range(10)]

print(digits)
```
Output
```bash
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

**Create a List Using Loops and List Comprehension in Python**

-   **Example 2: Comparing list creation methods in Python**

First, create a list and loop through it. Add an expression, in this example, we’ll raise x to the power of 2.

```bash
# create a list using a for loop
squares = []

for x in range(10):
    # raise x to the power of 2
    squares.append(x**2)

print(squares)
```
Output

```bash
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```


**Multiplying Parts of a List**

-   **Example 3: Multiplication with list comprehensions**

What if we wanted to multiply every number in a list by three in Python? We could write a for loop and store the results in a new list, or we could use list comprehensions.



```bash
# create a list with list comprehensions
multiples_of_three = [ x*3 for x in range(10) ]

print(multiples_of_three)
```
Output

```bash
[0, 3, 6, 9, 12, 15, 18, 21, 24, 27]
```
--------
**To know more please 
[visit this page](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)**

