# **Custom User Model**

Django ships with a built-in User model for authentication and if you'd like a basic tutorial on how to implement log in, log out, sign up and so on see the Django Login and Logout tutorial for more.
![Forms](assist/admin_book_add.png)

## **AbstractUser vs AbstractBaseUser**

There are two modern ways to create a custom user model in Django: `AbstractUser` and `AbstractBaseUser`. In both cases we can subclass them to extend existing functionality however `AbstractBaseUser` requires much, much more work. Seriously, don't mess with it unless you really know what you're doing. And if you did, you wouldn't be reading this tutorial, would you?

So we'll use `AbstractUser` which actually subclasses `AbstractBaseUser` but provides more default configuration.

## **Custom User Model**

Creating our initial custom user model requires four steps:

    update config/settings.py
    create a new CustomUser model
    create new UserCreation and UserChangeForm
    update the admin

```py
from django import forms
from django.contrib.auth.forms import UserCreationForm, UserChangeForm
from .models import CustomUser

class CustomUserCreationForm(UserCreationForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')

class CustomUserChangeForm(UserChangeForm):

    class Meta:
        model = CustomUser
        fields = ('username', 'email')

```

***

**To know more please [visit this page](https://learndjango.com/tutorials/django-custom-user-model)**

***