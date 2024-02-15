# *Course 401 Python, Entry 29: Django Custom User

**What are the key benefits of using a Django Custom User Model, and how does it differ from the default Django User Model?**

It allows for customization later, even if the need doesn't currently exist. This is mostly due to dependency issues, which are a giant hurdle if trying to swap over. Note, there are still required fields that must be defined, even with a custom user model. 

Some added benefits:

- Authentication backends
- Custom permissions
- Custom user statuses (active, inactive, etc.)
- Anonymous users

**Explain the process of creating and implementing a Custom User Model in Django, including the necessary changes to settings.py and the required model fields.**

1. Create the custom user model before migrating.
2. Add the accounts app in INSTALLED_APPS and `AUTH_USER_MODEL = "accounts.CustomUser"` to the bottom within settings.
3. Create a custom user model within models.py.
4. Update forms.
5. Update admin.
6. Now `makemigrations` and `migrate`

**What is DjangoX and how does it complement or extend the functionality of Django? Provide an example use case for incorporating DjangoX in a project.**

DjangoX greatly improves the user creation process. In its update to the user model, it elimintes the username field and allows login via other authentication services (google, meta, etc.).

## Things I want to know more about

I want to familiarize myself more with the custom user model fields.
