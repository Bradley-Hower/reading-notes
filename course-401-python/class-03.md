# *Course 401 Python, Entry 3: File IO & Exceptions*

## A File

Parts of a file:

+ Header - Metadata regarding file contents (name, type, size...).
+ Data - Core written code.
+ End of FIle (EOF) - Special character marking end of file.

## Line Endings

Windows uses the CR+LF characters to indicate a new line.

Unix based systems use the LF character.

**Windows Example:**

```
Pug\r\n
Jack Russell Terrier\r\n
```

**Unix Example:**

```
Pug\r
\n
```

This difference in structure can cause issues when iterating over each line.

## Encoding

Parsing with the wrong encoding can cause issues. However, ASCII is actually a subset of Unicode (UTF-8). Thus, just use Unicode.

## Opening Files in Python

Use the open() function with a path to the file. The file will be returned as an object.

ALWAYS make sure a file is propertly closed. Otherwise, you can overload your system resources and expose the file to data loss or altered permissions.

The two ways to ensure a file is closed is to use the try-finally block:

```
reader = open('dog_breeds.txt')
try:
    # Further file processing goes here
finally:
    reader.close()
```

Or the context managers via the with statement:

```
with open('dog_breeds.txt', 'r') as reader:
    # Further file processing goes here
```

The with statement takes care of closing a file, even in case of errors.

Modes to be used with *with*

+ **r**	- Read (default)
+ **w**	- Write
+ **rb** or **wb** - Binary mode (read/write using byte data)

Use .read to specify the size of content to read. Also, use .tell to give the current position. Together these can be used to toggle through a file. The .seek method can be used for writing but selecting where to start the next write. Note, seek will overwrite.

### Read

We have a couple of ways to read files:

+ .read(): reads the entire file.
+ .readline(size=n): reads n characters from the line. If n=0,-1 or empty, reads entire line. Useful when you only want to iterate over one line at a time.
+ .readlines(): readsthe remaining lines from the file and returns them as a list.

### Writing

+ .write(string): This writes the string to the file.
+ .writelines(seq): This writes the sequence to the file. No line endings are appended to each sequence item. It’s up to you to add the appropriate line ending(s).

## File Objects

There are three types of file objects, **text files**, **buffered binary files**, and **raw binary files**.

### Text Files

```
>>> file = open('dog_breeds.txt')
>>> type(file)
<class '_io.TextIOWrapper'>
```

Buffered Binary Files

```
>>> file = open('dog_breeds.txt', 'rb')
>>> type(file)
<class '_io.BufferedReader'>
>>> file = open('dog_breeds.txt', 'wb')
>>> type(file)
<class '_io.BufferedWriter'>
```

Raw Files

```
>>> file = open('dog_breeds.txt', 'rb', buffering=0)
>>> type(file)
<class '_io.FileIO'>

```

## Exceptions versus Syntax Errors

Syntax errors are detected syntactically errors by the parser. Exceptions occur when, at some level, inputs are off. Note, exception erros should ideally be specific. This way, the type of error is not cloaked by blanket statement. Also, errors are received as a one-and-done. The only way to know if there are more errors is to fix the prior.

Custome errors can be built and are triggered with the `raise` call statement.

**What is the purpose of the ‘with’ statement when opening a file in Python, and how does it help manage resources while reading and writing files?**

The with statement allows for the use of the context managers. The context managers handle the setup and teardown of external resources when performing operations. WIthout this management, a issue known as memory leaks can occur. This is due to a lack of closing down a prior session. The critical teardown steps include closing a file, releasing a lock and closing a network connection.

**Explain the difference between the ‘read()’ and ‘readline()’ methods for file objects in Python. Provide examples of when to use each method.**

The .readline() method pulls in data per line. If no size is set, then the entire line is pulled. The .read() method is within the context of the entire file, pulling in all data if no size is set. If called in repetition, each of these methods process their calls in succession.

**Briefly describe the concept of exception handling in Python. How can the ‘try’, ‘except’, and ‘finally’ blocks be used to handle exceptions and ensure proper execution of code? Provide a simple example.**

The 'try' block is the first block to be given a go. If it doesn't work, however, and there is an exception error, the 'except' block runs. If neither the try, nor the except block trigger due to prior conditions not being met and no errors respectively, then the 'else' block will run. The 'finally' block will run after all the priors. The finally block will always be executed.

Example:

```
try:
    linux_interaction()
except AssertionError as error:
    print(error)
else:
    try:
        with open('file.log') as file:
            read_data = file.read()
    except FileNotFoundError as fnf_error:
        print(fnf_error)
finally:
    print('Cleaning up, irrespective of any exceptions.')
```

In the above example, the system will try to run the linux function. Perhaps it can not for some reason unrealated to the OS. In this case, the else block will try to run. Assuming it was succesful, or maybe it wasn't, regardless, the finally block will run thereafter.

AssertionError

## Things I want to know more about

More details of what a file is composed of. Perhaps just more popular file types, such as images and videos like WEBP and WEBM formats. Perhaps this should be studied only as needed. Also, what kind of magic can be done in byte mode?
