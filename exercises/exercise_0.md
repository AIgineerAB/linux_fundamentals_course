# Exercise 0 - First glance at Linux

In this exercise, you get to familiarize yourself with Linux, the terminal, the unix shell and bash. 

These exercises require that you have already setup Linux.

> [!TIP] it's good if you work with a git repository when doing these exercises. You could write down the answers on markdown files to document your work so that you can come back and reference it in the future. Also it's good to practice working with version control

> [!TIP] in the beginning of your terminal adventure it could be good to have the GUI opened at the same time to see what each command does


> [!TIP] throughout this course it is good to familiarize yourself with the text editors that are preinstalled to linux


## 0. Simple navigation

Open up a terminal and do the following

&nbsp; a) Check where you are with `pwd`

&nbsp; b) Check what files exists in your current directory 

&nbsp; c) Go up a directory and repeat a) and b)

&nbsp; d) The root is /, so do `cd /` 

&nbsp; e) List and write down the folders inside of root 

&nbsp; f) From the root, cd back to your repository 

## 1. File management

Go into your local repository with bash

&nbsp; a) Create the following file structure in your repository 

```bash
.
├── 03_navigation
│   └── README.md
├── 04_file_management
│   └── README.md
├── exercise0
│   └── README.md
├── exercise1
│   └── README.md
├── exercise2
│   └── README.md
├── exercise3
│   └── README.md
```

Commit and push these to your github 

>[!NOTE] you should add more directories and files when needed to your repo 

&nbsp; b) Open up exercise0/README.md and add some documentation on how you solved different tasks.

&nbsp; c) Navigate to exercise0 and create 3 files called file1.md, file2.md, file3.md. Use globbing to achieve this

&nbsp; d) Create a directory called files and move these files into this directory

&nbsp; e) Move file2.md out to exercise0

&nbsp; f) Put in the text "Hello file2" into file2.md. Use `echo` together with output redirection `>>` 

&nbsp; g) Copy file2.md and call the new copy file2.txt

&nbsp; h) Output the content from both the files

&nbsp; i) Lets cleanup by removing all files in exercise0 except for README.md

&nbsp; j) Use a terminal text editor such as nano or vim to document these questions on README.md


## 2. Searching text

Download this text about [GNU/Linux from project gutenberg](https://www.gutenberg.org/cache/epub/6527/pg6527.txt). Use `curl` and save it in a file called `linux.txt`.

&nbsp; a) Use a pager on this text file and try the following:
- scroll page down with space and b to do page up
- / to search for a string e.g. search for linux 
- n to go forward in search and b to go backwards
- jk to scroll up and down
- q to quit

&nbsp; b) Use grep to search for debian 

&nbsp; c) Now search for debian and Debian (case insensitive search)

&nbsp; d) Search for debian and redirect the output to a file called debian.txt

&nbsp; e) Search for linux case insensitive and then pipe the output to further refine the search to search for the word partition

&nbsp; f) Search for GNU and then count the number of lines where GNU occur. 

&nbsp; g) Count number of time the word "server" appear


&nbsp; h) Count number of time the word starts with "server" appear case insensitive ex servers, Servers, Server, server


## 3. Theory questions

&nbsp; a) We usually open up a terminal to write commands, but then we talk about the shell. What are the different roles of the terminal and the shell?

&nbsp; b) Why would you use a shell to control the computer, when there is also a GUI that is simple to use? 


&nbsp; c) How does shell, bash and terminal relate to each other?


&nbsp; d) Describe the most common commands for navigation in bash?


&nbsp; e) Is a directory a file in Linux?


&nbsp; f) The CPU is said to be able to operate in kernel mode and user mode. What are the main purposes of each of the modes? 


&nbsp; g) Which other shells than bash exists?


&nbsp; h) What is pager like `less` used for? Isn't `cat` enough for outputting text from a file? 


&nbsp; i) What are the differences between git and github?


## Glossary

Fill in this table either by copying this into your own markdown file or copy it into a spreadsheet if you feel that is easier to work with.

| terminology          | explanation |
| -------------------- | ----------- |
| linux                |             |
| debian               |             |
| virtual box          |             |
| unix                 |             |
| RHEL                 |             |
| bash                 |             |
| shell                |             |
| terminal             |             |
| GUI                  |             |
| globbing             |             |
| grep                 |             |
| ls                   |             |
| pwd                  |             |
| cd                   |             |
| echo                 |             |
| cat                  |             |
| input redirection  < |             |
| output redirection > |             |
| virtual machine      |             |
| virtualbox           |             |
| ssh                  |             |
| github               |             |
| git                  |             |
| pager                |             |
| less                 |             |
| man                  |             |
| pipe                 |             |
| find                 |             |
| locate               |             |
|                      |             |
