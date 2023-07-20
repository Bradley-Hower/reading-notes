## *Class 102, Entry 3: Coder's Computer*

The **coder's computer** is ulimately the repository for all the coder's tools. And while the tools can vary, there are two major ones that all coders use. The text editor and the terminal. To get going, one must be well equipted. Obviously you are here to do so. Let's not delay!

## Text Editor

One of the key tools to the coder is the text editor. As with any profession, one can only be as good as the tools at hand. Therefore, it is important to know what to look for in a text editor. However, keep in mind, a text editor is a personal choice. Ultimately, the choice dependent on what the coder likes best. 

#### Text Editor vs IDE 
An IDE (Integrated Development Environments) is a text editor, and more. IDEs are a combination of various software, such as compliers, debuggers, built-in terminals, etc. Purists would say text editors are simply for editing text, nothing more. It can be hard to draw the arbitrary line.

While text editors can be fancy, sometimes simple is good. Minimalism is a beautiful thing. And every computer comes with a text editor. For Windows, it's Notepad. On Mac, Text Edit. And while these editors may be lacking, they can also be expanded to hold more powers through modified versions. Best to skip the dedicated word processors though. Formatting, styling and autocorrections in a word processor, such as Microsoft Word of Pages, will be of no help. Any formatting will not make it into the actual code. Actually, you will probably become irrate trying to use a word proccessor. Best advice is to skip.

Okay. Sounds good. Perhaps you want more?

## Important Features One Should Look for in a Text Editor

1. ### Code Completion
   
   **Code completion** is arguably the most useful feature. When initing typing, a good code completion software will pull up a list of predictive suggestions to allow for easy completion. Thi saves countless hours of searching for the correct characters and saves a ton of effort later by helping to prevent typing errors. One very popular code completion extension is Emmet. Emmet works assist the coder to quickly complete HTML and CSS code with ease. 
3. ### Syntax Highlighting

Secondly, and arguably a close one, is **syntax highlighting**. Syntax highlighting is what gives color to one's code, and not half-hazzardly. Coloration is added intelligently and automatically by coloring different parts of code differently. This massively improves the readability, thus allowing the coder to quickly identify where to make changes throughout the code at hand. 

4. ### Extensions

The world of coding offers a plethora of cures to acking needs. **Extensions** are like magic potions when it comes to features. Extentions can complete what might otherwise be lacking in the coder's text editor environment. Chances are, if you feel it is a strong need, someone else has already agreed with you and built it out. 

5. ### Themes

While perhaps not essential, **themes** are a nice feature which adds some life to one's software. It allows them to customize it to their personality. And moreover, themese which are easy for the coder to read and which produce less eye strain arguably is of great value to many. 

___

### Choice Text Editors
A strong list of editors can be found at the wikipedia article. [https://en.wikipedia.org/wiki/List_of_text_editors](https://en.wikipedia.org/wiki/List_of_text_editors)

For a more currated 2023 list, TechRadar has some great candidates. [https://www.techradar.com/best/best-text-editors](https://www.techradar.com/best/best-text-editors])

## Terminal



### Terminal Commands

`pwd` - Print working directory, which is the current folder.

`ls` - List directories under the current directory, if not otherwise specified.

`cd` - Change directory to the home directory, unless a location is specified.

`mkdir` - Make a new directory. That which is input afterwards will be the name of the new folder. 

`touch` - Creates a new file. That which is input afterwards will be the name of the new file. The file extension should also be entered immediately following the file name, such as `.pdf`, `.png`,  etc. 

### Examples:

What is happening in the following commands?

1. `cd projects`
2. `mkdir new-project`
3. `touch new-project/newfile.md`
4. `cd ..`
5. `ls projects/new-project`

Let's break it down.
1. Under the current directory, the subdirectory "projects" is being selected to become the current directy in use. The code `cd` is a *command* and prepresents the current directory selection. And `projects` is the *argument*, representing the directory being selected. Commands and arguments are always separated by spaces. 
2. Within the current directory, a new subdirectory is being created, named, "new-project". The code `mkdir` represents creating the new directory, and `new-project` represents the title of the directory being created. 
3. A new file is being created. The code `touch` informs the system to create a new file, while `new-project/newfile.md` specifies the location and new file name, `new-project/` being the prior, and `newfile.md` being the later. 
4. From the current directory, the current directory is being changed to the directory superior to the current directory. In other words, the current directory is being changed to the directory which is currently the parent directory. The code `..` represents one folder up. 
5. With this command the list of folders within a directory is given as an output. The code `ls` represenets the list command, while the the `projects/new-project` represents the folder of which to list the all the subfolders that exist thereunder. 
