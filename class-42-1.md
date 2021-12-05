# **Pythonisms**

## **Enriching Your Python Classes With Dunder (Magic, Special) Methods**

### **What Are Dunder Methods?**

In Python, special methods are a set of predefined methods you can use to enrich your classes. They are easy to recognize because they start and end with double underscores, for example `__init__` or `__str__`.

As it quickly became tiresome to say under-under-method-under-under Pythonistas adopted the term `“dunder methods”`, a short form of “double under.”

These `“dunders”` or `“special methods”` in Python are also sometimes called “magic methods.” But using this terminology can make them seem more complicated than they really are—at the end of the day there’s nothing `“magical”` about them. You should treat these methods like a normal language feature.

Dunder methods let you emulate the behavior of built-in types. For example, to get the length of a string you can call len(`'string'`). But an empty class definition doesn’t support this behavior out of the box:
```py
class NoLenSupport:
    pass

>>> obj = NoLenSupport()
>>> len(obj)
TypeError: "object of type 'NoLenSupport' has no len()"
```
To fix this, you can add a `__len__` dunder method to your class:
```py
class LenSupport:
    def __len__(self):
        return 42

>>> obj = LenSupport()
>>> len(obj)
42
```


### **Object Initialization: `__init__`**

Right upon starting my class I already need a special method. To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:
```py
class Account:
    """A simple account class"""

    def __init__(self, owner, amount=0):
        """
        This is the constructor that lets us create
        objects from this class
        """
        self.owner = owner
        self.amount = amount
        self._transactions = []
```
The constructor takes care of setting up the object. In this case it receives the owner name, an optional start amount and defines an internal transactions list to keep track of deposits and withdrawals.

This allows us to create new accounts like this:
```py
>>> acc = Account('bob')  # default amount = 0
>>> acc = Account('bob', 10)
```

### **Object Representation: `__str__`, `__repr__`**

It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

1.  `__repr__`: The “official” string representation of an object. This is how you would make an object of the class. The goal of `__repr__` is to be unambiguous.

2.  `__str__`: The “informal” or nicely printable string representation of an object. This is for the enduser.

Let’s implement these two methods on the Account class:
```py
class Account:
    # ... (see above)

    def __repr__(self):
        return 'Account({!r}, {!r})'.format(self.owner, self.amount)

    def __str__(self):
        return 'Account of {} with starting amount: {}'.format(
            self.owner, self.amount)
```
If you don’t want to hardcode "Account" as the name for the class you can also use self.`__class__`.`__name__` to access it programmatically.

If you wanted to implement just one of these to-string methods on a Python class, make sure it’s `__repr__`.

Now I can query the object in various ways and always get a nice string representation:
```py
>>> str(acc)
'Account of bob with starting amount: 10'

>>> print(acc)
"Account of bob with starting amount: 10"

>>> repr(acc)
"Account('bob', 10)"

```

***

**To know more please [visit this page](https://dbader.org/blog/python-dunder-methods)**

