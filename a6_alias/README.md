# Use alias to create comfortable shortcuts

<a href="https://youtu.be/I-NvxPYVWNE" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/alias.png?raw=true" alt="alias" width="600"/>
</a>

## alias

You can create shortcuts for longer commands using alias 

```bash
# does cd .. and prints out cd .. and ls and then perform ls 
alias ..='cd .. && echo "cd .. and ls" && ls'
```
However this alias disappears after the terminal session. To keep your permanent, go and modify `.bashrc`

```bash
vim ~/.bashrc

# add the aliases you want, e.g.
alias ll='ls -alF --color=auto'         
alias ll='ls -alF --color=auto'         
alias gs='git status'                   
alias ..='cd ..'                  
alias c=clear 
alias github='cd ~/Documents/github'
alias ehco=echo
alias l=ls
alias sbash='source ~/.bashrc'
```


