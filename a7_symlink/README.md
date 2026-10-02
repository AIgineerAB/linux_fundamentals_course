# Create shortcuts with symlinks 

<a href="https://youtu.be/_bMWj-aOQ_M" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/symlink.png?raw=true" alt="symlinks" width="600"/>
</a>

## symlink

1. Create a script e.g. `gitf` here 
2. Create a symlink (shortcut) to ~/.local/bin/gitf

```bash
ln -s "$PWD/gitf" ~/.local/bin/gitf 
```

Now it is possible to update gitf and then it will be reflected in the symlink. Also placing it in ~/.local/bin/gitf because it exists in PATH variable by default, which means you can immediately use gitf command in your system.

