# *Course 401 Python, Entry 28: Django Forms

**How do Django Forms facilitate user input handling, and what are some key components of creating a form using the Django framework?**

Django Forms allows for the collection of a bunch of data in way that is simple to process. Any inputs can be checked for validity.

Declaring a form is much like a model, the field types are the same for valid displaying purposes.

To created, the forms library must be imported. Then, the fields of the form are declared.

Within the form class, the form cleaning and validation functions reside. This is where the data is checked if it fits certain parameters.

The VUT then needs to be updated.

There is also ModelForm, which, if the form is a simple data collect, is the easier way to go. It creates a form out of the model fields.

**Explain the purpose of Django Templates in web development and describe how template inheritance can be utilized to improve code reusability and maintainability.**

Templates are the epitome of dry code. By using templates, code can be reused in a simple fashion. I presume when stating inheritance, it means that templates themselves should also be reused. This makes sense, as just like the code within the template, the template itself can repurposed in the same way.

**Describe the function of Django Views in handling HTTP requests, and outline the differences between function-based views and class-based views.**

Django Views defines how to manage incoming HTTP requests, depending on the source of the request, the appropriate data is served up.

Class-based views inherit the as_view() method.

In summary, class-based views is a simpler way to go, for most instances. Howerver, it is harder to customize and extend. In those cases, functions-based views is better. Note though, functions-based can be repetative.

## Things I want to know more about

What makes class-based views so confusing and yet useful?
