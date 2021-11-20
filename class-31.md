# **Django for APIs - Library Website**

Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework; it always must be added to a project after Django itself has been installed and configured.

The most important takeaway is that Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.

## **Django REST Framework**

Django REST Framework is added just like any other third-party app. Make sure to quit the local server Control + c if it is still running. Then on the command line type the below.**
```bash
(library) $ pipenv install djangorestframework~=3.11.0
```

Add it to the `INSTALLED_APPS` config in our `settings.py` file. I like to make a distinction between third-party apps and local apps as follows since the number of apps grows quickly in most projects.
```py
# config/settings.py
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',

    # 3rd party
    'rest_framework', # new

    # Local
    'books',
]
```

Let’s first create a new api app.

```
(library) $ python manage.py startapp api
```
Then add it to `INSTALLED_APPS`.

Let’s start with our `URL` configs. Adding an API endpoint is just like configuring a traditional Django app’s routes. First at the project-level we need to include the api app and configure its URL route, which will be api/.
```pay
# config/urls.py
from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('api/', include('api.urls')), # new
    path('', include('books.urls')),
]
```

Then create a `urls.py` file within the api app.
```bash
(library) $ touch api/urls.py
```
And update it as follows:

```py
# api/urls.py
from django.urls import path
from .views import BookAPIView

urlpatterns = [
    path('', BookAPIView.as_view()),
]
```
All set.

Next up is our `views.py` file which relies on Django REST Framework’s built-in generic class views. These deliberately mimic traditional Django’s generic class-based views in format, but they are not the same thing.

To avoid confusion, some developers will call an API views file `apiviews.py` or `api.py`. Personally, when working within a dedicated api app I do not find it confusing to just call a Django REST Framework views file views.py but opinion varies on this point.

Within our views.py file, update it to look like the following:
```py
# api/views.py
from rest_framework import generics

from books.models import Book
from .serializers import BookSerializer


class BookAPIView(generics.ListAPIView):
    queryset = Book.objects.all()
    serializer_class = BookSerializer
```

***

**To know more please [visit this page](https://djangoforapis.com/library-website-and-api/)**

***