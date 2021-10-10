
# Testing and Modules
## **Unit tests and TDD?**:

Unit tests are some pieces of code to exercise the input, the output and the behaviour of your code. You can write them anytime you want.

But Test-Driven Development is a strategy to think (and write!) tests first.

<br>

**Example of Unit Testing in TDD**

Once you know how to isolate the complex code and write structures and solid tests with the unit testing framework, the next step is to identify when to write the tests. In the traditional development approach, unit testing comes after the code has been written.

In TDD when you start unit testing, first you have to think of an outcome you want which you don’t currently have. You code towards that outcome. You run the code to see if you now have the outcome you wanted.

Sometimes developers find it very difficult to get an idea about what they expect from writing tests first. How to get the vague idea about the functions which are not written?

When you start writing code you think about the goal and how the function should work. To achieve the goal you require appropriate input data and expect what kind of results it will give back.

Let’s understand the process of TDD with unit tests by taking an example of a “table reservation system” used in the restaurant.

Cancellation can be done by two types of user:

**Step 1: Write the test case**
```json
[TestMethod]
public void CanBecancelledBy_UserIsAdmin_ReturnsTrue()
{
     
     var reservation= new Reservation();

     var result = reservation.CanBecancelledBy(new user { IsAdmin = true });

          Assert.IsTrue (result);
}

[TestMethod]
public void CanBecancelledBy_SameUserCancellingTheReservation_ReturnsTrue()
{
     
     var user= new User();
     var reservation = new Reservation { MadeBy = user };

     var result = reservation.CanBeCancelledBy(user);
     
     Assert.IsTrue (result);
}

[TestMethod]
public void CanBecancelledBy_AnotherUserCancellingReservation_ReturnsFalse()
    {
         
         var reservation = new Reservation { MadeBy = new user() };
    
         var result = reservation.CanBeCancelledBy(new user());
         
         Assert.IsFalse (result);
    }

```
**Step 2: Write a minimal production code**

At this stage, developers know should be the output based on input data. In our example, we know our output that cancellation request should pass for two types of users and fail for other users.

```json
Public class Reservation
{
      public User MadeBy { get; set; }
      public bool CanBeCancelledBy(User user)
      {
           If (user)
               return true;
      }
}
```

**Step 3: Refactor**

Now, to get the expected output we need to refactor our code where we will specify the user type.

```json
Public class Reservation
{
      public User MadeBy { get; set; }
      public bool CanBeCancelledBy(User user)
      {
           return (user.IsAdmin || MadeBy = user)
              
      }
}
```

*****

## ***Takeaways***

**I hope this was fun for you! To remember:**

- The greatest advantage about TDD is to craft the software design first.

- Your code will be more reliable: after a change you can run your tests and be in peace.

- Beginning may be hard — and that’s fine. You just need to practice!.


--------
**To know more please 
[visit this page](https://code.likeagirl.io/in-tests-we-trust-tdd-with-python-af69f47e6932)**
----------
----------------



## **If name equals main**

If the python interpreter is running that module (the source file) as the main program, it sets the special __name__ variable to have a value “__main__”.

If this file is being imported from another module, __name__ will be set to the module’s name. Module’s name is available as value to __name__ global variable. 

```json

# Python program to execute
# main directly
print ("Always executed")
 
if __name__ == "__main__":
    print ("Executed when invoked directly")
else:
    print ("Executed when imported")

```


### **Advantages :**
- Every Python module has it’s __name__ defined and if this is ‘__main__’, it implies that the module is being run standalone by the user and we can do corresponding appropriate actions.

- If you import this script as a module in another script, the __name__ is set to the name of the script/module.

- Python files can act as either reusable modules, or as standalone programs.

- if __name__ == “main”: is used to execute some code only if the file was run directly, and not imported.


--------
**To know more please 
[visit this page](https://www.geeksforgeeks.org/what-does-the-if-__name__-__main__-do/)**
-------


--------------------------

## **Recursion**

**What is Recursion? 
**
The process in which a function calls itself directly or indirectly is called recursion and the corresponding function is called as recursive function.

Using recursive algorithm, certain problems can be solved quite easily.

Examples of such problems are Towers of Hanoi (TOH), Inorder/Preorder/Postorder Tree Traversals, DFS of Graph, etc.

```json
int fact(int n)
{
    if (n < = 1) // base case
        return 1;
    else    
        return n*fact(n-1);    
}
```

**What is the difference between direct and indirect recursion?**

A function fun is called direct recursive if it calls the same function fun.

A function fun is called indirect recursive if it calls another function say fun_new and fun_new calls fun directly or indirectly. 

Difference between direct and indirect recursion has been illustrated in Table 1. 


**// An example of direct recursion**
```json

void directRecFun()
{
    // Some code....

    directRecFun();

    // Some code...
}

// An example of indirect recursion
void indirectRecFun1()
{
    // Some code...

    indirectRecFun2();

    // Some code...
}
void indirectRecFun2()
{
    // Some code...

    indirectRecFun1();

    // Some code...
}

```

--------
**To know more please 
[visit this page](https://www.geeksforgeeks.org/recursion/)**
-------
-----------
