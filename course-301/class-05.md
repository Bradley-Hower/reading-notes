# *Course 301, Entry 5: Puting it all together*

## React

**What is the single responsibility principle and how does it apply to components?**

The Single Responsibility Principle is the idea that a function should only be built for one purpose. Once the function goes beyond that, it should be split. Applying this to componenents, components likewise should be built for one purpose.

**What does it mean to build a ‘static’ version of your application?**

A static version of an application is the application built out, minus any state storage.

**Once you have a static application, what do you need to add?**

The next thing to add is state.

**What are the three questions you can ask to determine if something is state?**

The three questions to ask are:

+ Does the piece of data remain unchanged over time? If so, it isn’t state.
+ Is it passed in from a parent via props? If so, it isn’t state.
+ Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!

**How can you identify where state needs to live?**

After identifying all the components that use state, state should be added according to the nearest common ancestor.

## Higher-order functions

**What is a “higher-order function”?**

Higher-order functions are functions that operate on other functions. This is done using another function as an argument or returning a function.

**Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?**

```function greaterThan(n) {
  return m => m > n;
}
let greaterThan10 = greaterThan(10);
console.log(greaterThan10(11));
// → true
```

Line two is a setup for another function. In this example, after 10 is inserted in place of n', the expression then is primed for another figure to be entered, taking the place of m'. This arrow function 'm => m > n;', is then used in the next iteration.

**Explain how either map or reduce operates, with regards to higher-order functions.**

Map works by taking in another function and applying it to every element in an array.

## Things I want to know more about

When is it better to use higher-order functions vs multiple other functions? When is the line for single responsibility principle with regards to higher-order functions?
