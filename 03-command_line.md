# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

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

> >* `pwd`- show current working directory path
> >* `mkdir`- creating a directory
> >* `rm -r`deleting a directory
> >* `touch`- creating a file using `touch` command
> >* `rm` - deleting a file
> >* `mv`- renaming a file
> >* `ls -a`- listing hidden files
> >* `cp`- copying a file from one directory to another
> >* `cd ..` -Moves one level up the directory, add /.. for more levels
> >* `grep`- searches for files that match the filter, case sensitive


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

> > `ls`  - lists visible files in folder/ directory  
`ls -a`  - lists all files in folder / directory  
`ls -l`  - lists files in table (long form) format  
`ls -lh` - lists files in table (long form) format, and presents it in human readable form  
`ls -lah` - lists all files in table format, and presents it in human readable form  
`ls -t`  - lists files in order of date modified  
`ls -Glp`  - omits group name, list files in long format, and adds a "/" to the end of the directory


---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

> > `-m` - Displays the names as a comma-separated list  
`-R`- Displays subdirectories
`-r`- displays in reverse order
`-u`- organizes by access time
`-1`- displays each item as a row

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.

> > `xargs` can be used to build commands through standard inputs, and is helpful when filtering for files. For example, if i were to try to find files within a directory with an certain extention, I could pipe that output into xarg grep to determine files that contain files matching the grep argument.

 

