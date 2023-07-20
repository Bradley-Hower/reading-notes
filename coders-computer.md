## *Class 102, Entry 3: Coder's Computer*

The **coder's computer** is ulimately the repository for all the coder's tools. One of those key tools is the text editor. As with any profession, one can only be as good as the tools at hand. Therefore, it is important to know what to look for in a text editor. 

### What are some important features one should look for in a text editor? 

+ **a
+ **b
+ **c
+ **d
+ **e

### Terminal Prompts

`pwd` - Print working directory, which is the current folder.

`ls` - List directories under the current directory, if not otherwise specified.

`cd` - Change directory to the home directory, unless a location is specified.

`mkdir` - Make a new directory. That which is input afterwards will be the name of the new folder. 

`touch` - Creates a new file. That which is input afterwards will be the name of the new file. The file extension should also be entered immediately following the file name, such as `.pdf`, `.png`,  etc. 

### Examples:

What is happening in the following prompts?

1. `cd projects`
2. `mkdir new-project`
3. `touch new-project/newfile.md`
4. `cd ..`
5. `ls projects/new-project`

Let's break it down.
1. Under the current directory, the subdirectory "projects" is being selected to become the current directy in use. The code `cd` prepresents the current directory selection, and `projects` represents the directory being selected. 
2. Within the current directory, a new subdirectory is being created, named, "new-project". The code `mkdir` represents creating the new directory, and `new-project` represents the title of the directory being created. 
3. A new file is being created. The code `touch` informs the system to create a new file, while `new-project/newfile.md` specifies the location and new file name, `new-project/` being the prior, and `newfile.md` being the later. 
4. From the current directory, the current directory is being changed to the directory superior to the current directory. In other words, the current directory is being changed to the directory which is currently the parent directory. The code `..` represents one folder up. 
5. With this command the list of folders within a directory is given as an output. The code `ls` represenets the list command, while the the `projects/new-project` represents the folder of which to list the all the subfolders that exist thereunder. 
