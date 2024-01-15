# *Course 401 Python, Entry 7: Ten Thousand 2*

## Scope

**Explain the concept of variable scope in Python and describe the difference between local and global scope. Provide an example illustrating the usage of both.**

Scope is what defines acces to parts of code in terms of its functionality. The order of scope in Python is defined by LEGB - Local, Enclosing (non-local), Global, and Built-in. Local scope is what is available within the defined parts of code, such as a loop, object, function, etc. Note, local scope is created a function call, not definition. Global scope is what is accessible to all parts of code.

**How do the global and nonlocal keywords work in Python, and in what situations might you use them?**

Global

By using the global statement, the scope can be modified from outside that scope. For example a counter at the global level could be modified in a local scope, such as a function. This is accomplished by stating the global keyword and then the variable of interest. Using these scope loopholes is generally seen as bad practice.

Global Example:

```
count = 1

  def somefunc():
    global count
    count = 3
```

Nonlocal

Similarly, nonlocal allows for escaping the nonlocal scope to modify outside thereof to the local level. The nonlocal statement can only be used at the other levels, unlike global.

Nonlocal Example:

```
def func():
  var = 100
  def adder():
    nonlocal var
    var += 100
  adder()
  print(var)
```

**In your own words, describe the purpose and importance of Big O notation in the context of algorithm analysis.**

The purpose of Big O notation is to illustrate the eventual outcomes, which will eventually grow faster and outpace anything else. Thus, the bigger the data set, the more important Big O is.

**Based on the Rolling Dice Example, explain how you would simulate a dice roll using Python. Describe how you would use code to calculate the probability of rolling a specific number (e.g., the probability of rolling a 6) over a large number of trials.**

To simulate rolling of dice, we could create a function which twice produces a random integer using `random.randint(1,6)``. The total of these two figures would be summed and then output to a dictionary for tabulation. Another function could then be created for the purpose of loops which then takes in the prior random dice roll function and then loops the same number as the desired of number of trials.

## Things I want to know more about

What are the use cases for scope modifiers?
