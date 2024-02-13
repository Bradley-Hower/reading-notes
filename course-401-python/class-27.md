# *Course 401 Python, Entry 27: Django Models

**Explain the purpose and basic structure of Django models. How do they help in creating and managing database schema in a Django application?**

Django models are Python objects used to define the structure of data stored. Via these models, associations across data can be had, whether it is one-to-one (OnToOneField), one to many (ForeignKey), or many to many (ManyToManyField). The number of fields of data can be defined.

The different field options are listed here: [https://docs.djangoproject.com/en/4.2/ref/models/fields/#field-options](https://docs.djangoproject.com/en/4.2/ref/models/fields/#field-options)

Models also consist of metadata and methods.

**Describe the primary features and functionality of the Django Admin interface. How can it be customized to suit the specific needs of a project?**

The admin application allows the user to easily update records within a database. The models used can be customized via import, each when thereafter being registered.

Via a superuser (an admin-type privilege) allows for full access to change a database.

Views:

- List Views - additional fields, filters, view options.
- Detail Views - fields, related fields, inline editing

ModelAdmin Class - Change how a model is displayed in admin interface

List Views configuration - customize the fields to display and how to display them

List filters - customize how data is filtered

**Briefly outline the key components and workflow of a Django application, as discussed in the Beginner’s Guide to Django. How do these components interact with each other to create a functional web application?**

Models - Database management and representation.

Template Engine - How data is managed and organized

Static files - CSS, JavaScript, assets, etc.

Testing - Important aspect. Every project should have automated testing. It improves quality.

Django Admin - a dashboard to view data

## Things I want to know more about

How to effectively organize it all.
