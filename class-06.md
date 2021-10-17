
# Game of Greed 1

## **How to use the Random Module in Python**:

**Randint**

If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.

```bash
import random
print random.randint(0, 5)
```

This will output either 1, 2, 3, 4 or 5.

**Random**

If you want a larger number, you can multiply it.

For example, a random number between 0 and 100:

```bash
import random
random.random() * 100
```

**Choice**

Generate a random value from the sequence sequence.

```bash
random.choice( ['red', 'black', 'green'] ).
```
The choice function can often be used for choosing a random element from a list.

import random
```bash
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```
**Shuffle**

The shuffle function, shuffles the elements in list in place, so they are in a random order.

random.shuffle(list) Example taken from this post on Stackoverflow

```bash
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
```
Output:
```bash
# print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]

# of course your results will vary
```
**Randrange**

Generate a randomly selected element from range(start, stop, step)

```bash
random.randrange(start, stop[, step])
import random
for i in range(3):
    print random.randrange(0, 101, 5)

```

--------
**To know more please 
[visit this page](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)**
----------
----------------



## **What is Risk Analysis**

**What is Risk Analysis in Software Testing and how to perform it?**

In **Software Testing**, **risk analysis** is the process of identifying the risks in applications or software that you built and prioritizing them to test. 


**Why use Risk Analysis?**

In any software, using **risk analysis** at the beginning of a project highlights the potential problem areas. 

After knowing about the risk areas, it helps the developers and managers to mitigate the risks.

### **Risk Identification**
There are different sets of risks included in the risk identification process. Those are as follows:

**Business Risks:** This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

**Testing Risks:** You should be well acquainted with the platform you are working on, along with the software testing tools being used.

**Premature Release Risk:** a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

**Software Risks:** You should be well versed with the risks associated with the software development process.



--------
**To know more about  
[Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/)**
-------
-----------

## **Test Coverage**

**Test coverage** is a useful tool for finding untested parts of a codebase. 

**Test coverage** is of little use as a numeric statement of how good your tests are.

Like most aspects of programming, **testing requires** thoughtfulness. 

**TDD** is a very useful, but certainly not sufficient, tool to help you get good tests. If you are testing thoughtfully and well, 

I would expect a coverage percentage in the upper 80s or 90s. I would be suspicious of anything like 100% - it would smell of someone writing tests to make the coverage numbers happy, but not thinking about what they are doing.

The reason, of course, why people focus on coverage numbers is because they want to know if they are testing enough. 

Certainly low coverage numbers, say below half, are a sign of trouble. But high numbers don't necessarily mean much, and lead to ignorance-promoting dashboards. 

Sufficiency of testing is much more complicated attribute than coverage can answer. 

I would say you are doing enough testing if the following is true:

-   You rarely get bugs that escape into production, and
-   You are rarely hesitant to change some code for fear it will cause production bugs.





--------
**To know more about  
[Test Coverage](https://martinfowler.com/bliki/TestCoverage.html)**
-------
-----------

## **Big O Notation**

**Big O** is essentially an equation that describes how the runtime scales with respect to some input variables

This efficiency is evaluated based on 2 factors:

    Running Time (also known as time efficiency / complexity).
    The amount of time a function needs to complete.
***
    Memory Space (also known as space efficiency / complexity).
    The amount of memory resources a function uses to store data and instructions.

**O(1)** function takes constant time, which is to say that it doesn’t matter how many elements we have, or how huge our input is: it’ll always take the same amount of time and memory to run our algorithm.

**O(n)** function is linear, which means that as our input grows (from ten numbers, to ten thousand, to ten million), the space and time that we need to run that algorithm grows linearly.



--------
**To know more about  
[Test Coverage](https://martinfowler.com/bliki/TestCoverage.html)**
-------
-----------