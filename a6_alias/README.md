# Use alias to create comfortable shortcuts

TODO: video

<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt="file management" width="600"/>
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
alias ..='cd .. && ls'                  
alias c=clear 
```


