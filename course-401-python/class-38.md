# *Course 401 Python, Entry 38: React 2

**How does lifting state up in a React application help with managing data flow and what are the benefits of using this approach?**

https://legacy.reactjs.org/docs/lifting-state-up.html

Lifting state allows for two child components to be in sync with each other. In this way, the data is simultaneously transferred, which allows for a proper desired outcome. Rather than each being handled independently, and introducing the potential for a bunch of errors and synching issues, they are handled together in one parent state component, thus offering a single source of truth.

**Explain the concept of conditional rendering in React and provide an example of how to implement it in a component.**

Conditional rendering utilizes a flavor of if statements to conditionally render out some piece of code. What it does if the statement evaluates as False depends on the technique used.

The most flexible option is:

```
function Item({ name, isPacked }) {
  let itemContent = name;
  if (isPacked) {
    itemContent = (
      <del>
        {name + " ✔"}
      </del>
    );
  }
  return (
    <li className="item">
      {itemContent}
    </li>
  );
}
```

But there is also the "&&" statement method. Note, nothing will render if the first part is False. 

```
return (
  <li className="item">
    {name} {isPacked && '✔'}
  </li>
);
```
The other options is using a ternary:

```
return (
  <li className="item">
    {isPacked ? name + ' ✔' : name}
  </li>
);
```


**What are the main principles behind “Thinking in React” and how do they guide the process of designing and building a React application?**

1. Divide the data into components and hierarchies. Keep in mind the ease of programming, adding CSS, and the overall design appearance.
2. Keep it static, at first. There are lots of moving parts potentially. Best to get the wireframe componnents in first and then fill it in. This allows for reusability to be identified earlier and thus avoids a lot of problems and wasted code.
3. Add minimal state. Do what is essential for things to function, then later add anything else.
4. Identify where this state should be fed. Consider what is being rendered and hierarchy. Also, consider that this state might require its own component.
5. Reverse data flow. Often times, data needs to flow both ways between components. Be sure this is implemented where needed.

## Things I want to know more about

More about two-way binding.
