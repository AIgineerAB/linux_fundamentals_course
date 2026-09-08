# Vim

<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt="file management" width="600">
</a>


It is good to learn a text editor, and if you are interested, you can learn vim. It has a somewhat high learning curve, but once you get used to it, you will be able to move around quite nicely.


## Start vim 

```bash
vim <filename> 
```

## Normal mode 

Normal mode is kind of like "menu", which allows you to move around, copy lines, delete lines etc. 

### Navigation 

You can navigate using hjkl or using arrow keys.

```bash
h # left
j # up
k # down
l # right
```


### Cut, yank, paste

```bash
dd # delete line 
dd # cuts 3 lines
p # paste lines

```


## Insert mode 

If you want to put in text like a plain text editor, you want to enter into insert mode. Here are different ways to enter into insert mode

```bash
i # insert mode where the cursor is 
o # insert mode one line below cursor and adds the line
O # insert mode one line above cursor and adds that line
```


## Repeating a command

Base command to repeat commands
```
[number][command]
```

A few examples
```bash
3yy # yanks 3 lines
4dd # cuts 4 lines
10k # junmps up 10 lines
3o # open new line below in insert mode then repeat 3 times
```

## Other videos 📹

## Read more 👓
- [vim cheatsheet](https://vim.rtorr.com/)

