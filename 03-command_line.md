# Learn command line

Please follow and complete the free online [Command Line Crash Course
tutorial](https://web.archive.org/web/20160708171659/http://cli.learncodethehardway.org/book/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. Each "chapter" focuses on a command. Type the commands you see in the _Do This_ section, and read the _You Learned This_ section. Move on to the next chapter. You should be able to go through these in a couple of hours.

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

> > **Commands**  
**ls:** lists files and folders in the working directory  
**ls options:**  
   -a: shows files that are hidden (denoted by a “.” at the beginning of file name)  
   -l: lists all contents of a directory in long format  
   -t: orders files and directories by time last modified  
**pwd:** lists path of current directory  
**cd [directory name]:** way to switch into a different directory (“change directory”)  
**cd.. :** moves back/up one directory  
**mkdir [directory name]:** creates a new directory in the current working directory  
**touch [file name]:** creates a new file in the current working directory  
**cp [source file/directory] [destination file/directory]:** copies files from one directory to another  
**mv [source file/directory] [destination file/directory]:** moves or renames files or directories, works similar to cp.
**rm:** deletes files   
**rm -r:** deletes directories  
**echo:** echoes an input back to the terminal as an output  
**>:** redirects standard output to a file  
**cat:** outputs contents of a file to the terminal  
**>>:** appends to the file
**| :** “pipe” takes standard output of command to left and pipes it as standard input to the command on the right  
**sort:** sorts alphabetically  
**uniq:** filters out adjacent duplicates  
**grep:** searches files for lines that match a pattern and returns those results (similar to filter “content that contains…”) - case sensitive  
**grep -i:** enables to be case insensitive  
**grep -R:**  searches all files in a directory and outputs filenames and lines containing matched results  
**grep -Rl:** searches all files in a directory and outputs only filenames with matched results  
**sed:** stream editor - modifies strings in an expression and outputs it (“find and replace” functionality), only finds the first instance of the word to replace in a given line  
	s: substitution - always use with sed  
	format: sed ’s/find_string/replace_string’ [file]  
	g: replaces all instances in a line instead of just first  

---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

> > `ls` - lists files and folders in the current working directory  
`ls -a` -  lists all files and folder in the working directory including hidden files (which start with “.”)  
`ls -l`  - lists files and folders of a directory in long format  
`ls -lh` - lists files and folders of a directory in long format with readable file size  
`ls -lah` - lists files, folders and hidden files of a directory in long format with readable file size  
`ls -t`  - lists all files and folders in order by time last modified  
`ls -Glp` - lists files and folders in long format without group names but with a slash at the end of folders  

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > `ls -d` Displays only directories.  
`ls -m`	Displays the names as a comma-separated list.  
`ls -r`	Displays files in reverse order.  
`ls -R`	Displays subdirectories as well.  
`ls -t`	Displays newest files first. (based on timestamp)  

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > Xargs takes an input from stdin and executes a command to echo over it, meaning it will output what is in the stdin. It has a number of options that can tweak how it is output such as specifying the number of items on a line. If I were to input $ xargs -n 3 and my stdin is 'hello my name is shireen' it would result with 'hello my name' on the first line and 'is shireen' on the second. 
 

