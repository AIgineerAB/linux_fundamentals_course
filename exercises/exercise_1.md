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

Create a shell script called create_template that creates a template skeleton for an empty github repo 

It should create the following file structure

```bash
.
├── create_template
├── dirs.txt
└── template
    ├── 00_intro
    │   └── README.md
    ├── 01_setup
    │   └── README.md
    ├── 02_nav
    │   └── README.md
    └── 03_bash
        └── README.md
```

Create a file called dirs.txt which contains 

```
00_intro 01_setup 02_nav 03_bash
```

Now run the script using 

```bash
./create_template $(cat dirs.txt)
```




## 6. Theory questions

a) What is a bash script? 

b) What is the shebang line for bash and what is the purpose of it

c) Why can't you normally not execute a bash script directly. How to modify so that you can execute it 

d) How does if-statement differs from case? 

e) What is the output of `echo $((4/2))`

f) What is the output of `echo $((5/2))` and why? How to make it get the correct output?

## Glossary

Fill in this table either by copying this into your own markdown file or copy it into a spreadsheet if you feel that is easier to work with.

| terminology  | explanation |
| ------------ | ----------- |
| bc           |             |
| shebang      |             |
| bash         |             |
| stdin        |             |
| stdout       |             |
| if statement |             |
| case         |             |
| for          |             |
| while        |             |
| conditional  |             |
| $#           |             |
| $@           |             |
| $1           |             |
| arguments    |             |
| ./           |             |
| chmod        |             |
| chown        |             |
| tmux         |             |
| PS1          |             |
| clobbering   |             |
| >            |             |
| >>           |             |
|              |             |
|              |             |