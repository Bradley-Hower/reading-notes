# *Course 401 Python, Entry 4: Object Oriented Programming*

## Objects

Objects are composed of variables and functions in one package. The variables and functions found in objects come from classes.

To assign an object, use the following syntax, `someobject = TheClass()`

After assigning the object, accessing variables can be done via dot notation, `someobject.variable`. Note, these can be assigned to other variables and are not bound.

Similarly, a function can be accessed, `someobject.function()`.

### init()

The `__init__()` is a special function, called upon class initiation and used for assignments.

**What are the key differences between classes and objects in Python, and how are they used to create and manage instances of a class?**

Objects are itirations of classes. Classes are used to create the objects by utilizing the variables and functions therein.

**Explain the concept of recursion and provide an example of how it can be used to solve a problem in Python. What are some best practices to follow when implementing a recursive function?**

Per realpython.com, "A recursive function is a function defined in terms of itself via self-referential expressions."

The idea is that the function is a self-calling, iterative function which continues running a rescursive case until some pre-set condition (base case). Some example problems are the Tower of Hanoi.

The best practices in writing recurssive function is to avoid repeating code, as the nature of recurssive data structures does not require it. Secondly, is to use caching. Cache will vastly speed up the processing time.

**What is the purpose of pytest fixtures and code coverage in testing Python code? Explain how they can be used together to improve the quality and maintainability of a project.**

The purpose of pytest fixtures is to provide functions that will be used many times for the purposes of testing other functions. They allow for consistent context to be provided, such as a dataset.

Code coverage works to see the breadth of values being used in any given program. Meaning, you can see the holes in what should work, and might not be.

By using pytest fixtures and code coverage together, testing can systematized to good degree.
