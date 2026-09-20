# Exercise 1 - permissions, bash scripting

In this exercise, you get to familiarize yourself with Linux, the terminal, the unix shell and bash. 

These exercises require that you have already setup Linux.

> [!TIP] 
> it's good if you work with a git repository when doing these exercises. You could write down the answers on markdown files to document your work so that you can come back and reference it in the future. Also it's good to practice working with version control

> [!TIP]
> ssh into your VM to work with these exercises

> [!TIP]
>  throughout this course it is good to familiarize yourself with the text editors that are preinstalled to linux

## 0. Square

Create a program bash script that prompts the user for a side and then calculates and outputs the perimeter and area. Example

```bash
Enter a side for square: 2
A square with side 2 has perimeter: 8 and area: 4
```

## 1. Rectangle

Similar as above but prompt for length and width

## 2. Circle

Similar as above but prompt for radius. Also check if the circle is a unit circle, i.e. with radius 1. 

## 3. Take in argument

Modify the scripts above to take in argument directly when executing the script rather than prompting the users.

For example 

```bash
./square_arg 2
A square with side 2 has perimeter: 8 and area: 4
```

```bash
 ./circle_arg 1
Perimeter of circle is: 6.2830
Area of circle is: 3.1415
It is a unit circle
```

Also check give error if no argument was given

For example 

```bash
 ./circle_arg 
 an argument for the radius is required
```


## 5. Bash script to create a folder structure

Create a shell script called create_repo_template that creates a template skeleton for an empty github repo 

It should create the following file structure



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