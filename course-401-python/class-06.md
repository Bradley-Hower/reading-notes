# *Course 401 Python, Entry 6: Ten Thousand Game 1*

## The Random Module

### randint()

Taking in two integers as a range, the randint function generates random numbers on call.

### random()

This function works in acting as providing a probability value, generating a value between zero and one.

### choice()

Selects a random element among a collection object, such as lists and tuples.

### choices()

Not to be confused with choice(), this function works to select two or more elements from a list, with replacement.

### sample()

Works to select two or more elements from a list, with replacement. Like choices(), but without replacement.

### shuffle()

Takes in a list and returns the elements in a shuffled order.

### randrange()

## Questions

Likeunto the choice function, however, selects specific intervals. Takes three values, start, stop, step. For example, inputs of 0, 100 and 20, produces one of the following, 0, 20, 40, 60, 80.

**How can the random module be utilized in Python to generate random numbers or make selections from a list, and what are some common functions available within the module?**

To generate a random number, randint() can be used. To select a random element from a list, choice() can be used, or choices() if more than one is to be selected.

Some common random functions are: randint(), random(), choice(), choices(), shuff(), and randrange(). All random functions are actually bound methods of a hidden instance of random(). State is shared.

**In the context of software development, what is risk analysis, and what are the key steps involved in conducting a risk analysis for a software project?**

Risk analysis is the act of identifying areas in the software production process that could lead to substantial loss. The key steps are forecasting unwanted situations, estimating the loss with said situation, what decisions are to be made regarding such risk and then, future preventative measures.

**What is test coverage and why is it an important (or potentially misleading) metric in software testing?**

Test coverage is used to identify untested parts of a project. Test coverage does not give feedback on how good a test is. Coverage of around 90% is good, the rest of the time should be spent on quality of testing. Another good gauge is that tests should not take a lot of time to change on code updates.

**What is Big O notation, and how is it used to describe the performance of an algorithm? Give an example of an everyday task (not software related) that demonstrates O(n) time complexity.**

Time complexity is basically how much time it takes to run an algorithm. This is highly dependent on the size of the data being processed and the total number of potential iterations. Space complexity is dependent mostly on the data structure of the data being processed and its size. Objects, for example, are much more data hungry than an integer. Big notation is a metric to measure this time and space complexity. Big O describes the type of data structure of an algorithm at worst-case scenario. An example of O(n) notation is sand in the hour glass. The more sand that is added the longer it will take and the more space it will require.

## Things I want to know more about

Why random() should not be used for cryptocurrency.
