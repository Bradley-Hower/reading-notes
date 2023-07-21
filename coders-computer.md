## *Class 102, Entry 3: Coder's Computer*

The **coder's computer** is ultimately the repository for all the coder's tools. And while the tools can vary, there are two major ones that all coders use,  a text editor and Terminal. To get going, one must be well-equipped. Obviously, you are here to do so. Let's not delay!

## Text Editor

One of the key tools for the coder is the text editor. As with any profession, one can only be as good as the tools at hand. Therefore, it is important to know what to look for in a text editor. However, keep in mind a text editor is a personal choice. Ultimately, the choice depends on what the coder likes best. 

#### Text Editor vs IDE 

An IDE (Integrated Development Environment) is a text editor, and more. IDEs are a combination of various software, such as compilers, debuggers, built-in Terminals, etc. Purists would say text editors are simply for editing text, nothing more. It can be hard to draw an arbitrary line.

While text editors can be fancy, sometimes simple is good. Minimalism is a beautiful thing. And every computer comes with a text editor. For Windows, it's Notepad. On Mac, Text Edit. And while these editors may be lacking, they can also be expanded to hold more powers through modified versions. Best to skip the dedicated word processors though. Formatting, styling, and autocorrections in a word processor, such as Microsoft Word or Pages, will be of no help. Any formatting will not make it into the actual code. Actually, you will probably become irate trying to use a word processor for coding. The best advice is to skip word processors.

Okay. Sounds good. Perhaps you want more out of your text editor?

## Important Features One Should Look for in a Text Editor

1. ### Code Completion
   
   **Code completion** is arguably the most useful feature. When initially typing, a good code completion software will pull up a list of predictive suggestions to allow for easy completion. This saves countless hours of searching for the correct characters and saves a ton of effort later by helping to prevent typing errors. One very popular code completion extension is Emmet. Emmet works to assist the coder to quickly complete HTML and CSS code with ease. 

3. ### Syntax Highlighting

   Secondly, and arguably a close one, is **syntax highlighting**. Syntax highlighting is what gives color to one's code, and not haphazardly. Coloration is added intelligently and automatically by coloring different parts of code differently. This massively improves the readability, thus allowing the coder to quickly identify where to make changes throughout the code at hand. 

4. ### Extensions

   The world of coding offers a plethora of cures for your aching needs. **Extensions** are like magic potions when it comes to features. Extensions can complete what might otherwise be lacking in the coder's text editor environment. Chances are, if you feel it is a strong need, someone else has already agreed with you and built it out. 

5. ### Themes

   While perhaps not essential, **themes** are a nice feature that adds some life to one's software. It allows a coder to customize and give personality. Moreover, themes that are easier for the coder to read and which produce less eye strain are arguably of great value to many.
   
___

### Choice Text Editors

A strong list of editors can be found on [Wikipedia](https://en.wikipedia.org/wiki/List_of_text_editors).

For a more curated 2023 list, [TechRadar](https://www.techradar.com/best/best-text-editors) has some great candidates.

## Terminal

The Terminal, if you don't know, is the all-powerful portal. It is the tablet by which we can act as gods in the computer world. While everyone else is playing in a GUI sandbox, those that know how to use Terminal are playing outside. Here in this article will be an intro to some concepts along with some examples. 

Firstly though, Terminal is not a Shell, a Kernal, nor is it even Command Prompt (Command Prompt opens Console, which is the Windows OS equivalent to Terminal). Shell interprets what is input at the Terminal, and the Kernal interfaces this via Shell software with the OS and hardware drivers.

Terminal > Shell > Kernal > Hardware

### Vocabulary

**Prompt** - When the system is awaiting input from the user, this is known as the prompt. The first line, along with the text, first presented when initiating a Terminal session, is the primo example of a prompt. The system is *prompting* or informing you to know that a command can be entered. If the Terminal is blank or other text is continuously running, then the prompt is not present. 

**Command** - Instructions to the computer program to do a said thing. Generally speaking, it is a directive. 

**Argument** - Input expressions, which are to be passed to a function or procedure. 

**Option** - Options are also arguments. Modifiers to a command. Typically precursed with a `-`. 

**Location** - Intended directory for said command. 

**Relative Path** - Specifying which directory to work under, relative to the current directory. Paths are hierarchical. The root directory (the highest directory) is represented by `/`. Child directories and lower can be specified, each level separated by a `/`. To reference a parent directory, `../`. A single `.` just refers to the current directory. The `/` in this context is equivalent to "folder" (optional if no subdirectory is intended). Parent directories do not need to be specified by name, as there can only be one. To go one level above the parent, `../../`, etc. To refer to the home directory, use `~`. If you ever just want to go home, `~`. 

**Absolute Path** - Location specified relative to root. 

Note, options are also arguments. Also, Terminal is case-sensitive. 

### Introductory Terminal Commands

`pwd` - Print Working Directory. Outputs current folder operating under.

`ls` - List. Prints directories under the current directory, if not otherwise specified. To produce an orderly column, use the option `-l`. To list hidden files, `-a`. (Hidden files normally begin with a `.`.  Note, you will see a `.` file and a `..` file when showing hidden files. These are the current and parent paths, respectively. Paths are actually files in Linux it turns out. 

`cd` - Change Directory. Changes directory to the home directory, unless a location is specified.

`mkdir` - Make a new directory. That which is input afterward will be the name of the new folder. 

`touch` - Creates a new file. That which is input afterward will be the name of the new file. The file extension should also be entered immediately following the file name, such as `.pdf`, `.png`,  etc. 

`file` - Lists information about a file. 

### Examples:

What is happening in the following commands?

1. `cd projects`
2. `mkdir new-project`
3. `touch new-project/newfile.md`
4. `cd ..`
5. `ls projects/new-project`

Let's break it down.
1. Under the current directory, the subdirectory "projects" is being selected to become the current directory in use. The code cd is a *command* and represents the current directory selection. And projects is the *argument*, representing the directory being selected. Commands and arguments are always separated by spaces. If ever the folder or file has a space in it, wrap it in ' on each side. Otherwise, the space will confuse the system. Another way is to use \ before the space, thus nullifying it.
2. Within the current directory, a new subdirectory is being created, named, "new-project". The code `mkdir` represents creating the new directory, and `new-project` represents the title of the directory being created. 
3. A new file is being created. The code `touch` informs the system to create a new file, while `new-project/newfile.md` specifies the location and new file name, `new-project/` being the prior, and `newfile.md` being the latter. 
4. From the current directory, the current directory is being changed to the directory superior to the current directory. In other words, the current directory is being changed to the directory which is currently the parent directory. The code `..` represents one folder up. 
5. With this command, the list of folders within a directory is given as an output. The code `ls` represents the list command, while the `projects/new-project` represents the folder in which to list all the subfolders that exist thereunder. 
