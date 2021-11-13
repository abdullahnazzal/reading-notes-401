# **Intro to Django**

## **Why Django?**

With Django, you can take web applications from concept to launch in a matter of hours. Django takes care of much of the hassle of web development, so you can focus on writing your app without needing to reinvent the wheel. It’s free and open source.

## **Object-relational mapper**

Deﬁne your data models entirely in Python. You get a rich, dynamic database-access API for free — but you can still write SQL if needed.


A **model** is the single, definitive source of information about your data. It contains the essential fields and behaviors of the data you’re storing. Generally, each model maps to a single database table.

The basics:

1- Each model is a Python class that subclasses django.db.models.Model.

2- Each attribute of the model represents a database field.

3- With all of this, Django gives you an automatically-generated database-access API; see Making queries.

```py
from django.db import models

class Person(models.Model):
    first_name = models.CharField(max_length=30)
    last_name = models.CharField(max_length=30)
```

first_name and last_name are fields of the model. Each field is specified as a class attribute, and each attribute maps to a database column.

**Using models**

Once you have defined your models, you need to tell Django you’re going to use those models. 

Do this by editing your settings file and changing the INSTALLED_APPS setting to add the name of the module that contains your models.py.

For example, if the models for your application live in the module myapp.

models (the package structure that is created for an application by the manage.py startapp script), INSTALLED_APPS should read, in part:

```py
INSTALLED_APPS = [
    #...
    'myapp',
    #...
]
```

When you add new apps to INSTALLED_APPS, be sure to run manage.py migrate, optionally making migrations for them first with manage.py makemigrations.

**Fields**

The most important part of a model – and the only required part of a model – is the list of database fields it defines. Fields are specified by class attributes. Be careful not to choose field names that conflict with the models API like clean, save, or delete.

**Example:**

```py
from django.db import models

class Musician(models.Model):
    first_name = models.CharField(max_length=50)
    last_name = models.CharField(max_length=50)
    instrument = models.CharField(max_length=100)

class Album(models.Model):
    artist = models.ForeignKey(Musician, on_delete=models.CASCADE)
    name = models.CharField(max_length=100)
    release_date = models.DateField()
    num_stars = models.IntegerField()
```


**Field types**

Each field in your model should be an instance of the appropriate Field class. Django uses the field class types to determine a few things:

-   The column type, which tells the database what kind of data to store (e.g. INTEGER, VARCHAR, TEXT).

-   The default HTML widget to use when rendering a form field ```(e.g.<input type="text">, <select>).```

-   The minimal validation requirements, used in Django’s admin and in automatically-generated forms.

Django ships with dozens of built-in field types; you can find the complete list in the model field reference. You can easily write your own fields if Django’s built-in ones don’t do the trick; see Writing custom model fields.

***

**To know more please [visit this page](https://www.djangoproject.com/start/)**

***
