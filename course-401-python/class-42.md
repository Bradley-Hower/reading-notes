# *Course 401 Python, Entry 42: Pythonisms

**What are dunder methods in Python, and how do they allow for the customization of built-in behavior in classes? Provide an example of a common dunder method and its purpose.**

Dunder methods allow a particular built-in to be used with in a class. A common one would be `__len__`, which returns the length of an object.

Some other ones include the ability to:

- Initialize new objects
- Object representation
- Enable iteration
- Operator overloading (comparison)
- Operator overloading (addition)
- Method invocation
- Context manager support (with statement)

**Explain the concept of an iterator in Python. How do you create a custom iterator using the iter() and next() methods, and why are they important for enabling iteration in a class?**

In Python, to create an iterator, the `__iter__()` `__next__()` dunder methods must be used. These effectively identify the source and the next to be pulled.

**What is a generator in Python, and how does it differ from a regular function? Illustrate your answer with an example of a generator function using the ‘yield’ keyword.**

Generators allow for a more simplified version of a regular loop. It just beautifies it to smaller code. 

```
def firstn(n):
  num = 0
  while num < n:
    yield num
    num += 1

sum_of_first_n = sum(firstn(1000000))
```

**Define decorators in Python and explain their primary use case. How can you create and apply a custom decorator to a function or method? Provide a simple example to demonstrate this concept.**

Decorators add modularity with functions. It allows for inputs to be modified. This allows for repurposing.

## Things I want to know more about

Everything listed here.
