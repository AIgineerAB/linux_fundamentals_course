# tmux - a terminal multiplexer

<a href="https://youtu.be/dUUPOnkc74Q" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/tmux.png?raw=true" alt="tmux video"/>
</a>

## setup tmux

```bash
sudo dnf install tmux
```

## tmux commands

Start tmux running `tmux` in bash. `ctrl+b` is the prefix key combination in tmux which means that the next key I press is a tmux command. 

To split into two vertical panes do `ctrl+b %`. 

  <img src="https://github.com/kokchun/assets/blob/main/linux/tmux_2_cols.png?raw=true" alt="tmux video" width=500/>


Then to split it further vertically like this figure do `ctrl+b "`


  <img src="https://github.com/kokchun/assets/blob/main/linux/tmux_3_layout.png?raw=true" alt="tmux video" width=500/>
  
  <br>
  To jump between terminal windows do `ctrl+b q <number>` for example `ctrl+b q 1` to jump to top right. 

  <img src="https://github.com/kokchun/assets/blob/main/linux/tmux_navigation.png?raw=true" alt="tmux video" width=500/>


Also possible to navigate around using `ctrl+b arrowkey`