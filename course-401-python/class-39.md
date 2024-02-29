# *Course 401 Python, Entry 39: React 3

**What is React Context, and how does it help in managing state and data sharing in a React application?**

## React Context

React Context - Move data without using props. This is great for anything that would normally be stored on local cache, such as location, dark mode, login authentication.

React Context helps to avoid props drilling.

### Steps for React Context

1. Use the `createContext` method to create a context.
2. Wrap the context tags around the component tree.
3. Use the value prop to add data.
4. Use the context consumer to read the data.

Example

```
import React from 'react';

export const UserContext = React.createContext();

export default function App() {
  return (
    <UserContext.Provider value="Reed">
      <User />
    </UserContext.Provider>
  )
}

function User() {
  return (
    <UserContext.Consumer>
      {value => <h1>{value}</h1>} 
      {/* prints: Reed */}
    </UserContext.Consumer>
  )
}
```

**Explain the useContext Hook and how it can be used to access data from a React Context within a functional component.**

Another options is to use contextHook. This is a different way which can also access the useContext.

```
function User() {
  const value = React.useContext(UserContext);  
    
  return <h1>{value}</h1>;
}
```

### Redux

Redux is great if updating is needed, otherwise context is better.

**Describe the purpose of Next.js, and provide an example from the Vercel Next.js Examples reading on how it can be used to build a scalable web application.**

https://github.com/vercel/next.js/tree/canary/examples/headers

Honestly, I don't know what the point is. More of the same if you ask me. I understand it allows for faster rendering due to server-side rendering, but with modern hardware, I don't see this as being an issue. Perhaps the purpose is data control?

## Things I want to know more about

More about trade-offs between redux, context, props, etc.
