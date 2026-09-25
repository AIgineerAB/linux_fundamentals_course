# PS1 variable - prompt string

<a href="https://youtu.be/p1bctzY1Uc4" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/PS1_variable.png?raw=true" alt="file management" width="600"/>
</a>

## Configure PS1

I will configure my prompt string to look like this 

  <img src="https://github.com/kokchun/assets/blob/main/linux/PS1.png?raw=true" alt="file management" width="600"/>

To do that open up bashrc and configure it 

```bash
vim ~/.bashrc
```

Then add this line 

```bash
PS1='\[\e[1;32m\]\u@oracle_yt:\[\e[1;34m\]\W\[\e[0m\] \$ '
```

You don't need to understand all details, but here is a reference so that you can modify it

- \[ syntactic sygar -> tells bash these characters following don't take up screen space. Bash needs to keep track of screen space to know where the cursor is
- \e ANSI escape sequence -> interpret as command and not text
- 1 -> bold
- ; -> separator
- 32 -> green color
- m -> apply the style
- \u -> user
- 34 -> blue
- \W -> last part of current directory
- 0m -> resets all color styles