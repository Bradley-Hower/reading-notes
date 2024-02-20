# *Course 401 Python, Entry 32: Permissions & Postgresql

**What are the key components and purpose of Django Rest Framework (DRF) permissions, and how do they help in securing an API?**

- Permissions are used to determine if user should be granted or denied access to given assets within the API.
- Authentication is determined before running any other component.
- Permission can be set at the object level.
- Permission can be set a the views level, per view.

The finite ability to set permissions allows for any component to be locked down in any regard to the CRUD method used.

Permission statuses:

- AllowAny - alll access everywhere on a user basis, regardless of authentication.
- IsAuthenticated - Access allowed.
- IsAdminUser - Special admin permissions
- IsAuthenticatedOrReadOnly - Similar to IsAuthenticated, but gives readonly access to those without authentication.
- DjangoModelPermissions - Sets CRUD permission per model.

**In SQL, what is the purpose of the SELECT statement, and how would you use it to retrieve all columns from a table called ‘employees’?**

The purpose of "SELECT" is used to querey a database. To select all from a said table, the following line would work:

```
SELECT * FROM employees;
```

**Can you explain the role of DRF Generic Views and provide examples of their usage in building a RESTful API?**

The purpose of generic views is to abstraction basis for other views.

An example from Django REST framework:

```
from django.contrib.auth.models import User
from myapp.serializers import UserSerializer
from rest_framework import generics
from rest_framework.permissions import IsAdminUser

class UserList(generics.ListCreateAPIView):
    queryset = User.objects.all()
    serializer_class = UserSerializer
    permission_classes = [IsAdminUser]

    def list(self, request):
    # Note the use of `get_queryset()` instead of `self.queryset`
    queryset = self.get_queryset()
    serializer = UserSerializer(queryset, many=True)
    return Response(serializer.data)
```

## Things I want to know more about

Easy ways to set permission for types of users.
