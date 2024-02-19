# *Course 401 Python, Entry 31: Django REST Framework & Docker

**What are the key components of a Docker container, and how do they help streamline the development and deployment of applications?**

- Docker can be used to isolate any application on any OS.
- Docker is a way to implement Linux containers, a local virtualization platform.
- Allows for production databases
- Allows to select out a version, rather than an installed package.
- Docker contains images and containers. Images are a snapshot of a project, a container is a running instance of the image.

**Describe the primary steps involved in building a library website using Django, including essential components like models, views, and templates.**


1. Create a new virtual environment, activate it, and install Django.
2. Run the startproject line. `django-admin startproject django_project .`
3. Migrate. `python3 manage.py migrate`
4. Verify working with runserver. `python3 manage.py runserver`

---

5. Create new app. `python3 manage.py startapp books`
6. Add app to INSTALLED_APPS in settings.py. `"books.apps.BooksConfig",`
7. Models.py. Update to as follows:

```
# books/models.py
from django.db import models


class Book(models.Model):
    title = models.CharField(max_length=250)
    subtitle = models.CharField(max_length=250)
    author = models.CharField(max_length=100)
    isbn = models.CharField(max_length=13)

    def __str__(self):
        return self.title
```

8. Run makemigrations for the books app. `python3 manage.py makemigrations books`
9. Now migrate. `python3 manage.py migrate`
10. Admin. Create a superuser account. `python3 manage.py createsuperuser`
11. Update books admin.py.

```
# books/admin.py
from django.contrib import admin

from .models import Book

admin.site.register(Book)
```
12. Views. Update to as follows:

```
# books/views.py
from django.views.generic import ListView

from .models import Book


class BookListView(ListView):
    model = Book
    template_name = "book_list.html"
```

13. URLs. Update the top-level urls to as follows:

```
# django_project/urls.py
from django.contrib import admin
from django.urls import path, include  # new

urlpatterns = [
    path("admin/", admin.site.urls),
    path("", include("books.urls")),  # new
]
```

14. Create a urls file for the app as follows:

```
# books/urls.py
from django.urls import path

from .views import BookListView

urlpatterns = [
    path("", BookListView.as_view(), name="home"),
]
```

15. Create a file `books/templates/books/book_list.htm` and edit as follows:

```
<!-- books/templates/books/book_list.html -->
<h1>All books</h1>
{% for book in book_list %}
<ul>
  <li>Title: {{ book.title }}</li>
  <li>Subtitle: {{ book.subtitle }}</li>
  <li>Author: {{ book.author }}</li>
  <li>ISBN: {{ book.isbn }}</li>
</ul>
{% endfor %}
```

**Can you explain the primary differences between Django and Django REST framework?**

The major differences with Django REST are:

- Installing framework.
- Serialization snippet - created to transform data into JSON.
- Saved method for when receiving data.
- Add endpoints to users in model.

----

- Add user authentication to views.
- Adding log in.
- Object level permissions.
- Root API endpoint.

----

- HTML Render
- API Hyperlinking
- Pagination

## Things I want to know more about

How to streamline the installation of all the Django REST components.
