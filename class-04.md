
# Topics
## **Classes and Objects**:

**Objects** are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. 

**Classes** are essentially a template to create your objects.

```bash
class MyClass: #Class
    variable = "blah"

    def function(self):
        print("This is a message inside the class.")

myobjectx = MyClass() #Object
```
 
**Accessing Object Variables**

```bash
myobjectx.variable
```

**Accessing Object Functions**

```bash
myobjectx.function()
```

--------
**To know more please 
[visit this page](https://www.learnpython.org/en/Classes_and_Objects)**
----------
----------------



## **Thinking Recursively**

**recursive function** is a function defined in terms of itself by self-referential expressions.

This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. 

All recursive functions share a common structure made up of two parts: base case and recursive case.

To demonstrate this structure, let’s write a recursive function for calculating n!:

**1-** Decompose the original problem into simpler instances of the same problem. This is the recursive case:

n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1

n! = n x (n−1)!

**2-** As the large problem is broken down into successively less complex ones, those subproblems must eventually become so simple that they can be solved without further subdivision. This is the base case:

n! = n x (n−1)! 
n! = n x (n−1) x (n−2)!
n! = n x (n−1) x (n−2) x (n−3)!
⋅
⋅
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3!
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2!
n! = n x (n−1) x (n−2) x (n−3) ⋅⋅⋅⋅ x 3 x 2 x 1!
Here, 1! is our base case, and it equals 1.

Recursive function for calculating n! implemented in Python:

```bash
def factorial_recursive(n):
    # Base case: 1! = 1
    if n == 1:
        return 1

    # Recursive case: n! = n * (n-1)!
    else:
        return n * factorial_recursive(n-1)
 
>>> factorial_recursive(5)
120
```
--------
**To know more please 
[visit this page](https://realpython.com/python-thinking-recursively/#recursive-functions-in-python)**
-------
-----------

## **Pytest Fixtures and Coverage**

**Fixtures**

When you're writing tests, you're rarely going to write just one or two. Rather, you're going to write an entire "test suite", with each test aiming to check a different path through your code. In many cases, this means you'll have a few tests with similar characteristics, something that pytest handles with "parametrized tests".

But in other cases, things are a bit more complex. You'll want to have some objects available to all of your tests. Those objects might contain data you want to share across tests, or they might involve the network or filesystem. These are often known as "fixtures" in the testing world, and they take a variety of different forms.

In pytest, you define fixtures using a combination of the pytest.fixture decorator, along with a function definition. For example, say you have a file that returns a list of lines from a file, in which each line is reversed:



```bash
def reverse_lines(f):
   return [one_line.rstrip()[::-1] + '\n'
           for one_line in f]
```

**Coverage**

This is all great, but if you've ever done any testing, you know there's always the question of how thoroughly you have tested your code. After all, let's say you've written five functions, and that you've written tests for all of them. Can you be sure you've actually tested all of the possible paths through those functions?

For example, let's assume you have a very strange function, only_odd_mul, which multiplies only odd numbers:
```bash
def only_odd_mul(x, y):
   if x%2 and y%2:
       return x * y
   else:
       raise NoEvenNumbersHereException(f'{x} and/or {y}
 ↪not odd')
```
Here's a test you can run on it:
```bash
def test_odd_numbers():
   assert only_odd_mul(3, 5) == 15
```
--------
**To know more please 
[visit this page](https://www.linuxjournal.com/content/python-testing-pytest-fixtures-and-coverage)**
-------
-----------