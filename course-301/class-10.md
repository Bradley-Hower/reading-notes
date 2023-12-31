# *Course 301, Entry 10: In memory storage*

## Understanding the JavaScript Call Stack

**What is a ‘call’?**

A call is the running of a callback function.

**How many ‘calls’ can happen at once?**

Calls are synchronous, running one at a time in order.

**What does LIFO mean?**

LIFO stand for Last In First Out. It is in reference to how items are processed based on storage.

**Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.**

![Call Stack](https://github.com/Bradley-Hower/reading-notes/assets/139923955/ba75dad0-9762-46d3-84e3-a3a6fd3c7ce5)
![Call Stack Process](https://github.com/Bradley-Hower/reading-notes/assets/139923955/9ff2a712-6f7b-4d65-b1b3-304dbf9726f2)


![Event Loop](https://github.com/Bradley-Hower/reading-notes/assets/139923955/38095ca5-5b3d-450b-9da8-287557a4eb09)

How does this fit in with the Event Loop? The callstack is a JavaScript runtime component. The event queue contains JavaScript runtime.  

**What causes a Stack Overflow?**

A *Stack Overflow* occurs when a recursive function (loop) occurs without an exit. Once the stack memory allocations is exceeded, the stack error is thrown.

## JavaScript error messages

**What is a ‘reference error’?**

A variable is used but has not yet declared.

**What is a ‘syntax error’?**

An error in the syntax composition. Common syntax errors are missing commas, parenthesis or bracket notation.

**What is a ‘range error’?**

An invalid length has been entered. No negative lengths are allowed.

**What is a ‘type error’?**

The data type being used is not compatible with the place in which it is being used. This can also be due to a reference error, as the type error can precursor a reference error. This is because if a variable is undefined, there is no type.

**What is a breakpoint?**

hitBreakpoints are stopping points in a code execution which are hit if certain conditions are met.

**What does the word ‘debugger’ do in your code?**

"Debugger" sets a breakpoint in the code.

Image sources: https://stackoverflow.com/questions/21596172/what-function-gets-put-into-eventloop-in-nodejs-and-js

https://medium.com/swlh/in-depth-introduction-to-call-stack-in-javascript-a07b8513bcc3

## Things I want to know more about

Expanding further on the browser processes perhaps. I am not sure what is a good range of knowledge, as I know there is a lot going on.
