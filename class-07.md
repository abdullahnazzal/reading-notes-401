
# Game of Greed 2

## **Python Scope**:

**The Global Scope**

From the moment you start a Python program, you’re in the global Python scope. Internally, Python turns your program’s main script into a module called **__ main __** to hold the main program’s execution. The namespace of this module is the main global scope of your program.

```
Note: In Python, the notions of global scope and global names are tightly associated with module files. For example, if you define a name at the top level of any Python module, then that name is considered global to the module. That’s the reason why this kind of scope is also called module scope.
```

If you’re working in a Python interactive session, then you’ll notice that **__ main __** is also the name of its main module. To check that out, open an interactive session and type in the following:

There’s only one global Python scope per program execution.

```

Note: Global names can be updated or modified from any place in your global Python scope. Beyond that, the global statement can be used to modify global names from almost any place in your code, as you’ll see in The global Statement.

Modifying global names is generally considered bad programming practice because it can lead to code that is:

-   Difficult to debug: Almost any statement in the program can change the value of a global name.

-   Hard to understand: You need to be aware of all the statements that access and modify global names.

-   Impossible to reuse: The code is dependent on global names that are specific to a concrete program.

Good programming practice recommends using local names rather than global names. Here are some tips:

-   Write self-contained functions that rely on local names rather than global ones.

-   Try to use unique objects names, no matter what scope you’re in.

-   Avoid global name modifications throughout your programs.

-   Avoid cross-module name modifications.

-   Use global names as constants that don’t change during your program’s execution.
```



--------
**To know more please 
[visit this page](https://realpython.com/python-scope-legb-rule/#modules-the-global-scope)**
----------
----------------



## **What is Risk Analysis**

**What is a Big O Natation**

Time complexity: How long an algorithm takes to do something.

Space complexity: how mush memory it takes up while is's doing it.

**Why is it necessary:**

It's a way of comparing algorithms with each other,
and it's a way of finding out how your algorithm will perform,

especially id you are design something that is mission-critical.

**Big O notation computational complexity:**

Constant Complexity: O(1),

Linear Complexity: O(n),

Quadratic Complexity: O(N²), 

Exponential: O(2^N), 

Logarithmic Complexity: O(log n)

--------
**To know more about  
[Watch the video](https://www.edureka.co/blog/risk-analysis-in-software-testing/)**
-------
-----------

