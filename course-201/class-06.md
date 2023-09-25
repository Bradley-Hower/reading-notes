# *Course 201, Entry 6: Problem Domain, Objects, and the DOM*

## Introduction to Objects

In JavaScript there are **objects**. What is an object?

An object is much like a tray of driver's licenses. This tray is an **object**. Within the tray you can pull a driver's license, an **object member**. On the driver's license, we can find detailed value attached aspects - the name, date of birth, expiration, etc., these are **properties**. Lastly, there can be capabilities attached to this such as semi-truck endorsements or motorcycle endorsements, these are **methods**. Functions are very much functions within a function. Essentially, an object is a container for data pairs and/or functions. Thus, a property itself can be an object. In the analogy, the driver's birth date can be an object property for the properties of month, day, and year.

### Dot Notation

**Dot notation** consists of the object name for the **namespace**, a dot, and then the item to be accessed (property, method, or another object).

Example:

```
driver.name;
driver.semi-truck_driving();
```

### Object Literals

What are some advantages of creating object literals?

Object literals are great for writing out one object. The definitions are fully descriptive, referring to names within the object. However, they are bad for scaling.

### Objects vs Arrays

Like arrays, brackets can be used instead of dot notation.

Example:

```
driver["semi-truck_driving()"];
driver["date of birth"]["month"]
```

These are very similar to arrays (sometimes called associative arrays), but with bracket notation for objects, the name is used instead of the index number. Strings to values rather than numbers to values. Dot notation is preferred though as it is easier to read.

### Bracket Notation

Note, it is not possible to access properties for an object that is held within variable parentheses. Bracket notation must be used.

Example:

```
funtion driverproperty_pull(["date of birth"]){
console.log(driver["date of birth"]);
}
```

Moreover, adding a property to an object using a variable can only be done using bracket notation.

### This

Evaluate the code below. What does the term "this" refer to and what is the advantage of using "this"?


```
const dog = {
  name: 'Spot',
  age: 2,
  color: 'white with black spots',
  humanAge: function (){
    console.log(`${this.name} is ${this.age*7} in human years`);
  }
}
```

The "this refers to the name of the object in which the code is being written, in this case, "dog". It allows for reference to the object without writing out the name of the object. Very useful scaling. Constructors can then be built to create objects from an object definition. By convention, constructors start with a capital letter.




## Introduction to The DOM

DOM (Document Object Model) is the representation of a web page as nodes and objects. Setting the web page code as objects allows programs to interact with it. DOM is not a programming language, but an interface. It functions as a Web API.

### DOM and Java Script

Being that DOM can be interfaced with, JavaScript scripting can modify a page. An example of this is via the `querySelectorAll` method. JavaScript, while it can interact with the DOM, it is not its only area of functionality. The DOM is independent of JavaScript. And other languages, such as Python, can also interact with it. To access the DOM, the `<script>` tags are used within an HTML document.

## Things I want to know more about

How JavaScript can be used to interact with JavaScript
