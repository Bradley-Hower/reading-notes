# *Course 201, Entry 10: Debugging*

What a pain bugs can be. And like the real life bugs, programming bugs can irritate and make it hard to sleep. Thus, having a good process to remove these types of bugs can alleviate a lot of pain.

## Troubleshooting JavaScript

There are two main types of errors. Syntax Errors and Logic Errors.

**Syntax Errors**: an error resulting from a fundamental improper construction of the code. This will result in error codes tripping. Compared to logic errors, these are generally easier to fix. With a console in hand to indicate where the error is occurring, it becomes easier to isolate. Spelling, capitalization, and punctuation all count. These three are the common source of problems, as usually, a coder won't be so far off on syntax.

**Logic Errors**: the code is technically legal, but the results are not as desired. These are difficult. One needs to typically make efforts to review code thoroughly to isolate the code that was written incorrectly. In addition, if logic errors exist in tandem with syntax errors, resolving the error will take multiple rounds. Logic errors can be deceptive. Run a program multiple times with multiple inputs to see if the program is actually working correctly.

### Experience with Errors

Among these errors, I have probably experienced them all at this point. Syntax errors resulting from missing a bracket, not declaring a variable correctly via "const" or "let", and other similar construction errors. These are generally easy to fix. The console log makes it easy to discover.

The logic errors are harder. I have to really understand what each code does in the program. And I need to be sure that I constructed it correctly. This one has no lazy way out. I have to step by step go through how the code is running and test it in my mind to see if it makes sense. I had a big logic error in this last assignment that went undetected from a previous lab. The code worked perfectly. Then, when I needed to remove that table row in the next lab, I had unexpected results. I checked multiple times to see if the code I was inputting was correct. I then decided to eat dinner and think about the problem. In thinking about it, I concluded that the code to delete the line must be correct. Perhaps I should look at the to-be-deleted code's creation to see if it was done correctly. Sure enough. Bad construction.

### Moving Forward

In debugging my code I will work harder to discover logic errors. These take more effort and are not the easier low-hanging fruit that are syntax errors. However, I spend too much time on the ground and must climb.

## JavaScript Debugger

A debugger tool allows one to isolate a problem. It is a diagnostic tool that allows the coder to test and play with the lines of code to see what happens. By doing this in isolation with the feedback prompts that the debugger provides, the coder can isolate the problem more easily. 

### Breakpoint

**Breakpoints** are set pause points set upon the code. The breakpoint sets the bounds of view for analysis.

### Call Stack

The **call stack** provides a readout of what code ran up to the breakpoint. 

## Things I want to know more about

How to best use the debugger tools for the the most effective outcomes.