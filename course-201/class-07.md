# *Course 201, Entry 7: Object-Oriented Programming, HTML Tables*

## Domain Modeling

A domain model creates a conceptual framework for a feature. This serves well when communicating between business folks and programming management.

1. When creating a model with multiple instances, create a single object which will hold a constructor function. This constructor function is what will hold properties.

2. Methods will then be created with each doing a singular task. Within these different methods, `this` can be used to access the object's properties and other methods.

3. Instances can then be created using the `new` keyword, followed by a call to the constructor function, all stored within a variable.

## Tables

Tables are great when implemented correctly. However, tables should not be used for layouts. The reasons are:

+ Poor accessibility for screen readers.
+ There ends up being a lot more code than necessary.
+ Table so easy to create with responsiveness to various screen sizes.

### Semantic Elements

Some table semantic elements include: 

+ `<th>` - Table header
+ `<td>` - Table data
+ `<tr>` - Table row
+ `<colspan>` - Number of columns
+ `<rowspan>` - Number of rows
+ `<colgroups>` - Holds the `<col>` elements
+ `<col />` - Allows for CSS formatting to columns

## Constructors

A constructor is a model-based object. It allows for multiple instances of instantiation to be set, running off of the same object. This allows for massive repurposing.

### this - Object Literal vs Constructor

In an object literal, `this` is used simply to refer to the object by name and pull properties or functions from there. In constructors, `this` serves the purpose of **initializing** a property. This allows a parameter to be pulled in and applied, creating properties from it.

### Prototypes

Prototypes are like subject matter experts for a department. These folks do one thing and they do it well. Anytime they need to be called on within the department, they can. This is **prototype**. Prototype allows us to call upon that method.

Inheritance is similar to saying, "Let me ask my co-worker".

## Things I want to know more about

How prototyping really works is still a bit confusing to me, although I know what it does.
