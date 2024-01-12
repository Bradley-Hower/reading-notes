# *Course 401 Python, Entry 4: Object Oriented Programming*

## Objects

Objects are composed of variables and functions in one package. The variables and functions found in objects come from classes.

The `sys` module provides functions and variables which are used in connection with the Python runtime environment. One attribute of `sys` is `path`.

Everything in Python is an object. While not everything hass attributes or methods or are sub-classable, everything is an object in the sense that it can be assigned to a variable or passed as an argument to a function.

Classes allow for bundling. New instances can be created of other objects. Every class can have an attribute attached to state, with mothods for defining the state. Any derived classes can override methods of its base class or classes. Methods can call the method of a base class by the same name. Classes are created at runtime and can further be modified thereafter.

Class objects support two kinds of operations:

+ Attribute references
+ Instantiation

The attribute, `__doc__`, is a special attribute which returns the docstring.

Assigning a variable to a function call is an instantiation.

For example:

> `someobject = TheClass()`

After assigning the object, accessing variables can be done via dot notation, `someobject.variable`. Note, these can be assigned to other variables and are not bound.

Similarly, a function can be accessed, `someobject.function()`.

There are classes, superclasses, and subclasses. When passing in a calss, the superclass is typically passed into a class as a parameter.

Another way to interact with a superclass, other than by name, is to use `super().`.

### init()

The `__init__()` is a special function, called upon class initiation and used for assignments. It is used to define the initial state.

There are more "magic methods" similar to `__init__`, these are just more built-in methods which we are able to pre-load into a class and define its use.

https://nitesh-yadav.medium.com/dunder-methods-in-python-really-crazy-functions-3455ecb6472d


## Fixtures

Fixtures provide a baseline dataset to run a test. They are activated by declaring their use from a test function, modules, classes or whole project. Fixtures are modular and scalable. They can also be passed as parameters To run a fixture from multiple test files, move it to `conftest.py`, no need to import. Order of operations by pytest is test classes, test modules, conftest.py, and then plugins.

The `yield` keywords is specific to fixtures, used to execute teardown code.

```
# conftest.py
import pytest

@pytest.fixture  # This is a decorator... more about those later.
def my_fixture(scope='module'):
    # I can do a thing or 10 here to set up my test data
    some_value = 50
    return some_value
```
```
# my_test.py
def test_a_thing(my_fixture):
    # Passing the fixture in as a parameter to the test allows us to immediately run assertions on that expected return value
    assert my_fixture == 50
```

### Fixture Scope

+ session: This will run once for the complete pytest session; i.e. all of your test files.
+ module: This is similar to function scope, but will rather run once for the whole module.
+ class: This will run once for each test class that the fixture is passed into. We won't use this one for a while.
+ function (default): This will run once for each tests that the fixture is passed into.

**What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?**

Objects are iterations of classes. Classes are used to create the objects by utilizing the variables and functions therein.

**Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?**

Per realpython.com, "A iterations function is a function defined in terms of itself via self-referential expressions."

The idea is that the function is a self-calling, iterative function which continues running a recursive case until some preset condition (base case). Some example problems are the Tower of Hanoi.

The best practices in writing recursive function is to avoid repeating code, as the nature of recursive data structures does not require it. Secondly, is to use caching. Cache will vastly speed up the processing time.

**What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project.**

The purpose of pytest fixtures is to provide functions that will be used many times for the purposes of testing other functions. They allow for consistent context to be provided, such as a dataset.

Code coverage works to see the breadth of values being used in any given program. Meaning, you can see the holes in what should work, and might not be.

By using pytest fixtures and code coverage together, testing can systematized to good degree.

## Things I want to know more about

How to properly implement figures for maximum effectiveness.
