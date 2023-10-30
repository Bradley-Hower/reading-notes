# *Course 301, Entry 9: Functional Programming*

## Functional Programming Concepts

**What is functional programming?**

Functional programming is programming with a focus on functions. The concept is that the functions are trees of expressions for mapping values. This means not changing state and mutating data.

**What is a pure function and how do we know if something is a pure function?**

A pure funciton is a function that is repeatable. In otherwords, the same parameters will result in the same output, every time.

**What are the benefits of a pure function?**

The benefits of pure functions is predictable programming. This predictability makes testing much easier as a result.

**What is immutability?**

Immutability is being impervious to chanage.

**What is Referential transparency?**

Referential transparency is the combination of pure funcitons and immutible data.

>Pure Functions + Immutible Data = Referential Transperency

## Modules and require()

**What is a module?**

A module is an exportable function.

**What does the word ‘require’ do?**

"Require" pulls in the specified module into another file.

**How do we bring another module into the file the we are working in?**

To bring a module in the following syntax is used:

`const somemodule = require('./somefile');`

**What do we have to do to make a module available?**

To make this module available, it must be exported in the specified module file. 

`module.exports = somemodule;`

## Things I want to know more about

In what contexts is referential transparency considered standard? Is the goal to always use when possible?
