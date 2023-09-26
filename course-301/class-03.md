# *Course 201, Entry 3: Passing Functions as Props*

## .map()

Using `.map()`, the entries in an array are returned.

### React

To run through an array and return the figures in React, the element being returned just needs to be contained within curly brackets.

Example:

```
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  {number}
);
```

Every list item needs a locally unique **key**. The keys is what allows the computer to track each item and make changes. IDs from the given dataset are a great way to create keys. When IDs are not available, index numbers also work. Using indexes is not ideal, as changes to datasets can entirely through off what is being referenced. In addition, there are performance issues associated with using index numbers as keys.

Avoid puting keys and values elsewhere. Keys and values should stay under the .map() call.

## Spread Operator

The spread operator effectively allows the coder to take the contents, of an arary for example, and apply it within other purposes.

Examples of uses:

+ **Attached to variables.** This allows for easy copying and repurposing of an array.

```
const arr = [1, 2, 3];
const arr2 = [...arr];
```

+ **Applied as an argument within a function.** This can be done once or multiple times within an assortment of arguments.

```
function myFunction(v, w, x, y, z) {}
const args = [0, 1];
myFunction(-1, ...args, 2, ...[3]);
```

+ **Used in a `new` instanciation.** This is a unique capability. The `.apply()` method, for example, can not do this.

```
const dateFields = [1970, 0, 1]; // 1 Jan 1970
const d = new Date(...dateFields);
```

+ **A much cleaner and easier way to splice in an array within another array.** Otherwise, methods such as `.push()`, `.slice()`, `.unshift()`, etc, would have to be used. Likewise to function arguments, spread can be used multiple times within an array. Similarly, contatonation can be done easily, allow for the combination of arrays.

```
const parts = ["shoulders", "knees"];
const lyrics = ["head", ...parts, "and", "toes"];
//  ["head", "shoulders", "knees", "and", "toes"]
```

```
let arr1 = [0, 1, 2];
const arr2 = [3, 4, 5];

// Append all items from arr2 onto arr1
arr1 = arr1.concat(arr2);
```

+ **Combining objects*.** The properies from multiple objects can be combined into one. Also, spread can be used to override the current properties of an object, as the last properties added in will replace any prior keys of the same name.

```
const obj1 = { foo: "bar", x: 42 };
const obj2 = { bar: "baz", y: 13 };

const mergedObj = { ...obj1, ...obj2 };
// { foo: "bar", x: 42, bar: "baz", y: 13 }
```

```
const obj1 = { foo: "bar", x: 42 };
const obj2 = { foo: "baz", y: 13 };

const mergedObj = { x: 41, ...obj1, ...obj2, y: 9 }; // { x: 42, foo: "baz", y: 9 }
```

+ **Conditionally adding to an array.** With a boolean, a variable can be added in. How keen! This can also be done with objects.

```
const isSummer = false;
const fruits = ["apple", "banana", ...(isSummer ? ["watermelon"] : [])];
// ['apple', 'banana']
```

```
const isSummer = false;
const fruits = {
  apple: 10,
  banana: 5,
  ...(isSummer ? { watermelon: 30 } : {}),
};
// { apple: 10, banana: 5 }
```

Note: "&&" can be used in place of "?" in the two above examples, as the conditional is a falsy. Once the conditional changes to true, the propery is added in this case.

### Limits

Spread can not mutate objects. `.asssign()` can, however. This means there the coder can't directly replace a property value.

## Passing Functions Between Components

The following Q&As are in reference to the following video: [https://www.youtube.com/watch?v=c05OL7XbwXU](https://www.youtube.com/watch?v=c05OL7XbwXU)

**In the video, what is the first step that the developer does to pass functions between components?**

In the video, the developer creates an arrow function, "Increment", at the App level which mirrors the state object. This function can then be used at the person level.

**In your own words, what does the increment function do?**

The increment function allows the correct property to be identified at the state level and the count therein to be incremented.

**How can you pass a method from a parent component into a child component?**

Passing a method from a parent to a child can done by using an arrow function. Inside is the object within angle brackets. Then, thereunder as a property, within curly brackets, "this.methodname". In this case, "this.increment". This moves in through props at the child constructor.

**How does the child component invoke a method that was passed to it from a parent component?**

This is accomplished using `this.props.parentfunctionname()` syntax. In this case, the element pushed through within the parenthesis was "this.prop.name".

## Things I want to know more about

What rest is in relation to spread.


<sub>Example code taken from [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax)</sub>

