# *Course 401 Python, Entry 2: Introduction to React and Components*

## In Tests We Trust - Test-driven development (TDD) with Python

Construct the unit test folder in a way to mirror the working code - module for module. And be descriptive when naming test.

Then test it:

+ Arrange - Organize data for input.
+ Act - Execute code.
+ Assert - Find out if the output was as expected

The three-step process to feature development:

1. Write code which will probably fail.
2. Fix the code so it works.
3. Refactor to make it cleaner and more readable.

Write the method for expected outcome.

Write the method for other expected scenerios.

### What are the key principles of Test-Driven Development (TDD) in Python, and how do they contribute to the overall quality of code?

The key principles are to test the code directly via cases, rather than chasing down bugs everywhere afterwards. The process is much faster.

### Explain the purpose of the if __name__ == '__main__': statement in Python scripts. What are some use cases for including this conditional in your code?

This conditional in the code allows for more flexibility. It allows for either reusable modules or standalone programs. Meaning, you can specialize the use purpose without having to write another program.

### Describe the concept of recursion in Python

Recursion works by a function calling a copy of itself under modified conditions. There needs to be a termination case (base case), and the function needs to work towards the either equily or less complex status of the original. Recusion uses a LIFO structure. When there is not enough space or the base case is not reach/not defined, a stack overflow will occur.

### What is the difference between Python modules and packages? Explain how to create, import, and use them in your Python programs.

Modules are typically written in Python, while packages are a collection of modules. Packages can be created using the OS file system.

For importing modules, you just need to enter ```import <module_name>``` at the top of your python file. For importing a specific object, ```from <module_name> import <name(s)>```. To import a specific module from a package, ```from pkg.mod3 import *```

Functions can be assigned ```from pkg.sub_pkg2.mod4 import qux as grault```.

Otherwise, it can just be called using full notation ```pkg.sub_pkg1.mod1.foo()```.

## Things I want to know more about

How to structure the tests.
