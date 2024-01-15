# *Course 401 Python, Entry 8: Ten Thousand 3*

**What is the basic syntax of Python list comprehension, and how does it differ from using a for loop to create a list? Provide an example of a list comprehension that squares the elements in a given list of integers.**

List comprehension is accomplished using the following syntax:

```
TheList=[1,2,3,4,5,6]
newList=[item**2 for item in TheList if item%2==0]
```

To write this same code otherwise is as follows:

```
TheList=[1,2,3,4,5,6]
newList= []
for item in TheList:
  if item%2==0:
    newList.append(item**2)
```

This is not only shorter, but significantly easier to read.

We can also pass items into a function:

```
newList=[double(item) for item in myList]
```

**What is a decorator in Python?**

A decorator in Python are function modifiers that work by wrapping the function.

**Explain the concept of decorators in Python. How do they work, and what are some common use cases for them? Provide an example of a simple decorator function from the reading.**

Decorators offers ways to modify a function. Here is a breakdown:

```
def my_decorator(func):
  def wrapper(*args, **kwargs):
      print("Something is happening before the function is called.")
      func(*args, **kwargs)
      print("Something is happening after the function is called.")
  return wrapper

@my_decorator
def say_whee(w):
  print("Whee!")
  print(w)
say_whee("woo")
```

The `@my_decorator` line, which uses pie syntax, is equivalent to `say_whee = my_decorator(say_whee)`. However, in the above, the arugment `"woo"` is passed in.

The function, say_whee(), is then passed into the my_decorator function. This is done without any parenthesis, as passing functions into a function go without. The funciton is then used in the inner function. In order for the argument to be passed through, the inner function, wrapper(), uses the wildcard syntax `*args, **kwargs`. This then allows the full expression of say_whee().

So why decorators? In summary, it allows for plugin capabilities into many different functions with the simple pie syntax line. Moreover, multiple other functions can still be plugged into the original target function. It offers quick modularity, flexibility and reusability.

## Things I want to know more about

I think I understand decorators well. I Just need more exposure.
